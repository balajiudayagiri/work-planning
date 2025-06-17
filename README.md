# Project Documentation

This project is designed to automatically sync the contents of the `docs/` folder with the GitHub Wiki of the repository. The syncing process is managed through a GitHub Actions workflow defined in the `.github/workflows/sync-to-wiki.yml` file.

## Overview

- The `docs/` folder contains markdown files that serve as documentation for the project.
- The GitHub Actions workflow triggers on pushes to the `main` branch, ensuring that any updates to the documentation are reflected in the Wiki.

## Setup Instructions

1. **Personal Access Token (PAT)**: 
   - Generate a Personal Access Token with `repo`, `workflow`, and `read/write` access from your GitHub account settings.
   - Add the token as a secret in your repository settings under `Secrets` with the name `GH_PAT`.

2. **Workflow Configuration**:
   - The workflow file `.github/workflows/sync-to-wiki.yml` is already set up to handle the syncing process. It will:
     - Clone the Wiki repository.
     - Copy the contents of the `docs/` folder into the Wiki.
     - Commit and push the changes back to the Wiki.

## Example Documentation

The `docs/example.md` file contains sample markdown content that will be synced to the Wiki. This serves as a template for the type of documentation you can maintain.

## Notes

- The first run of the workflow may create a blank Wiki if it does not exist yet.
- All markdown files in the `docs/` folder will become separate pages in the Wiki.
- You can use markdown links within the documentation, and they will function correctly in the Wiki.

For any further customization or questions regarding the setup, feel free to reach out!