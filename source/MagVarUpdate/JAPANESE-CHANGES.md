# Japanese runtime build

Upstream MagicalAstrogy/MagVarUpdate v0.188.0, commit 183d8ade3b9a3369e824a55cb13b4ddf91aada50. Japanese locale, six help pages and six button event names are localized. The card-specific build presents Japanese; source Chinese/English dictionaries remain in source for comparison. API protocols, event sequencing and rendering triggers are retained.

The StageDog adapter source and its AFPL license are in vendor-source/tavern_resource, with its upstream commit recorded there. Only its visible messages and the local import path are translated.

Build: npm ci --legacy-peer-deps --ignore-scripts; CI=true npm run build; CI=true node node_modules/webpack-cli/bin/cli.js --config build-zod.config.ts --mode production. After building, rewrite module imports using the upstream/path ledger in ../../DEPENDENCIES.json. Source-map hints are omitted from delivered modules.
