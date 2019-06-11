<template>
  <div>
    <app-header></app-header>
    <router-view></router-view>
    <app-footer></app-footer>
  </div>
</template>

<script>
import addBlog from './components/addBlog.vue';
import showBlogs from './components/showBlogs.vue';
import header from './components/header.vue';
import footer from './components/footer.vue';

export default {

  components: {
      'add-blog': addBlog,
      'show-blogs': showBlogs,
      'app-header': header,
      'app-footer': footer
    },
  data () {
    
    return {
    
    }
  }
}
</script>

<style scoped>

</style>
