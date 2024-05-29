<script>
export default {

    props: {
         carte: Array 
        },

    data() {return {}},

    methods: {
        
    },

    mounted() {

     },
}
</script>

<template>

    <button>Alien</button>

    <div class="container-fluid">
        <div class="row">
            <div class="col-10 bg-info">
                <ul class="st_image d-flex flex-wrap">
                    <li v-for="element in carte">
                        <img :src="element.card_images[0].image_url" alt="">
                        <span>{{}}</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>

</template>

<style>
.st_image img {
    height: 20rem;
}
</style>
