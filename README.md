# Omarchy theme loops

The live background loops for the built-in Omarchy themes: a quiet version of a theme's still that keeps moving, which OWE plays in the still's place while animations are on. They ship as the `omarchy-themes-loops` package, which installs `<theme>/<name>.mp4` here to `/usr/share/omarchy/themes/<theme>/backgrounds/loops/<name>.mp4`.

A loop plays in place of the still with the same name in that theme in [omacom/omarchy-themes-backgrounds](https://github.com/omacom/omarchy-themes-backgrounds), so `lumon/01-united-in-severance.mp4` belongs to `lumon/01-united-in-severance.webp` there. Its first frame is that still and its last frame leads straight back into it. See `docs/theming.md` in [omacom/omarchy](https://github.com/omacom/omarchy) for how loops play.

`bin/check` holds every loop to the format `docs/theming.md` asks for, so the hand-over from the still and each restart stay seamless: H.264 with no B-frames, one keyframe, colour tags, twenty seconds or less, and its still's shape at no larger than its size.

To add or change a loop, open a pull request here. Once it merges, cut a release tagged with the date, `vYYYY.MM.DD` (or `vYYYY.MM.DD.1` for a second one that day). [omacom/omarchy-pkgs](https://github.com/omacom/omarchy-pkgs) picks the release up and updates `omarchy-themes-loops` to it.
