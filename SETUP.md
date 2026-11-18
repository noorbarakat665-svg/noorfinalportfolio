# Noor portfolio v3 — editing-ready files

This package preserves Version 2 and separates many text fields and all five existing images into `content/site.json`. The public website loads that JSON on hosting. The original HTML provides fallback content when opened locally.

## Upload to GitHub
1. Open https://github.com/noorbarakat665-svg/noor-portofolio
2. Choose Add file > Upload files. Upload the CONTENTS of this folder, not the ZIP itself. Preserve `admin/`, `content/`, `assets/`, and `index.html` paths.
3. Commit changes to main. The repo may remain private.

## Deploy to Netlify
1. Sign in at https://app.netlify.com/ and choose Add new project > Import an existing project > GitHub.
2. Authorize access to the private repository and select `noor-portofolio`.
3. No build command is needed; publish directory is `.` (repository root).
4. BEFORE sharing the Netlify URL, set site access controls. A private GitHub repo does NOT hide the deployed site. Netlify access restrictions depend on your plan and available settings. If password protection is not included, do not deploy sensitive material or assume it is private.

## Enable /admin editor (separate authentication step)
Decap CMS with the GitHub backend REQUIRES an OAuth authentication service. GitHub login does NOT work just by uploading these files. Set up a compatible OAuth provider (for example a self-hosted or third-party GitHub OAuth bridge), then add its `base_url` and, if needed, `auth_endpoint` to `admin/config.yml`. The OAuth provider may require its own hosting and secrets. Never place GitHub OAuth client secrets in this public repository.

The current config is a starter configuration, not a working authenticated dashboard. Do not enter credentials until an OAuth provider is configured and trusted. The JSON can also be edited directly through GitHub's web editor meanwhile, but that is not visual editing.

## Drafts
This starter config does NOT enable Decap editorial workflow, because its GitHub branch/PR behavior and deployment previews must be configured and tested first. Any edits committed to main on a connected Netlify deployment can go live automatically.

## Content limitations
The editor exposes most simple text fields and existing images, but not every link, complex rich-text paragraph, or the ability to add/remove article cards. These need a later structured-content update.

## Contact form
The inquiry form opens an email draft in the visitor's email application; it does not submit messages to a server.
