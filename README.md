# Flatcap for Stylus

![Version](https://img.shields.io/badge/version-2.0.0-blueviolet) ![Stylus](https://img.shields.io/badge/Stylus-UserCSS%20%2B%20LESS-blue) ![License](https://img.shields.io/badge/license-MIT%20%2B%20third--party%20notices-blue)

<p align="center">
  <img src="https://raw.githubusercontent.com/cheycron/flatcap-userstyles/main/images/reddit-slate.png" alt="Flatcap Slate on a Reddit user page: matte dark canvas, mineral-blue accent, personal data blurred" width="100%">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/cheycron/flatcap-userstyles/main/images/reddit-daylight.png" alt="Flatcap Daylight on a public Reddit community page: light neutral canvas with a blue accent" width="100%">
</p>

<p align="center"><sub>Flatcap Slate (dark) above, Flatcap Daylight (light) below, on Reddit.</sub></p>

**Flatcap for Stylus** brings the Flatcap visual system to four websites through UserCSS: Gemini, Gmail, Instagram and Reddit. Matte surfaces, one mineral-blue accent, and an interface that stays in the background.

Each style keeps the selectors and behaviors it already had on the site; only the colors, fonts and focus treatment changed to Flatcap 2.0. Slate and Daylight are available in every style.

> The interface organizes. Content takes the foreground. Color informs.

## Install

Requires [Stylus](https://add0n.com/stylus.html) ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/), [Chrome / Edge / Brave](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne)). Stylus recognizes `*.user.less` files natively.

Click a link below and Stylus opens its install page (Firefox may ask to confirm). Every style updates itself from the same `main` URL.

| Site | Install | Besides recoloring |
| :--- | :--- | :--- |
| **Gemini** | [gemini.google.com.user.less](https://raw.githubusercontent.com/cheycron/flatcap-userstyles/main/styles/gemini.google.com.user.less) | Hides upsell buttons and location footers; the prompt toolbar fades in on hover or focus. |
| **Gmail** | [gmail.com.user.less](https://raw.githubusercontent.com/cheycron/flatcap-userstyles/main/styles/gmail.com.user.less) | IBM Plex Sans Condensed for dense lists. The message body keeps its own light colors on purpose. |
| **Instagram** | [instagram.com.user.less](https://raw.githubusercontent.com/cheycron/flatcap-userstyles/main/styles/instagram.com.user.less) | Maps Instagram's color variables to Flatcap roles; sprites and logos are inverted in Slate only. |
| **Reddit** | [reddit.com.user.less](https://raw.githubusercontent.com/cheycron/flatcap-userstyles/main/styles/reddit.com.user.less) | Hides the home-feed right rail and widens the feed; community info panels stay. |

If the link opens as plain text, copy the URL and use Stylus → *Write new style* → *Import*, or clone the repository and drag a `styles/*.user.less` file onto a Firefox tab (Chromium: Stylus's [Installing local files](https://github.com/openstyles/stylus/wiki/Writing-UserCSS#installing-local-files)).

## Use it

Every style has two options in the Stylus config panel:

| Option | Values | Default |
| :--- | :--- | :--- |
| Color mode | Follow system, Slate (dark), Daylight (light) | Follow system |
| Load IBM Plex from Google Fonts | on / off | on |

*Follow system* emits both modes and lets `prefers-color-scheme` choose, so it switches live. Slate and Daylight force one mode and set `color-scheme` to match. The Gmail message body keeps its own light colors in every mode.

## Fonts

The styles use **IBM Plex Sans** (Gmail also **IBM Plex Sans Condensed**) and **Cascadia Code** for code. With *Load IBM Plex from Google Fonts* off, no request is made to Google Fonts and the stack falls back to the installed fonts, then to system fonts. Fonts are not bundled. See the [Flatcap typography guide](https://github.com/cheycron/flatcap-theme/blob/main/docs/typography.md).

## Accessibility

Text and control roles are chosen against the contrast contracts of the [Flatcap core](https://github.com/cheycron/flatcap-theme), and `python3 scripts/build.py --check` fails if a role pair misses its target. Focus rings use the `focus.ring` role with a 2px width and offset.

Limits that affect you: the core's increased-contrast overrides (`contrast.*`) are not wired into these styles yet, and the check covers the roles the styles paint, not a pixel-level audit of the live sites. Details are in the [full mapping](https://github.com/cheycron/flatcap-userstyles/blob/main/docs/mapping.md).

## Compatibility

Tested by the author in Firefox with Stylus on Gmail, Gemini, Instagram and Reddit in Slate. Daylight and *Follow system* compile and pass the build checks, but only Reddit Daylight has been rendered (without a session). The sites change their markup often, so a selector can stop matching; please [open an issue](https://github.com/cheycron/flatcap-userstyles/issues). Chromium with Stylus should work but is untested.

## Upgrading from v1

The styles are renamed (`Flatcap — <Site>`) and share one namespace, so Stylus installs them as new styles. Disable or remove the old entries (*Gemini - Clean Flatcap*, *Gmail - Flatcap Theme*, *Instagram - Flatcap Theme*, *Reddit - Flatcap (Tokyo Port)*) to avoid two themes fighting over the same page.

## Contributing

The token block in each `styles/*.user.less` is generated from `src/theme.json`; do not edit it by hand. Run `python3 scripts/build.py --check` before opening a pull request. See [docs/mapping.md](https://github.com/cheycron/flatcap-userstyles/blob/main/docs/mapping.md) and [AGENTS.md](https://github.com/cheycron/flatcap-userstyles/blob/main/AGENTS.md).

## License

MIT © Cheycron Blaine. See [LICENSE](https://github.com/cheycron/flatcap-userstyles/blob/main/LICENSE).

Three of the four styles derive from third-party UserStyles, credited in full in [NOTICE.md](https://github.com/cheycron/flatcap-userstyles/blob/main/NOTICE.md): Reddit (JoshuaMarkle), Gmail (Catppuccin) and, published here with the author's decision, **Gemini** (*gemini clean* by [sonho](https://userstyles.world/style/25979)) and **Instagram** (*Dark & simple instagram* by [sergio9929](https://userstyles.world/style/536/dark-simple-instagram)). Those two upstreams do not declare a clear license, so their parts are **not covered by the MIT grant** and no extra permission is claimed. If an original author asks, the style is adjusted or removed.

## Support

If Flatcap makes your workspace calmer, you can support its development.

<p align="center">
  <a href="https://www.buymeacoffee.com/cheycron">
    <img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me a Coffee">
  </a>
</p>
