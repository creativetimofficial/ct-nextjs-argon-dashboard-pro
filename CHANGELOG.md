## [1.1.0] 2021-02-04
### Bug fixing
- Changed all class components to functional ones (the `pages/_app.js` and `pages/_document.js` were kept as class components, read more here: https://nextjs.org/docs/advanced-features/custom-document)
- https://github.com/creativetimofficial/ct-nextjs-argon-dashboard-pro/issues/1 (it also solves the serverless issues as well)
  - please check inside `pages/admin/sortable.js` and `pages/admin/components.js` to see the solution
### Major style changes
- Delete the `src/assets/scss/bootstrap` folder and changed all the bootstrap imports from `src/assets/scss` files to ones from `node_modules`
### Deleted components
### Added components
- `components/TagsInput/TagsInput.js` (it is actually react-tagsinput, but it uses new React API)
### Deleted dependencies
- @types/react
- @types/markerclustererplus
- @types/googlemaps
- react-google-maps (We've replace this plugin with Google Maps API Vanilla JS)
- react-tagsinput (we've copied the code from this plugin, and updated it to latest React version)
### Added dependencies
+ sweetalert2@10.13.0 (so that we can import the styles from node_modules, not a downloaded version)
+ select2@4.0.13 (so that we can import the styles from node_modules, not a downloaded version)
+ @fortawesome/fontawesome-free@5.15.2 (so that we can import the styles from node_modules, not a downloaded version)
+ quill@1.3.7 (so that we can import the styles from node_modules, not a downloaded version)
+ bootstrap@4.6.0 (and deleted the downloaded version of Bootstrap)
+ node-sass-package-importer@5.3.2 (so we can import bootstrap from node_modules)
### Updated dependencies
```
@fullcalendar/core            5.3.0   →    5.5.1
@fullcalendar/daygrid         5.3.0   →    5.5.0
@fullcalendar/interaction     5.3.0   →    5.5.0
chart.js                      2.9.3   →    2.9.4
list.js                       1.5.0   →    2.3.1
moment                       2.27.0   →   2.29.1
next                          9.5.2   →   10.0.6
next-compose-plugins          2.2.0   →    2.2.1
next-transpile-modules        4.1.0   →    6.1.0
nouislider                   14.6.1   →   14.6.3
react                       16.13.1   →   17.0.1
react-chartjs-2              2.10.0   →   2.11.1
react-copy-to-clipboard       5.0.2   →    5.0.3
react-datetime               2.16.3   →    3.0.4
react-dom                   16.13.1   →   17.0.1
react-notification-alert     0.0.12   →   0.0.13
react-to-print                2.9.0   →   2.12.2
reactstrap                    8.5.1   →    8.9.0
webpack                      4.44.1   →    4.46.0
```
### Warning
_The following warnings will appear when running the installation command, but they do not affect the UI or the functionality of the product (they will be solved in our next update):_
```
npm WARN react-bootstrap-table2-paginator@2.1.2 requires a peer of react@^16.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-bootstrap-table2-paginator@2.1.2 requires a peer of react-dom@^16.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-bootstrap-table2-toolkit@2.1.3 requires a peer of react@^16.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-bootstrap-table2-toolkit@2.1.3 requires a peer of react-dom@^16.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-bootstrap-table-next@4.0.3 requires a peer of react@^16.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-bootstrap-table-next@4.0.3 requires a peer of react-dom@^16.3.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-datetime@3.0.4 requires a peer of react@^16.5.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-quill@1.3.5 requires a peer of react@^0.14.9 || ^15.3.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-select2-wrapper@1.0.4-beta6 requires a peer of react@^0.14.0 || ^15.0.0-rc || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-select2-wrapper@1.0.4-beta6 requires a peer of react-dom@^0.14.0 || ^15.0.0-rc || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-popper@1.3.7 requires a peer of react@0.14.x || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN create-react-context@0.3.0 requires a peer of react@^0.14.0 || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
```
_If they will persist in our 2.*.* version, we will drop their usages and replace them with other plugins._
_In development mode, some of the above plugins will throw a warning because they still use React v16 syntax. If the error will persist in our 2.*.* version, we will drop their usage and replace them with other plugins._

## [1.0.0] 2020-09-14
### Original Release
- Started project with NextJS
- Added design from Argon Dashboard PRO React by Creative Tim
### Warning
_Warnings might appear while doing an npm install - they do not affect the UI or the functionality of the product, and they appear because of NodeJS and not from the product itself._
_While in development some of the plugins that were used for this product will throw some warnings - note, this only happens in development, the UI or the functionality of the product is not affected, also, if the issues will persist in React 17, we'll drop usage of those plugins, and replace them with other ones._
