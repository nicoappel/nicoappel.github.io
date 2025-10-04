---
tags: template
---

# Space Script: Auto Publish

This Space Script monitors blog posts for status changes to "published" and automatically commits and pushes them to GitHub.

```space-script
silverbullet.registerEventListener({name: "page:saved"}, async (event) => {
  const pageName = event.page;

  // Only process files in blog/_posts directory
  if (!pageName.startsWith("blog/_posts/")) {
    return;
  }

  // Get the page content
  const pageContent = await space.readPage(pageName);

  // Check if status is "published" in frontmatter
  const frontmatterMatch = pageContent.match(/^---\n([\s\S]*?)\n---/);
  if (!frontmatterMatch) {
    return;
  }

  const frontmatter = frontmatterMatch[1];
  if (!frontmatter.includes('status: "published"')) {
    return;
  }

  // Check if this is a status change (not already published)
  const fileName = pageName.replace("blog/_posts/", "");

  console.log(`Publishing ${fileName}...`);

  // Run git commands to commit and push
  try {
    // Git add
    await syscall("shell.run", "git", ["add", fileName], {
      cwd: "/root/apps/silverbullet/data/blog/_posts"
    });

    // Git commit
    await syscall("shell.run", "git", ["commit", "-m", `Publish: ${fileName}`], {
      cwd: "/root/apps/silverbullet/data/blog"
    });

    // Git push
    await syscall("shell.run", "git", ["push"], {
      cwd: "/root/apps/silverbullet/data/blog"
    });

    await editor.flashNotification(`✅ Published ${fileName} to GitHub!`, "info");
  } catch (error) {
    console.error("Publishing error:", error);
    await editor.flashNotification(`❌ Failed to publish: ${error.message}`, "error");
  }
});
```

## How it works

1. Listens for page save events
2. Checks if the page is in `blog/_posts/` directory
3. Reads the frontmatter to check status
4. If status is "published", commits and pushes to GitHub
5. Shows notification of success/failure

## Usage

Simply change `status: "draft"` or `status: "ready"` to `status: "published"` in any blog post and save. The script will automatically commit and push the change.