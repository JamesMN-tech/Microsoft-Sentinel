# Maintaining the GitHub Portfolio

Repository: [JamesMN-tech/Microsoft-Sentinel](https://github.com/JamesMN-tech/Microsoft-Sentinel)

This public repository contains the full lab report, 14 original screenshots, a downloadable Word report, and five explicitly untested KQL starter queries. Its initial README commit is preserved in the publication history.

## Future updates

1. Pull the latest main branch before editing.
2. Add new evidence to the relevant lab. Keep untested queries labeled until execution is documented.
3. Review screenshot identifiers and query results before publication.
4. Stage the intended files, check the diff, commit, and push using your authenticated Git client or connected GitHub tools.

```sh
git pull --ff-only origin main
git add README.md labs queries docs
git diff --cached --check
git diff --cached --stat
git commit -m "Update Sentinel lab evidence"
git push origin main
```

Configure your own Git author name and email if needed. The connected GitHub integration and terminal Git authentication are separate; successful publishing through the integration does not configure terminal credentials.

## Repository conventions

- Keep local document rendering artifacts out of Git.
- Preserve the distinction between verified lab outcomes and proposed exercises.
- Use relative links for report images and downloads.
- No license has been applied. Choose an appropriate license before permitting broader reuse.
