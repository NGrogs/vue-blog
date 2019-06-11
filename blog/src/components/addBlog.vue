<template>
    <div id="add-blog">
        <h2> What's on your mind?</h2>
        <form v-if="!submitted">
            <label>Blog Title</label>
            <input type="text" v-model="blog.title" required>
            
            <label>Blog Content</label>
            <div class="input-field col s12">
            <textarea class="materialize-textarea"v-model="blog.content"></textarea>
            </div>

            <button class="btn-large cyan lighten-1" v-on:click.prevent="post">Post Blog </button>
        </form>

        <div v-if="submitted">
            <h3>Post submitted</h3>
        </div>

        <div id="preview">
            <h3>Blog Preview</h3>
            <p>Title: {{ blog.title }} </p>
            <p>Content:</p>
            <p> {{ blog.content }} </p>
        </div>
    </div>
</template>

<script>
export default {

    data () {
        return {
            blog: {
                title: "",
                content: ""
            },
            submitted: false
        }
    },
    methods: {
        post: function(){
            this.$http.post('https://blog-ab26a.firebaseio.com/posts.json', this.blog).then(function(data){
                this.submitted = true;
            });
        }
    },
}
</script>

<style scoped>
#add-blog {
    margin: 20px auto;
    max-width: 50%;
    margin-bottom: 10em;
}

label {
    display: block;
    margin: 20px 0 10px;
}

#preview {
    border: 1px dotted #ccc;
    margin: 30px 0;
    padding: 10px 20px;
}

h3 {
    margin-top: 10px;
}

h2 {
    margin-bottom: 1em; 
}

</style>
