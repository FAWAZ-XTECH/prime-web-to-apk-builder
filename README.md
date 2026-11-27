# PRIME WEB TO APK — GitHub Actions Builder

This is a separate builder repository for the PRIME WEB TO APK website. It contains a manually triggered GitHub Actions workflow and a minimal Android WebView app template.

## Workflow
1. Create a separate GitHub repository and upload these files to its default branch.
2. Open Actions and enable workflows if GitHub asks.
3. Run **Build Web APK** using `workflow_dispatch` inputs: website URL, app name, package ID.
4. When successful, download the APK from the run's Artifacts section. Artifact retention is 7 days.

## Important limitations
- Starter workflow is a basic, unsigned debug APK build; not a release-signed APK.
- The website integration is not included yet. The website must be authorized to dispatch this workflow and read run status/artifacts.
- GitHub API authorization is required. Do not hard-code personal access tokens in frontend code or commit them.
- The Android wrapper supports basic WebView display/navigation only; some websites may not work in WebView or may refuse to load.
- User is responsible for converting sites they own or have permission to wrap.
