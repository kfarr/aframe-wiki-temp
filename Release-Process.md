## A-Frame

- Update CHANGELOG.md
- Update version field in `package.json`
- Create versioned builds by modifying the `npm run dist:min` and `npm run dist:max` commands to build `aframe-vx.x.x` vs. `aframe-master`
- Update `prerelease` command in `package.json` with the before and after versions and `npm run prerelease` to update documentation, README.md, and build filenames with the new version.
- Git tag
- Publish GitHub release notes, copying and pasting from CHANGELOG.md
- Create and push documentation branch (i.e., `docs-vx.x.0`)
- Create builds for the CDN by modifying `dist:min` and `dist:max` commands to remove the `-master` suffix. Run `npm run dist`. Copy and push these `aframe.*` builds to the [A-Frame releases repository](https://github.com/aframevr/releases).
- Deploy GitHub pages (`npm run ghpages`).
- `npm publish`

## A-Frame Site

For major versions.

- Update `aframe.current_version` in `_config.prod.yml`
- Add new version to `multidep.json` config, pointing to the documentation branch
- Publish blog post
- Update `src/_data/examples.yml`

## Inspector

Coordinate with Inspector maintainers.

- Bump builds (`npm run dist`)
- Git tag
- Publish GitHub release notes
- `npm publish`
- Deploy GitHub pages (`npm run ghpages`)

## Registry

 For major versions.

- Update `aframe_version` in `package.json`
- Add the A-Frame version to `scripts/build.js` array

## Misc

- Bump A-Frame CDN URL in boilerplates (`aframevr/aframe-boilerplate`), CodePen, and [Glitch](https://glitch.com/~aframe/).
- For major versions, pull request to [algolia/docsearch-configs](https://github.com/algolia/docsearch-configs/blob/master/configs/aframe.json) to index documentation
- Announce on social channels (Twitter, Reddit, HN, Slack)
