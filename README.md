# markdown-B
Some good markdown parser libraries.

## marked
installs using npm. 
after importing provides a function witch returns html data by getting markdown inputs.

like: 
```r
import marked from "marked";

const parsed = marked("# hello joseph");

<template>
  <div v-html="parsed"></div>
</template>

```

### you could import the marked library in main.js and make a mixin, like: 
```r
import marked from "marked";

const markedMixin = () => {
  methods: {
    parse: function (input) {
      return marked(input);
    }
  }
}

... .mixin(markedMixin).mount("#app");
```



## vue-markdown
you could use by adding a script to the code or just install it by npm.
if you install it by npm: 

### you should add it as a component to you file, like: 

```r
<template>
  <vue-markdown>hello world</vue-markedown>
</template>

<script>
  import VueMarkdown from "vue-markdown";

  new Vue({
    components: {
      VueMarkdown
    }
  });

</script>
```


## markdown-it-vue
install it using npm.
I don't personaly recomend that but here is some code: 

```r
<template>
  <div>
    <markdown-it-vue class="md-body" :content="content" />
  </div>
</template>

<script>
import MarkdownItVue from 'markdown-it-vue'
import 'markdown-it-vue/dist/markdown-it-vue.css'
export default {
  components: {
    MarkdownItVue
  },
  data() {
    return {
      content: '# your markdown content'
    }
  }
}
</script>
```


### There are some more libraries, and I just metion them: 

1. v-markdown-editor
2. markdown-to-vue-loader
3. Vue-SimpleMDE
4. mavonEditor

and some more unknown 

but I recomend the first one.
