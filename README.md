# git-guidelines

## Commit Messages

- Add issue number followed by colon `:`
  - For GitHub and GitLab issue numbers use square brackets `[#123]:`
  - For Jira issues brackets are not needed `PROJ-123:`
- Use the imperative, present tense: "Change" not "Changed" nor "Changes"
- Do capitalize the first letter
- Do not end the first line with a period `.`
- Second line must always be empty
- Use a list to describe changes (in case first line is not enough)
- Separate changes that are not related to current ticket:
  - Use separate section in a commit message OR
  - Use separate commit

## Branch Names

Branch names must be all lowercase and follow the pattern

```bash
${BRANCH_TYPE}-${ISSUE_NUMBER}-${SHORT_DESCRIPTION}
```

for example `fix-123-handle-null-pointer`

### Branch Types

- `feature` or `feat`: when it contains a new feature or code refactoring
- `documentation` or `doc`: any documentation changes
- `test`: when adding tests
- `fix`: for bug fixes

## Commands

### Create Branch

```bash
git branch feature-123-some-description
```

### Change Branch

```
git checkout feature-123-some-description
```

### View Changed Files

```
git status
```

### View Actual Changes

It does not display new files or directories.

```bash
git diff
```

or view specific file(s) or directories

```bash
git diff test.ts
git diff test1.ts test2.ts
git diff src/common
```

### Add For Commit

```bash
git add file1
git add file1 file2 file3
git add src/common
```

### Commit

Always check what is added before commit using `git status`

```bash
git commit
```

or

```bash
git commit -m "Fix race condition in test foo"
```

### Rebase

`-i` means interactive, where commits can be squashed, fixed up or dropped.

```bash
git rebase -i main
```

### Push Branch

```bash
git push -u origin feature-123-some-description
```

### Force Push (Safe)

To override history, for example when squashing commits, always use `--force-with-lease` it prevents overriding if the remote branch is newer.

```bash
git push --force-with-lease
```

### Merge

```bash
git checkout main
git merge feature-123-some-description
git push
```
