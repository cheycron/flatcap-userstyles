# Third-party notices and open licensing questions

This file records where each style comes from and what is **not** settled. It is a good-faith record based on public pages checked on 2026-11-06, not legal advice. The Flatcap 2.0 changes (role tokens, Slate/Daylight, fonts, build scripts) are by Cheycron Blaine and offered under the MIT License; that grant cannot cover upstream code the author did not license.

| Style | Upstream (closest match found) | License the upstream declares | Status |
| :--- | :--- | :--- | :--- |
| Reddit | [Reddit Tokyo Night](https://userstyles.world/style/15549/) / [20093](https://userstyles.world/style/20093/) by JoshuaMarkle | Header: `CC Zero`. API of 15549: `MIT`; API of 20093: `CC Zero` | All 121 custom-property names of the upstream appear in the style. Both candidate licenses are permissive; the discrepancy is on the upstream side. Declared here as `CC0-1.0`, the license in the code header. |
| Gmail | Port of Catppuccin for Gmail: [catppuccin/userstyles `styles/gmail`](https://github.com/catppuccin/userstyles/tree/main/styles/gmail); intermediate copies [Gmail Nord Theme](https://userstyles.world/style/16347/) (MIT) and [Catppuccin gmail](https://userstyles.world/style/16722/) (`No License`) | Official repo: MIT, `Copyright (c) 2021 Catppuccin` | 162 of 372 normalized lines match each of those two copies; the current official port shares 48. The exact ancestor was not established. Declared as `MIT` with the Catppuccin notice below; the chain is still open. |
| Gemini | `gemini clean` by sonho ([userstyles.world/style/25979](https://userstyles.world/api/style/25979)) | `No License` (header and API) | Selectors and variables are shared. **No permission to redistribute or relicense was found.** |
| Instagram | `Dark & simple instagram` by sergio9929 ([userstyles.world/style/536](https://userstyles.world/style/536/dark-simple-instagram), [repo](https://github.com/sergio9929/userstyles)) | Header and API: `No License`. The repo also contains an `UNLICENSE` file (public-domain dedication) while the file itself still says `No License`. | Extensive, specific matches. The two statements conflict, so permission is **not unambiguous**. `Dark-Instagram` by vednoc ([style 30](https://userstyles.world/api/style/30), MIT) matches far less and is not credited as the source. |

## What this means for publishing

- The repository author decided to publish all four styles, **including Gemini and Instagram**, with full credit to sonho and sergio9929 and links to the originals (table above). This is a decision by the author, not a permission granted by the upstream authors.
- Those two upstreams declare no clear license (`No License`; for Instagram, a conflicting `UNLICENSE` file in the repo). Their parts are **not covered by the MIT License** of this repository, and nothing here grants rights the original authors did not. The headers of those two files say `SEE-NOTICE` for that reason, not `MIT`.
- If sonho, sergio9929 or any other original author asks, the style is adjusted or removed promptly (open an issue on this repository).
- Reddit and Gmail are published with the notices kept. The Gmail chain of origin is still not fully established (see table).
- The Reddit baseline credited `Gemini (Auxiliar de Diseño)` as author. That credit is replaced by the repository author for the Flatcap changes, and the upstream author is credited here.

## Catppuccin notice (Gmail)

MIT License. Copyright (c) 2021 Catppuccin. Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, subject to the inclusion of this copyright notice and the full MIT permission notice in all copies or substantial portions of the Software. Full text: <https://raw.githubusercontent.com/catppuccin/userstyles/main/LICENSE>.

## Fonts

The styles reference IBM Plex Sans, IBM Plex Sans Condensed (SIL OFL 1.1) and Cascadia Code (SIL OFL 1.1) by name and optionally load them from Google Fonts. No font files are included.
