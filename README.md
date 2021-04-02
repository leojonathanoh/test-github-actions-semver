# test-github-actions

[![github-actions](https://github.com/leojonathanoh/test-github-actions/workflows/ci-master-pr/badge.svg)](https://github.com/leojonathanoh/test-github-actions/actions)
[![github-tag](https://img.shields.io/github/tag/leojonathanoh/test-github-actions)](https://github.com/leojonathanoh/test-github-actions/releases/)
[![docker-image-size](https://img.shields.io/docker/image-size/leojonathanoh/test-github-actions/latest)](https://hub.docker.com/r/leojonathanoh/test-github-actions)

## Workflows

### Build

Trigger: `git push origin push` or PR

- `ci-master-pr`: CI

### Releases

#### semver-based releases

Trigger: `git checkout release && git merge --no-ff master`.

- `ci-release`: CI on branch `release`, ends by tagging its `HEAD` in format: `v<MAJOR>.<MINOR>.<PATCH>`, which will be an official release. Creates the release based on tag `v<MAJOR>.<MINOR>.<PATCH>`, publishing release notes.

#### date-based releases

Trigger: `git checkout release-tags-date && git merge --no-ff master`.

- `ci-release-tags-date`: CI on branch `elease-tags-date`, ends by tagging its `HEAD` in format: `YYYYMMDD.<MINOR>.<PATCH>`, which will be an official release.
- `ci-tags-date`: Creates the release based on tag `YYYYMMDD.<MINOR>.<PATCH>`, publishing release notes.

