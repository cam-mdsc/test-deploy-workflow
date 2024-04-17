# Deploy workflow

The branch `main` (or `master`) is the integration branch. All feature branches are merged into this branch. This is the level at which developers make changes to the code.

## Deployments

Branches under `deploy/` are deployment branches. Te perform a deployment to a certain environment, a pull request is made from `main` to the appropriate environment's branch (e.g. `deploy/prod`). The title of the pull request is **Deployment (...)** where the **...** is a very short title of the changes made in the deployment (optional). The body contains several sections where each update is included. Sections that are empty should be removed. These sections are
- **Added** - Updates that add new functionality
- **Changed** - Updates that change existing functionality or refactor current code
- **Deprecated** - Sections of code that are deprecated (common modules). This section will likely be used very sparingly
- **Removed** - Updates that remove functionality
- **Fixed** - Updates that fix existing functionality
- **Security** - Updates that resolve security issues

Breaking changes should be avoided. If a breaking change must be made, then notes of that breaking change, impacts, and special deployment instructions must be included in the pull request.
