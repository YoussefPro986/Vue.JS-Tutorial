# Vue Tutorial
In this article ,you can learnning:

* How to install Vue.js
* ABC
    * Hello Vue
    * Vue Instance
    * Template Syntax & Data Binding
    * Computed Properties & Watchers
    * Event
    * Forms
    * Components
* Advanced
    * Custom Directives
    * Custom Filters
    * Mixins
    * Router
    * Plugins

## How to install Vue.js
* Stanalone
    * [dev version](http://vuejs.org/js/vue.js)
    * [pro version](http://vuejs.org/js/vue.min.js)
* `npm install vue`
* CLI
    * `npm install --global vue-cli`
    * `vue init webpack my-project`
    * `cd my-project`
    * `npm install`
    * `npm run dev`

## ABC
* [Hello Vue](src/hello.html)
    * import vue.js
    * index.html
    * create vue instance
* [Vue Instance](src/vue-instance.html)
    * constructor
    * properties & methods
    * instance lifecycle hooks
        * created
        * beforeMounted
        * mounted
        * updated
        * destroyed
* [Template Syntax & Data Binding](src/syntax.html)
    * text: `<span>{{ msg }}</span>`
    * raw html: `<span v-html="rawHtml"></span>`
    * attributes: `<span v-bind:title="title"></span>` shorthand `<span :id="title"></span>`
    * expressions: `{{ number + 1 }}` *only contain one single expression*
    * filters: `{{ message | capitalize }}`
    * directives: `<span v-if="seen">Now you see me</span>`
    * modifiers: `<a v-on:click.stop="doThis">stop modifiers</a>`
    * class binding: `<span v-bind:class="{active:isActive}">class</span>`
    * style binding: 
    * conditional rendering: `v-if`, `v-else`, `v-show`
    * list rendering: `v-for`
* Computed Properties & Watchers
* [Event](src/event.html)
    * listening
    * method event handlers
    * event modifiers
        * .stop
        * .prevent
        * .capture
        * .self
    * key modifiers
        * `<input v-on:keyup.enter="submit">`
        * .enter
        * .tab
        * .delete
        * .esc
        * .space
        * .up
        * .down
        * .left
        * .right
        * `Vue.config.keyCodes.f1 = 112`
* [Forms](src/forms.html)
    * text
    * checkbox
    * radio
    * select
    * value bindings
    * modifiers
* [Components](src/components.html)
    * global
        * register: `Vue.component('custom-component',{})`
        * `<custom-component></custom-component>`
    * local
        * declare: `var child = { template: ''}`
        * register: `components: { 'child-component': child }`
        * `<child-component></child-component>`
    * props
        * `components: { props: ['message'] }`
        * `<custom-component message="hello"></custom-component>`
        * `<custom-component :message="msg"></custom-component>`
    * data must be a Function
    * methods are same as Vue instance
    * parent-child communication
    * dynamic component
        * `<component v-bind:is="currentView"></component>`
    * async component
        * use webpack's code-splitting

## Advanced
* [Custom Directives](src/directive.html)
    * register: `Vue.directive('custom-directive')`
    * `v-custom-directive`
    * hook functions
        * bind
        * inserted
        * undate
        * componentUpdated
        * unbind
* Custom Filters
    * Register: `Vue.filter('customFilters')`
    * `{{ data | customFilters }}`
* Mixins
* Router
    * how to use:
        * create `<router-view></router-view>` template
        * create child components
        * declare routes
        * create VueRouter instance
        * insert router to Vue instance
    * dynamic matching
    * navigation
        * router.push('');
        * router.push({ path: '', query: { key: 'value'}})
        * router.go(1)
    * redirect & alias
    * h5 history mode
    * navigation hook
        * global
            * beforeEach
            * afterEach
        * router
            * beforeEnter
            * afterEach
        * component
            * beforeRouteEnter
            * beforeRouteLeave
    * fetch data
    * lazy loading
        
* Plugins
    * vue-router
    * vue-resource
    * vue-async-data
    * vue-validator
    * vue-animated-list
