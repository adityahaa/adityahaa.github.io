# Aditya Hambire portfolio

A static Astro and TypeScript portfolio presenting education, projects, experience, certificates, and a downloadable resume. The source uses ordinary CSS, progressive animation, and accessible HTML rather than a backend service.

## Source and architecture

Reviewed source is stored in [aditya-hambire-portfolio-source.zip](aditya-hambire-portfolio-source.zip), under `portfolio/`. Content lives in `src/content/*.json`; Astro renders the homepage, project case studies, resume page, sitemap, and 404 page. `src/styles/global.css` supplies responsive styling. Project graphics are workflow illustrations, not screenshots or measured results.

The supplied code configures no visitor login, database, AI service, analytics, third-party fonts, or cookies. Public asset and build audits enforce explicit allowlists. Existing public resume/certificate derivatives remain unchanged.

## Reproduce locally

Use Node.js 24 and the declared pnpm 11.25.0 package manager. From PowerShell:

```powershell
git clone https://github.com/adityahaa/adityahaa.github.io.git
cd adityahaa.github.io
Expand-Archive aditya-hambire-portfolio-source.zip -DestinationPath source
cd source/portfolio
pnpm install --frozen-lockfile
pnpm run check
pnpm run build
pnpm run preview
```

Open the preview URL printed by Astro, normally http://127.0.0.1:4321/. `pnpm run dev` starts editable development. The source package declares Node >=22.22.0. Keep dependency and generated folders out of Git.

Public portfolio: [adityahaa.github.io](https://adityahaa.github.io/). The homepage returned HTTP 200 on 1 November 2026; this does not constitute a complete browser interaction test.

## Deployment and verification

The repository's manual GitHub Actions workflow checks the archive SHA-256, extracts it, builds/audits it, and deploys the static output through GitHub Pages. Pushing documentation does not trigger deployment. See [architecture and deployment notes](docs/ARCHITECTURE.md) for the current procedure and verification evidence; use these notes instead of the archived deployment document's obsolete repository-creation instructions.

## Maintenance and limitations

Edit the JSON content and source components in an extracted working copy. Preserve both file allowlists when adding assets. Repack the reviewed archive and update the workflow's expected SHA-256 together. Build success does not establish browser accessibility or verify every linked credential. This review does not alter the resume, certify personal claims, or introduce publication claims. Do not regenerate the supplied resume with the archive's older asset-generation script.

## Attribution

Portfolio content identifies Aditya Hambire. Git history records repository contributions. Third-party certificate issuers, project collaborators, and dependencies retain their respective attribution and rights; a displayed certificate does not imply employment or publication.

Current checks and unresolved prerequisites: [verification record](docs/VERIFICATION.md).
