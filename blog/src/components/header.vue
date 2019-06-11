<template>
    <nav class="cyan lighten-1">
        <div id="header-nav" class="container">
            <ul class="row">
            <div class="col s4">
                <li class="right"><router-link to="/" exact >Blog</router-link></li>
            </div>
            <div class="col s4">
                <li class="right"><router-link to="/add" exact>Add</router-link></li>
            </div>
            <div class="col s4">
                <li class="right"><router-link to="/about" exact>About</router-link></li>
            </div>
            </ul>
        </div>
    </nav>
</template>

<script>

export default {

    components: {
    
    },
    data () {
        return {
            
        }
    },
    methods: {
        
    }
}
</script>

<style scoped>
ul {
    list-style-type: none;
    text-align: center;
    margin: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #fff;
    text-decoration: none;
    padding-left: 2em;
    padding-right: 2em;
    font-size: 1.3em;
    font-weight: bold;
}

nav {
    padding: 14px 0;
    padding-bottom: 5em  ;
    margin-bottom: 4em;
    text-align: center;
}

.router-link-active{
    color: #444;
}

</style>
