# Lighthouse plugin recipe

## Contents
- `package.json` - declares the plugin's entry point (`plugin.js`)
- `plugin.js` - instructs Lighthouse to run the plugin's own `preload-as.js` audit; describes the new category and its details for the report
- `audits/preload-as.js` - the new audit to run in addition to Lighthouse's default audits

## To run

You can use this folder as your template. Download and extract this folder to an empty folder.

```sh
curl -L https://github.com/GoogleChrome/lighthouse/archive/master.zip | tar -xzv
mv lighthouse-master/docs/recipes/lighthouse-plugin-example/* ./
rm -rf lighthouse-master

yarn
yarn lighthouse https://example.com --plugins=.
```

## Result

![Screenshot of report with plugin results](./plugin-recipe-screenshot.png)
