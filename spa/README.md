# Single Page Application

> Intro to Vue.js


## Scaffold Project

    $ npm install -g vue-cli
    
    $ vue-cli init webpack <project-name>
    
    # ... answer questions
    # ... select vue-router
    # ... say yes to ESlint

    $ cd <project-name>

## Build Setup

``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:8080
$ npm run dev

# build for production with minification
$ npm run build

# build for production and view the bundle analyzer report
$ npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Install Extra Modules

    $ npm install --save vue-resource vuex
    
    $ npm install --save bootstrap-sass jquery node-sass sass-loader

## Activate Router 

in _src/main.js_

    import router from './router'
    
    new Vue({
      el: '#app',
      router,  // <------ insert here
      template: '<App/>',
      components: { App }
    })

## Create routes

in _src/router/index.js_

    import Activities from '@/components/Activities'

    // extend routes: [ ] array with
    {
      path: '/activities',
      name: 'Activities',
      component: Activities
    }

## Activate Bootstrap

in _src/main.js_

    require('../node_modules/bootstrap-sass/assets/stylesheets/_bootstrap.scss')

in _src/App.vue_

    var $ = require('jquery')
    window.$ = window.jQuery = $
    require('bootstrap-sass')

## Activate Vue-Resource

in _src/App.vue_

    import VueResource from 'vue-resource'
    
    Vue.use(VueResource)
    Vue.http.options.root = 'http://localhost:8080/'
