## loading 加载器

### 使用方法
```html
<code>
<template>
  <loading v-show="loading"></loading>
</template>
<script>
  import Loading from '@/wm-kit/packages/loading/src/Loading.vue'

  export default {
    components: {
      Loading
    }
  }

</script>
```

### 示例
<template>
  <div class="loading-wrap">
        <div id="editor"></div>
    <loading v-show='loading' ref="loading"></loading>
    <button @click="toggleLoading">点我查看加载效果</button>
    <button @click="toggleEditor">点我编辑</button>
  </div>
</template>

<script>
import Loading from '@/wm-kit/packages/loading/src/Loading.vue'

export default {
  data() {
    return {
      loading: false,
      editor: false
    }
  },
  components: {
    Loading
  },
  methods: {
    toggleLoading() {
      this.loading = !this.loading
      setTimeout(() => {
        this.loading = !this.loading
      }, 1000)
    },
    toggleEditor() {
      this.editor = !this.editor
    }
  }
}

</script>

<style>
  .editor-wrap {
    width: 300px;
    height: 300px;
    border: 1px solid #ccc;
  }
</style>



