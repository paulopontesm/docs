# Self-hosted v1.5.0 for Kubernetes

These release notes are for [Codacy Self-hosted v1.5.0](https://github.com/codacy/chart/releases/tag/1.5.0) for Kubernetes. [Follow these instructions](https://docs.codacy.com/chart/maintenance/upgrade/) to upgrade Codacy.

## Product enhancements

-    Added support for Gosec, the Golang Security Checker, as a [client-side tool](../../related-tools/client-side-tools.md)
-    It's now possible to add repositories to Codacy programmatically with the new API v3 endpoint [addRepository](https://app.codacy.com/api/api-docs#addrepository) (CY-1877)
-    Streamlined the configuration of Git providers and improved the onboarding flow that guides the user while performing the initial Codacy setup. (CY-468)
-    Added support for GitLab Enterprise synced organizations (CY-68)

## Bug fixes

-    Codacy no longer displays a banner asking to add the user to the list of authors for commits with no associated email address (CY-2020)
-    Fixed an issue that prevented Codacy from automatically removing GitHub organizations with the GitHub Marketplace plan when they were deleted on the Git provider (CY-1989)
-    Fixed an issue that allowed users with access to a repository on the Git provider but who did not belong to the organization on Codacy to change settings for that repository on the Codacy UI (CY-1985)
-    Added missing redirect from the login page to the repositories list page when the user is already logged in. (CY-1946)
-    Fixed an issue that could cause the list of repositories in an organization to display the repositories in the incorrect order. (CY-1940)
-    Fixed an issue that could prevent pull requests from being analyzed if they were created while Codacy was already performing an analysis. (CY-1902)
-    Fixed an issue that prevented Codacy from reporting the Complexity metric on TypeScript repositories (CY-1824)
-    Fixed an issue related to the expiration of the session cookie that caused the Codacy API to return 401 Unauthorized errors when the user was correctly logged in (CY-1815)