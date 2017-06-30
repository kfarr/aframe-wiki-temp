## A-Frame

- Update version field in `package.json`
- Bump builds (`npm run dist`)
- Update `prerelease` command in `package.json` and `npm run prerelease` to update documentation, README.md, and build filenames.
- Git tag
- Publish GitHub release notes, copying and pasting from CHANGELOG.md
- `npm publish`
- Create and push documentation branch (i.e., `docs-vx.x.0`)
- Modify `dist:min` and `dist:max` commands to remove the `-master` suffix. Run `npm run dist` and copy the `aframe.*` builds to the [A-Frame releases repository](https://github.com/aframevr/releases).
- Deploy GitHub pages (`npm run ghpages`).
- Copy build to `aframevr/releases` repo.

## A-Frame Site

- Update `aframe.current_version` in `_config.prod.yml`
- Add new version to `multidep.json` config, pointing to the documentation branch
- Publish blog post
- Update `src/_data/examples.yml`

## Inspector

- Bump builds (`npm run dist`)
- Git tag
- Publish GitHub release notes
- `npm publish`
- Deploy GitHub pages (`npm run ghpages`)

## Registry

- Update `aframe_version` in `package.json`

## Misc

- Bump A-Frame CDN URL in boilerplates (`aframevr/aframe-boilerplate`) and CodePen
- Pull request to [algolia/docsearch-configs](https://github.com/algolia/docsearch-configs/blob/master/configs/aframe.json) to index documentation
- Announce on social channels (Twitter, Reddit, HN, Slack)