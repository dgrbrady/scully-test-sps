See output of terminal to see commands used to reproduce this issue
```
E:\code>ng new
? What name would you like to use for the new workspace and initial project? scully-test-sps
? Would you like to add Angular routing? Yes
? Which stylesheet format would you like to use? SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
CREATE scully-test-sps/angular.json (3261 bytes)
CREATE scully-test-sps/package.json (1078 bytes)
CREATE scully-test-sps/README.md (1059 bytes)
CREATE scully-test-sps/tsconfig.json (863 bytes)
CREATE scully-test-sps/.editorconfig (274 bytes)
CREATE scully-test-sps/.gitignore (548 bytes)
CREATE scully-test-sps/.browserslistrc (600 bytes)
CREATE scully-test-sps/karma.conf.js (1432 bytes)
CREATE scully-test-sps/tsconfig.app.json (287 bytes)
CREATE scully-test-sps/tsconfig.spec.json (333 bytes)
CREATE scully-test-sps/.vscode/extensions.json (130 bytes)
CREATE scully-test-sps/.vscode/launch.json (474 bytes)
CREATE scully-test-sps/.vscode/tasks.json (938 bytes)
CREATE scully-test-sps/src/favicon.ico (948 bytes)
CREATE scully-test-sps/src/index.html (299 bytes)
CREATE scully-test-sps/src/main.ts (372 bytes)
CREATE scully-test-sps/src/polyfills.ts (2338 bytes)
CREATE scully-test-sps/src/styles.scss (80 bytes)
CREATE scully-test-sps/src/test.ts (745 bytes)
CREATE scully-test-sps/src/assets/.gitkeep (0 bytes)
CREATE scully-test-sps/src/environments/environment.prod.ts (51 bytes)
CREATE scully-test-sps/src/environments/environment.ts (658 bytes)
CREATE scully-test-sps/src/app/app-routing.module.ts (245 bytes)
CREATE scully-test-sps/src/app/app.module.ts (393 bytes)
CREATE scully-test-sps/src/app/app.component.html (23364 bytes)
CREATE scully-test-sps/src/app/app.component.spec.ts (1100 bytes)
CREATE scully-test-sps/src/app/app.component.ts (220 bytes)
CREATE scully-test-sps/src/app/app.component.scss (0 bytes)
✔ Packages installed successfully.
    Successfully initialized git.

E:\code>cd scully-test-sps

E:\code\scully-test-sps>ng add @scullyio/init
ℹ Using package manager: npm
✔ Found compatible package version: @scullyio/init@2.1.20.
✔ Package information loaded.

The package @scullyio/init@2.1.20 will be installed and executed.
Would you like to proceed? Yes
✔ Package successfully installed.
? Which route renderer would you like to use? Scully platform server
    Installing ng-lib
    Installing Scully Platform Server plugin
UPDATE src/app/app.module.ts (466 bytes)
UPDATE src/polyfills.ts (2531 bytes)
UPDATE .gitignore (638 bytes)
UPDATE package.json (1260 bytes)
⠹ Installing packages (npm)...npm ERR! code ERESOLVE
npm ERR! ERESOLVE unable to resolve dependency tree
npm ERR!
npm ERR! While resolving: scully-test-sps@0.0.0
npm ERR! Found: @angular/animations@13.2.4
npm ERR! node_modules/@angular/animations
npm ERR!   @angular/animations@"~13.2.0" from the root project
npm ERR!
npm ERR! Could not resolve dependency:
npm ERR! peer @angular/animations@"12.2.16" from @angular/platform-server@12.2.16
npm ERR! node_modules/@angular/platform-server
npm ERR!   @angular/platform-server@"^12" from the root project
npm ERR!
npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! this command with --force, or --legacy-peer-deps
npm ERR! to accept an incorrect (and potentially broken) dependency resolution.
npm ERR!
npm ERR! See E:\nodejs\npm-cache\eresolve-report.txt for a full report.

npm ERR! A complete log of this run can be found in:
npm ERR!     E:\nodejs\npm-cache\_logs\2022-03-01T15_45_16_992Z-debug-0.log
✖ Package install failed, see above.
The Schematic workflow failed. See above.

E:\code\scully-test-sps>npm i --legacy-peer-deps
npm WARN deprecated source-map-resolve@0.6.0: See https://github.com/lydell/source-map-resolve#deprecated
npm WARN deprecated @wessberg/ts-evaluator@0.0.27: this package has been renamed to ts-evaluator. Please install ts-evaluator instead

added 1055 packages, and audited 1056 packages in 1m

97 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

=============================================== EDITOR NOTE =======================================================
node_modules and package-lock.json were deleted outside of the CLI, but were fully removed before this next command
===================================================================================================================

E:\code\scully-test-sps>npm i @scullyio/scully@next @scullyio/platform-server@next @scullyio/ng-lib@next @scullyio/init@next --legacy-peer-deps

added 39 packages, removed 15 packages, changed 17 packages, and audited 1080 packages in 26s

96 packages are looking for funding
  run `npm fund` for details

7 vulnerabilities (2 low, 5 high)

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.

E:\code\scully-test-sps>npx ng g @scullyio/init:ng-add --renderer sps
    polyfills.ts is already upto date
    Installing ng-lib
    Installing Scully Platform Server plugin
UPDATE package.json (1287 bytes)
✔ Packages installed successfully.
CREATE scully.scully-test-sps.config.ts (325 bytes)
UPDATE package.json (1361 bytes)
CREATE scully/tsconfig.json (450 bytes)
CREATE scully/plugins/plugin.ts (305 bytes)

E:\code\scully-test-sps>ng build
✔ Browser application bundle generation complete.
✔ Copying assets complete.
✔ Index html generation complete.

Initial Chunk Files           | Names         |  Raw Size | Estimated Transfer Size
main.c5c9952bf23b9efb.js      | main          | 219.34 kB |                60.02 kB
polyfills.bb25d2fe2ec9894e.js | polyfills     |  37.47 kB |                11.83 kB
runtime.c95941cd9075f261.js   | runtime       |   1.05 kB |               604 bytes
styles.ef46db3751d8e999.css   | styles        |   0 bytes |                       -

                              | Initial Total | 257.87 kB |                72.44 kB

Build at: 2022-03-01T15:51:31.169Z - Hash: 6e1c9073b53d73fa - Time: 24296ms

E:\code\scully-test-sps>npx scully
'"-S"' is not recognized as an internal or external command,
operable program or batch file.
```
