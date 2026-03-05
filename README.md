# VideoWall Updates

Public update manifests and portable release artifacts for VideoWall.

## Purpose

This repository is intentionally public and contains only:

- `latest.json` (current update manifest)
- Portable release zip artifacts (uploaded as release assets or stored with manifests)
- Optional checksums/release notes for updater clients

No source code from the private app repository should be added here.

## Manifest Contract (`latest.json`)

```json
{
  "version": "1.1.0",
  "publishedAt": "2026-03-05T00:00:00.000Z",
  "zipUrl": "https://example.com/VideoWall-1.1.0-portable.zip",
  "sha256": "REPLACE_WITH_REAL_SHA256",
  "notes": "Release notes text"
}
```

## Publishing Flow

1. Build a new portable package from private app repo.
2. Produce a zip suitable for replacement install.
3. Compute SHA-256 for that zip.
4. Upload zip to a stable public URL.
5. Update `latest.json` with version/url/hash/notes.
6. Commit and push to this repository.

