# campaignion_vue_project

Template for Vue apps in Campaignion.
Replace `messages_app` with your app’s name.

Webpack compiles js and css into the respective module subdirectories:
```
campaignion_my_module
 │
 ├── my_vue_app (= root of this template)
 │    ├── build
 │    ├── config
 │    ├── src
 │    ...
 │    └── package.json
 │
 ├── js (drupal_add_js from here)
 │    ├── my_vue_app
 │    │    ├── app.min.js
 │    │    └── app.js.map
 │    └── some_behavior.js
 │
 ├── css (drupal_add_css from here)
 │    ├── my_vue_app
 │    │    └── app.css
 │    └── my_module_styles.js
 │
 ├── campaignion_my_module.info
 └── campaignion_my_module.module
```

Don’t forget to add campaignion_vue:
```
drupal_add_js(
  drupal_get_path('module', 'campaignion_vue') . '/js/campaignion_vue.min.js',
  {'scope' => 'footer', 'preprocess' => FALSE}
);
drupal_add_js(
  drupal_get_path('module', 'campaignion_my_module') . '/js/my_vue_app/app.min.js',
  {'scope' => 'footer', 'preprocess' => FALSE}
);
```


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
