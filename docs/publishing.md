# Publishing to GitHub

The studio publishes through the GitHub account connected to the workspace. Only repositories that account can write to are available.

## What can be published

- `README.md`, optionally with the banner and logo at the top.
- `.github/brand/banner.svg` and `.github/brand/logo.svg`. These are stored in the repository itself, so GitHub shows them without relying on this site.
- Pages in `docs/`, such as a code report or the studio's own documentation.
- The repository description and topics.
- A tag and a Release with notes. An existing Release with the same tag is left unchanged.

## Confirmation

After publishing, the studio reads the repository again and shows a checklist: README found, banner and logo linked and present, description matching, tag found, Release published.

## Wiki pages

GitHub does not let apps write Wiki pages. Use **Copy for wiki** on any page and paste it into the repository's Wiki.

## Social preview image

GitHub only accepts PNG or JPG for the social preview, and there is no API to upload it. Set it by hand in the repository settings.
