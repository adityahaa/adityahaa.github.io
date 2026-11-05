# Portfolio architecture and deployment

## System

The reviewed ZIP contains an Astro/TypeScript project under portfolio/. JSON content feeds static Astro pages; ordinary CSS and progressive JavaScript provide presentation. Project routes derive from content slugs. Public resume/certificate derivatives are allowlisted; scripts/audit-public.mjs rejects unexpected assets and scripts/audit-build.mjs checks generated routes/metadata and private references. This review preserves all existing published assets.

## Existing repository deployment

Use the existing repository, not the archived DEPLOYMENT.md instructions to create a new one. .github/workflows/deploy.yml is manually dispatched. It verifies SHA-256 38db2dfcf26d06baacee5fcbde18d42b5c281c92f7356dd5051748139edd95e9 for the source ZIP, extracts portfolio/, uses the declared Node/pnpm toolchain, checks/builds/audits the site, uploads the output, and deploys through GitHub Pages. The workflow sets SITE_URL to https://adityahaa.github.io/.

For a future source change, edit the extracted project, run check/build, review all altered public assets, repack the archive without dependencies/private files, and update the workflow checksum in the same commit. Configure Pages to use GitHub Actions and manually run the existing workflow when deployment is intended. This documentation-only review does not dispatch a deployment or replace the source archive.

## Evaluation and limitations

See [verification record](VERIFICATION.md) for executed checks and any live HTTP verification. A successful response from the homepage does not validate every link, asset, or browser interaction. No performance, accessibility score, admissions outcome, or recruiter conversion result is claimed. Browser checks should cover narrow/wide layouts, keyboard navigation, reduced motion, certificate viewer, resume download, case studies, sitemap, and missing routes.

## Reproduction

Use the root README extraction/install/check/build/preview commands. Content editing and visual review are separate from deploying a changed archive. Do not run the older resume-generation script over the supplied reviewed PDF. Git history and third-party attribution remain unchanged.


## DecisionLens portfolio update — 2026-11-06

Replaced the old RAG Document Chatbot entry with DecisionLens, retaining the existing project
URL. Updated local-runtime status, retrieval methods, comparison/review/export workflow, recorded
pilot results, AI-assisted development disclosure and limitations. No live DecisionLens app is
deployed. Astro check passed without diagnostics; static build and public/build asset audits pass.


## Application-focused portfolio scope — 2026-11-06

At the owner's request, the DecisionLens entry now presents the completed local application.
Paper status, research-pilot metrics and the research-results link were removed from the
portfolio entry. Existing research artifacts remain in the application repository; no claim
that research is complete or published was added. The documented application workflow and
19-test verification are retained, alongside relevant input and evidence-review limitations.
Build, Astro diagnostics and both asset audits passed. No DecisionLens app hosting is enabled.
