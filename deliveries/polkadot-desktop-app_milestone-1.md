# Milestone Delivery :mailbox:

> Only the GitHub account, which is responsible for the pull request of the accepted application is allowed to submit milestones. Don't remove any of the mandatory parts presented in bold letters or as headlines!

**The [invoice form :pencil:](https://forms.gle/8Wx7nxtq8fKrsuEz8) has been filled out correctly for this milestone.**  

* **PR Link:** [Polkadot.{js} Desktop App](https://github.com/w3f/Open-Grants-Program/pull/17)
* **Milestone Number:** 1

Please provide a list of all deliverables of the milestone extracted from the initial application and a link to the deliverable itself. Ideally all links inside the below table should include a commit hash, which should be used for testing.

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 1. | Polkadot.{js} web application as an Electron app | The Electron app package is defined in [packages/apps-electron](https://github.com/polkadot-js/apps/tree/master/packages/apps-electron)| Relevant PRs: [#2765](https://github.com/polkadot-js/apps/pull/2765) [#2819](https://github.com/polkadot-js/apps/pull/2819) [#3158](https://github.com/polkadot-js/apps/pull/3158) [#3159](https://github.com/polkadot-js/apps/pull/3159) [#2923](https://github.com/polkadot-js/apps/pull/2923) [#2795](https://github.com/polkadot-js/apps/pull/2795) [#2817](https://github.com/polkadot-js/apps/pull/2817) [#3212](https://github.com/polkadot-js/apps/pull/3212) [#2821](https://github.com/polkadot-js/apps/pull/2821) | 
| 2. | Redesigned account storage | [Shared API](https://github.com/polkadot-js/apps/blob/master/packages/apps-electron/src/api/account-store-api.ts), [Electron main process implementation](https://github.com/polkadot-js/apps/tree/master/packages/apps-electron/src/main), [Electron renderer process implementation](https://github.com/polkadot-js/apps/tree/master/packages/apps-electron/src/renderer) | In the main Electron process, we use the [FileStore](https://github.com/polkadot-js/ui/blob/master/packages/ui-keyring/src/stores/File.ts) from `polkadot-ui` and expose it via ContextBridget to the renderer process. Relevant PRs: [#2880](https://github.com/polkadot-js/apps/pull/2880) [#2883](https://github.com/polkadot-js/apps/pull/2883) [#3160](https://github.com/polkadot-js/apps/pull/3160) | 
| 3. | Continuous Integration environment | Scripts to build electron app are in [package.json](https://github.com/polkadot-js/apps/blob/master/package.json). The github actions [PR workflow](https://github.com/polkadot-js/apps/blob/master/.github/workflows/pr-any.yml) has now the step of `build:electron`. Tests for electron store ([main](https://github.com/polkadot-js/apps/blob/master/packages/apps-electron/src/main/account-store.spec.ts), [renderer](https://github.com/polkadot-js/apps/blob/master/packages/apps-electron/src/renderer/remote-electron-store.spec.ts)) are also executed as part of the build. | Relevant PRs: [#2765](https://github.com/polkadot-js/apps/pull/2765), [#3118](https://github.com/polkadot-js/apps/pull/3118 |
| 4. | Continuous Delivery to automate packaging for Mac, Windows and Linux | Release scripts in [package.json](https://github.com/polkadot-js/apps/blob/master/package.json). Workflow in [push-master.yml](https://github.com/polkadot-js/apps/blob/master/.github/workflows/push-master.yml) | Relevant PRs: [#2780](https://github.com/polkadot-js/apps/pull/2780), [#2816](https://github.com/polkadot-js/apps/pull/2816) [#3108](https://github.com/polkadot-js/apps/pull/3108) [#3138](https://github.com/polkadot-js/apps/pull/3138) [#2794](https://github.com/polkadot-js/apps/pull/2794) [#3043](https://github.com/polkadot-js/apps/pull/3043) [#2825](https://github.com/polkadot-js/apps/pull/2825) [#3040](https://github.com/polkadot-js/apps/pull/3040)
| 5. | Documentation | Updated [Readme](https://github.com/polkadot-js/apps/blob/master/README.md) | In this milestone we update the main readme do describe the `apps-electron` package |