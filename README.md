# Tla updates

The Tla app reads `version.json` from this repo when it opens, to tell users about a new version or to require one.

| Field | Meaning |
|---|---|
| `latest` | The newest version code. Users on an older one see "A new version is available" (they can dismiss it). |
| `latestName` | The newest version name, shown to users (e.g. `0.2.0`). |
| `min` | The oldest version code still allowed. Users below it must update: the app shows only the update screen. |
| `url` | Where the Update button goes (a Play Store page, or this repo's latest release with the APK attached). |
| `notes.ar` / `notes.en` | A short line about what is new, in Arabic and English. |

To announce an update: raise `latest` (and `latestName`, `notes`). To force one: raise `min` too.
Version codes are the `versionCode` in the app's `androidApp/build.gradle.kts`.

GitHub may take a few minutes to serve a changed file.
