# Releasing

[A GitHub Action workflow](../.github/workflows/release.yml) automatically
builds a git ref when:
drafts a release when the followings are met:

- A pull request has been created or a branch is pushed

And it drafts a release when the followings are met:
- All builds for targets are successfully built
- The ref has a tag with "v\*"
- If the tag ends with "-pre", the release will be pre-release
