# Docs Foundry Feedback

USA / Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/) [Cloud2BR](https://github.com/Cloud2BR)

Last updated: 2026-02-25

----------

> This repository is the intake queue for Docs Foundry product feedback. It receives feature requests, workflow improvements, documentation suggestions, and roadmap input so the main product repository can stay focused on source code, releases, and implementation work.

## How feedback gets here

There are two supported intake paths:

1. Preferred: the hosted GitHub Pages form at https://cloud2br.github.io/docs-foundry/feedback.html prepopulates the request and opens a ready-to-submit issue in this repository.
2. Direct: users can open an issue in this repository through the template chooser if they want to skip the Pages form.

> [!NOTE]
> Both paths end in GitHub Issues here.

## What happens after submission

> - This repository includes a GitHub Actions intake workflow at .github/workflows/feedback-intake.yml.
> - It also includes a bootstrap workflow at .github/workflows/bootstrap-labels.yml that creates the expected feedback labels when the repository setup changes are pushed.

When a new issue is opened, the workflow:

- detects the request category from hidden Pages metadata, existing labels, title prefixes, or the issue body
- creates any missing labels that the feedback flow expects
- applies triage labels such as `needs-triage`, `kind:feature`, `kind:improve`, `kind:docs`, or `kind:roadmap`
- automatically assigns the default maintainer routing configured in the workflow
- posts an intake confirmation comment so the request has an immediate status marker

No extra repository variables or token secrets are required for the workflows in this repository. They use the built-in `GITHUB_TOKEN` that already exists in GitHub Actions runs, and feedback is routed automatically to the default maintainer configured in the workflow.
## Issue templates

This repo includes issue forms for:

- Feature requests
- Workflow improvements
- Documentation feedback
- Roadmap input

> [!NOTE]
> Blank issues are still enabled because the GitHub Pages feedback form opens prefilled issue URLs directly.

## Recommended repository settings

1. Keep Issues enabled.
2. Keep Actions enabled.
3. Leave the default workflow permissions at read repository contents. The workflow requests explicit `issues: write` permissions for label, assignee, and comment updates.
4. Test the flow from https://cloud2br.github.io/docs-foundry/feedback.html after pushing these files.

## Related links

- Product repository: https://github.com/Cloud2BR/docs-foundry
- Feedback form: https://cloud2br.github.io/docs-foundry/feedback.html
- Public roadmap: https://cloud2br.github.io/docs-foundry/roadmap.html

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-3-limegreen" alt="Total views">
  <p>Refresh Date: 2026-04-13</p>
</div>
<!-- END BADGE -->
