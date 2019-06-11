<template>
    <div id="about">
        <div>
            <img src="../assets/Dee.jpg"  class="responsive-img"/>
        </div>
        <div>
            <h2>Denise Quirke</h2>
            <p>
                Student nurse @ TCD
            </p>
        </div>
        <div class="row" id="media" >
            <div class="col s6">
            <a href="https://www.facebook.com/quirkey14" class="btn-large cyan lighten-1"><i class="fab fa-facebook"></i> <span class="network-name">Facebook</span></a>
            </div>
            <div class="col s6 ">
                <a href="https://www.instagram.com/quirke.denise/" class="btn-large cyan lighten-1"><i class="fab fa-instagram"></i> <span class="network-name">Instagram</span></a>
            </div>
        </div>
    </div>
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
#about {
    margin: 20px auto;
    max-width: 50%;
    margin-bottom: 10em;
    text-align: center;
}

img {
    height: 25em;
    border: black solid .1em;
    border-radius: 3em;
}

#media {
    padding-top: 4em;
}
</style>
