To reproduce the issue:

```
yarn install
yarn build-storybook
yarn visual # runs percy storybook --dry-run --debug ./storybook-static
```

Output:

```
$ ~/taskbox/node_modules/.bin/percy storybook --dry-run --debug ./storybook-static
[percy:config] Config file not found (0ms)
[percy:storybook] Requesting Storybook: http://localhost:63064 (58ms)
[percy:core] Percy has started! (18ms)
[percy:core:browser] Launching browser (0ms)
[percy:core:browser] Browser connected [84613]: HeadlessChrome/96.0.4664.0 (239ms)
[percy:core:page] Page created (7ms)
[percy:core:page] Page created (2ms)
[percy:core:page] Navigate to: http://localhost:63064/?path=/settings/about (533ms)
[percy:core:page] Navigate to: http://localhost:63064/iframe.html (1ms)
[percy:core:page] Page navigated (32ms)
[percy:core:page] Page navigated (82ms)
[percy:core:page] Page closed (80ms)
[percy:core:queue] Clearing discovery queue, queued state: 0, pending state: 0 (1ms)
[percy:core:queue] Clearing snapshot queue, queued state: 0, pending state: 0 (0ms)
[percy:core] Stopping percy... (0ms)
[percy:core:queue] Clearing discovery queue, queued state: 0, pending state: 0 (1ms)
[percy:core:browser] Closing browser (0ms)
[percy:core:browser] Browser closed (38ms)
[percy:core:queue] Clearing snapshot queue, queued state: 0, pending state: 0 (0ms)
[percy:core] Build not created (0ms)
[percy:cli] Error: Storybook object not found on the window. Open Storybook and check the console for errors.
    at withPage (file://~/taskbox/node_modules/@percy/storybook/dist/utils.js:129:47)
    at async yieldTo (file://~/taskbox/node_modules/@percy/core/dist/utils.js:194:36)
    at async Promise.all (index 1)
    at async yieldAll (file://~/taskbox/node_modules/@percy/core/dist/utils.js:213:11)
    at async takeStorybookSnapshots (file://~/taskbox/node_modules/@percy/storybook/dist/snapshots.js:174:38)
    at async Object.callback (file://~/taskbox/node_modules/@percy/storybook/dist/storybook.js:36:3)
    at async generatePromise (file://~/taskbox/node_modules/@percy/core/dist/utils.js:158:115)
    at async runCommandWithContext (file://~/taskbox/node_modules/@percy/cli-command/dist/command.js:132:3)
    at async percy (file://~/taskbox/node_modules/@percy/cli-command/dist/command.js:162:9)
    at async ~/taskbox/node_modules/@percy/cli/bin/run.cjs:14:5 (1ms)
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```
