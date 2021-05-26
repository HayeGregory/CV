npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! cv@1.0.0 sass: `node-sass -w scss -o css`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the cv@1.0.0 sass script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR! C:\Users\Kyutah\AppData\Roaming\npm-cache_logs\2021-05-26T18_27_21_485Z-debug.log

# ------------------------------------------------------------------

1. npm cache clean --force
2. delete folder : node_modules
3. file package.json => add this : "postinstall": "patch-package" in scripts
4. npm i
5. not step 3 : npm i patch-package
6. change command in package.json :
   "sass": "node-sass -w scss -o css"
   to
   "sass": "sass --watch scss:css"
