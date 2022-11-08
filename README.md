# checkout_to_anywhere
Github action to checkout a repo to any path, including outside of $GITHUB_WORKSPACE

inputs:
  repository:
    description: 'Repository to clone. Ex.: githubuser/repo'
    required: true
  path:
    description: 'Path to clone the repo to. default is home dir ($HOME)'
    required: false
    default: '$HOME'
  ref:
    description: 'Branch to clone'
    required: false
    default: ''
  token:
    description: 'Personal access token (PAT) used to fetch the repository.'
    required: false
    default: ''


example:
```
- uses: nickohold/checkout_to_anywhere@latest
  with:
    repository: 'nickohold/some_repo'
    ref: 'some_branch_name'
    path: "~/this_path"
```
