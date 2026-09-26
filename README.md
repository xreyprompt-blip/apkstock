# apkstock

Public release distribution repository for **nzNoraji** APK and version tracking.

## Files
- `version.json`: Public metadata read by the nzNoraji app to detect newer versions.
- `com.noraji.nznoraji-Signed.apk`: The latest published APK (excluded from Git tree via `.gitignore` to prevent repository bloat, hosted on GitHub Releases).

## Direct Download URL
Latest signed APK can always be downloaded directly from:
`https://github.com/xreyprompt-blip/apkstock/releases/latest/download/com.noraji.nznoraji-Signed.apk`

## Automated Publishing
Run from the root project directory:
```powershell
pwsh scripts/publish_apk.ps1 -Changelog "Rincian catatan rilis"
```
This automatically compiles the Release APK, updates `version.json`, commits and pushes to Git, creates the GitHub Release with the corresponding tag, and uploads the APK binary asset.
