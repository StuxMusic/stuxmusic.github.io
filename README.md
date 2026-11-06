<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.music/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.music/logo-dark.png"><img src="https://global.media.stux.music/logo-dark.png" height="100" alt="Stux.Music Logo"></picture>
</p>

# stuxmusic.github.io

Stux.Music's GitHub Pages redirect: anyone visiting [stuxmusic.github.io](https://stuxmusic.github.io), the org's default
GitHub Pages address, is sent to the org's GitHub profile, [github.com/StuxMusic](https://github.com/StuxMusic).

## How it works

`index.html` is the whole site. A meta refresh sends visitors on immediately, with a canonical link to the same address:

```html
<meta http-equiv="refresh" content="0;url=https://github.com/StuxMusic" />
<link rel="canonical" href="https://github.com/StuxMusic" />
```

It always goes to the profile itself: the path a visitor asked for isn't carried over. GitHub Pages serves it from
`main`, as the org's `<org>.github.io` repository. Stux.Music's own sites are on their own domains, such as
[stux.music](https://stux.music) and [artists.stux.music](https://artists.stux.music).

To change where it goes, edit both URLs in `index.html`. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

Work happens on the `test` branch: releases are committed and tagged there, and go live when Leo merges its pull request into `main`. See [CONTRIBUTING.md](CONTRIBUTING.md#branches).

## Copyright

Copyright © 2026 Stux.Group. All rights reserved.

---

*Built & Maintained by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.music/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.music/icon-dark.png"><img src="https://global.media.stux.music/icon-dark.png" height="14" valign="middle" alt="Stux.Music"></picture> [Stux.Music](https://github.com/StuxMusic), hosted on GitHub Pages.
Stux.Music is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" valign="middle" alt="Stux.Group"></picture> Stux.Group brand of businesses.*
