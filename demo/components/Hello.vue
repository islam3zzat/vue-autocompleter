<template>
  <div class="hello">
    <Autocomplete
      :source="options"
      :limit="3"
      v-model="msg">
      <template  scope="{option, index}">
        <div class="option">
          <strong>{{index}}</strong>
          <span>{{option}}</span>
        </div>
      </template>
    </Autocomplete>
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>

    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      options: [
        'Lorem ipsum dolor',
        'sit amet, consectetur',
        'adipisicing elit. Accusantium',
        'adipisci architecto corporis',
        'dolor dolores dolorum, ea eveniet',
        'inventore modi nemo, nihil, nostrum',
        ' nulla provident quam quis',
        ' ullam ut voluptatem voluptates?'
      ]
    }
  },
  methods: {
    path (res) {
      return res.data.items.map(i => i.full_name)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
