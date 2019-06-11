<template>
    <div id="show-blogs">
        <h1>All Blogs</h1>

        <input type="text" v-model="search" placeholder="search blogs"/>

        <div v-for="blog in filteredBlogs" class="single-blog">
            <h2>{{blog.title}}</h2>
            <article>{{blog.content}}</article>
            <router-link  v-bind:to="'blog/' + blog.id">
                <button class="btn-large cyan lighten-1"> See Post </button>
            </router-link>
        </div>
    </div>
</template>

<script>

export default {

    components: {
    
    },
    data () {
        return {
            blogs: [],
            search: ''
        }
    },
    methods: {
        
    },
    created() {
        this.$http.get('https://blog-ab26a.firebaseio.com/posts.json').then(function(data){
            return data.json();
        }).then(function(data){
            var blogsArray = [];
            for(let key in data){
                data[key].id = key;
                blogsArray.push(data[key]);
            }
            this.blogs = blogsArray;
        })
    },
    computed: {
        filteredBlogs: function(){
            return this.blogs.filter((blog) => {
                return blog.title.match(this.search);
            })
        }
    },
}
</script>

<style scoped>
#show-blogs {
    max-width: 50%;
    margin: 0 auto;
    margin-bottom: 10em;
}

.single-blog {
    padding: 20px;
    margin: 20px;
    box-sizing: border-box;
    background: #eee;
}

button {
    margin-top: 2em;
}
</style>
