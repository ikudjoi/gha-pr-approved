# gha-pr-approved

Pull request approving review count check GitHub composite action, used by Minerva as of Nov 2022.

Composite GitHub action that checks from GitHub API whether the pull request
has enough approving reviews. Will either return truth value or fail on request.

Relies on issuesAndPullRequests API as it's as of my knowledge the only way to conveniently find out
whether a Pull Request has enough approvals specified by the repository branch protection settings.
Head branch name is required to narrow down the search conditions as we were suffering from
GitHub's secondary API rate limit.

Requires the pull-requests read permission to your workflow:

```yaml
permissions:
  pull-requests: read
```

# usage

```yaml
  - uses: FinnishRail/gha-pr-approved@v1
    with:
      pr-number: 123
      head-ref: feat-1
      fail: false
```