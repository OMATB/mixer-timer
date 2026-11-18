# mixer-timer

Firmware releases for the mixer sequence timer.

Boards fetch `firmware.bin` and `version.txt` from the release marked **Latest**.

## How a release is made

1. The firmware and version file go in a new folder `releases/vX.Y.Z/` (optional `notes.md`).
2. When that folder is pushed to `main`, GitHub Actions creates a **draft** release from it
   (`.github/workflows/draft-release.yml`). It refuses if `version.txt` and the folder name disagree,
   and never touches a version that already has a release.
3. A person checks the draft and clicks **Publish**. Only then can boards see it.
