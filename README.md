# test-github-actions

[![github-actions](https://github.com/leojonathanoh/test-github-actions/workflows/ci-master-pr/badge.svg)](https://github.com/leojonathanoh/test-github-actions/actions)
[![github-tag](https://img.shields.io/github/tag/leojonathanoh/test-github-actions)](https://github.com/leojonathanoh/test-github-actions/releases/)
[![docker-image-size](https://img.shields.io/docker/image-size/leojonathanoh/test-github-actions/latest)](https://hub.docker.com/r/leojonathanoh/test-github-actions)

Example repository with SemVer release workflow.

## Github Workflows

### Build

Trigger: `git push origin master` or PR

- `ci-master-pr`: CI on `master` and PRs. Resolves the next tag in SemVer format `v<MAJOR>.<MINOR>.<PATCH>`, drafts release notes on `master`.

### Releases

#### SemVer releases

Trigger: `git checkout release && git merge --no-ff master`.

- `ci-release`: CI on `release`. Resolves the next tag in SemVer format `v<MAJOR>.<MINOR>.<PATCH>`, creates the release, and publishes release notes.
