# Components-InDepth
HTML:
<div id="app"> 
  <button @click="goto('home')">Home</button> 
  <button @click="goto('news')">News</button> 
  <button @click="goto('about')">About</button>
  <hr>
  <component :is="currentView"></component>
</div>

<script src="https://unpkg.com/vue/dist/vue.js"></script>

JavaScript/Vue:
Vue.component('home', {
  template: '<div>Home</div>'
});

Vue.component('news', {
  template: '<div>News</div>'
});

Vue.component('about', {
  template: '<div>About</div>'
});

new Vue({
  el: '#app',
  
  data: {
    currentView: 'home'
  },
  
  methods: {
    goto: function (view) {
      this.currentView = view
    }
  }
});
