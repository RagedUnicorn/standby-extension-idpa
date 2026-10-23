![standby-extension-idpa](docs/standby_extension_idpa_banner.svg)

# Standby extension: IDPA

What [Standby](https://github.com/RagedUnicorn/standby) draws for IDPA stages:

- **Targets**: threat, non-threat, threat with hard cover, and the retention threat with its -0 circle cut out.
- **Props**: a table with an open box on its top, for magazines or a gun staged in the box; port flaps, hinged at the top or at the bottom, set over a port and closed at the start, which the shooter opens to engage through it.
- **Boards** `idpa`: the true outline (seeded from RagedUnicorn/shooting-sports-targets), the hard-cover lines and the non-threat's open hands; `idpa-retention`: the same outline with the body -0 circle (8 in) cut out.
- **Stage defaults**: IDPA stages' movers take the `idpa` board, and a bullet trap carries the threat target.

Standby comes with a release of it. Newer releases reach Standby as updates (Settings, Extensions).

**Viewer:** every element in 2D and 3D, at https://ragedunicorn.github.io/standby-extension-idpa/

## Changing it

An element is its file `elements/<category>/<id>.json`. An element drawn from files has a drawing `assets/2d/<id>.svg` and a model `assets/3d/<id>.glb`. A board is `boards/<id>.json`. The [extension kit](https://github.com/RagedUnicorn/standby-extension-kit) describes the format, and each file names its schema.

- **See your changes**: `npx https://github.com/RagedUnicorn/standby-extension-kit/releases/download/v0.4.0/standby-extension-kit-0.4.0.tgz view` opens the viewer at http://localhost:4310 and reloads it as you save. To see them in Standby, link this folder: Settings, Extensions, Link a folder.
- **Check them**: `npx https://github.com/RagedUnicorn/standby-extension-kit/releases/download/v0.4.0/standby-extension-kit-0.4.0.tgz validate`, as the CI does.
- **In IntelliJ**: the run configurations View and Validate run the two commands above.
- **A pull request** gets a preview of the viewer with each changed element before and after, linked in a comment.
- **Ids never change** once stages use them: Standby finds placed elements by id. The old ids `idpa.paper` and `idpa.noshoot` stay as aliases.

## Releasing

Set `version` in extension.json, merge, and push the tag `v<version>`. The workflow releases `<id>-<version>.zip`, which Standby installs, and publishes the viewer. Standby bundles a release by pinning it: `npm run extensions:bump -- <id>` in the standby repository.

## Licence

MIT
