## A-Frame

When builds are built, make sure the source map URLs at the bottom of the builds are correct.

- Update CHANGELOG.md. Go through each commit in the Git log since the last release and include every notable patch. The categories should be `Major Changes`, `Deprecations`, `Enhancements`, `Performance`, `Bug Fixes`. In each category, loosely sort the more impacting changes at the top.
- Update version field in `package.json`. Push that to GitHub so the bot can build it. Then rebase off that.
- Update `prerelease` command in `package.json` with the before and after versions and `npm run prerelease` to update documentation, README.md, and build filenames with the new version.
- Git tag
- Create and push documentation branch (i.e., `docs-vx.x.0`, only for major versions)
- Create builds for the `dist/` folder with `npm run prerelease`.
- Create builds for the CDN with `FOR_RELEASE=true npm run prerelease`. Copy and push these `aframe.*` builds to the [A-Frame releases repository](https://github.com/aframevr/releases). 
- `npm publish`
- Deploy GitHub pages (`npm run ghpages`).
- Publish GitHub release notes, copying and pasting from CHANGELOG.md

## Site

For major versions.

- Update `aframe.current_version` in `_config.prod.yml`
- Add new version to `multidep.json` config, pointing to the documentation branch
- In `package.json`, update the version in the `bumpdocs` command to have the bot force clean the documentation cache on each update
- Publish blog post
- Update `src/_data/examples.yml`

## Inspector

- Bump builds (`npm run dist`)
- `npm publish`
- Deploy GitHub pages (`npm run ghpages`)

## Misc

- Bump [Glitches](https://glitch.com/~aframe/), owned by @ngokevin
- Announce on social channels
