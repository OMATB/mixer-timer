# mixer-timer

Firmware releases for the mixer sequence timer.

Boards fetch `firmware.bin` and `version.txt` from the release marked **Latest**.

## How a release is made

1. The firmware and version file go in `releases/vX.Y.Z/` (optional `notes.md`).
2. A tag `vX.Y.Z` is pushed.
3. GitHub Actions creates a **draft** release from those files
   (`.github/workflows/draft-release.yml`). It refuses if `version.txt` and the tag disagree.
4. A person checks the draft and clicks **Publish**. Only then can boards see it.
