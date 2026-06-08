# Upload Guide

This folder is designed to become the root of a public GitHub repository such as:

```text
chronosoothe-research
```

## Recommended GitHub Settings

- Repository name: `chronosoothe-research`
- Visibility: Public
- Description: `Source-audited spatio-temporal acupressure framework for safe non-invasive self-care.`
- README: use the existing `README.md` in this folder
- License: do not choose one until you decide the IP strategy

## Upload Through GitHub Website

1. Create a new public repository on GitHub.
2. Open the new repository.
3. Click **Add file**.
4. Click **Upload files**.
5. Drag all contents of this `research-release` folder into the upload area.
6. Commit with a message such as:

```text
Initial public research release
```

## Upload Through Command Line

From inside this folder:

```text
git init
git add .
git commit -m "Initial public research release"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/chronosoothe-research.git
git push -u origin main
```

## Do Not Upload Yet

For the first public research release, avoid uploading:

- full app source code
- complete private point database
- copyrighted source scans or OCR extracts
- full extracted classical texts
- unreleased commercial strategy
- user data
- private Netlify tokens or deployment settings
- `.env` files

## Suggested First Public Post

> I’m opening an early research repository for ChronoSoothe, a source-audited spatio-temporal acupressure framework for safe, non-invasive self-care. This is not a medical product or clinical claim. The first release focuses on method authority, safety boundaries, source audit workflow, and a public whitepaper draft.

## Next Step After Upload

Open GitHub Issues for:

- expert source review
- Ling Gui Ba Fa test vectors
- local mean solar time terminology
- no-pulse product scope
- point image clarity
- safety wording review
