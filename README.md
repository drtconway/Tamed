# Tamed

Tamed helps Hunters in Classic WoW find the tameable pets that teach each rank of a pet ability, and shows where they spawn on the world map.

Supports Vanilla and The Burning Crusade. Forever support is planned.

![Tamed](/.github/images/Tamed.png?raw=true)
![Pins](/.github/images/Pins.png?raw=true)

This is a fork of [moody/Tamed](https://github.com/moody/Tamed) that adds a zone view.

## Install

In WowUp, choose *Get Addons → Install from URL* and enter `https://github.com/drtconway/Tamed`. Or download the zip from the [releases page](https://github.com/drtconway/Tamed/releases) and unzip it into your `Interface\AddOns` folder.

## Commands

### Toggle

Toggles the user interface.

```txt
/tamed
```

### Clear Pins

Clears all pins from the map.

```txt
/tamed clear
```

## Contributing

Pet ability and NPC data is hand-editable. See [CONTRIBUTING.md](CONTRIBUTING.md) to add or fix entries.

### Releasing

Work happens on `dev`; `master` only changes through pull requests. To release:

1. Move the `[Unreleased]` entries in `CHANGELOG.md` under a new version heading.
2. Open a pull request from `dev` to `master` on GitHub and merge it.
3. Tag the merged `master`:
   `git switch master && git pull && git tag -a v2.1.0 -m "Tamed 2.1.0" && git push origin v2.1.0`,
   then `git switch dev` to carry on.

Pushing the tag does the rest:
- **The workflow:** `.github/workflows/release.yml` runs the BigWigs packager.
- **The zip:** the packager builds `Tamed-<tag>.zip`, leaving out what `.pkgmeta` lists.
- **The version:** it replaces `@project-version@` in the `.toc` with the tag.
- **The release:** it publishes a GitHub release with the zip, `CHANGELOG.md` as its notes, and a `release.json` for WowUp.

## Credit

### Libraries

- [CallbackHandler-1.0](https://www.wowace.com/projects/callbackhandler)
- [HereBeDragons-2.0](https://www.wowace.com/projects/herebedragons)
- [LibDataBroker-1.1](https://www.wowace.com/projects/libdatabroker-1-1)
- [LibDBIcon-1.0](https://www.wowace.com/projects/libdbicon-1-0)
- [LibStub](https://www.wowace.com/projects/libstub)
- [Waffle](https://github.com/moody/Waffle)
- [Wux](https://github.com/moody/Wux)

## License

[MIT](LICENSE)
