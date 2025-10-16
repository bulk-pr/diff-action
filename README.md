# diff-action

diff-action is a GitHub Action to output the diff to stdout/stderr and a GitHub Job Summary.

![github-job-summary](https://github.com/user-attachments/assets/1cb3f24b-5a29-4abd-beb0-24f99afa2403)

```
Run git status
HEAD detached at pull/1/merge
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	deleted:    LICENSE
	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	foo.txt
	foo.yml

no changes added to commit (use "git add" and/or "git commit -a")
---

diff --git a/README.md b/README.md
index c84c484..101a875 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,3 @@
 # diff-action
 GitHub Action showing diff
+bar
---

New file (foo.txt):
foo
---

New file (foo.yml):
foo: bar
---
```

## How To Use

```yaml
- uses: bulk-pr/diff-action@main
  with:
    working-directory: foo # Optional
```

## LICENSE

[MIT](LICENSE)
