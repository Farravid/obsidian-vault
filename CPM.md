
If a repository does not have a version tag, CPM will not be able to find a specific version to download and use. To work around this issue, you can specify a branch, commit hash, or use another mechanism to point to a specific version of the library. Here's how you can handle the situation in your case:

## Solution 1: Specify a branch

If the repository you're using has a specific branch (like main or master), you can directly reference that branch.

```shell
CPMAddPackage(
  NAME yahoo-finance
  GITHUB_REPOSITORY foxadb/yahoo-finance
  GIT_TAG main  # Or whatever the branch name is
)
```

## Solution 2: Specify a commit hash

If the repository doesn't have tags but you want to reference a stable commit, you can specify a commit hash.

```shell
CPMAddPackage(
  NAME yahoo-finance
  GITHUB_REPOSITORY foxadb/yahoo-finance
  GIT_TAG <commit-hash>  # Replace with actual commit hash
)
```

## Solution 3: Add default tag handling

You could also specify GIT_TAG as origin/HEAD, which will automatically use the latest commit in the default branch.

```shell
CPMAddPackage(
  NAME yahoo-finance
  GITHUB_REPOSITORY foxadb/yahoo-finance
  GIT_TAG origin/HEAD
)
```

Try one of these approaches depending on the structure of the repository you're working with.