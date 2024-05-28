<script>
export default {

    props: { carte: Array },

    data() {return {}},

    methods: { },

    mounted() { },
}
</script>

<template>

    <button>Alien</button>

    <div class="container-fluid">
        <div class="row">
            <div class="col-10 bg-info">
                <ul>
                    <li v-for="element in carte">
                        <img :src="element.card_images[0].image_url" alt="">
                        <span>{{ element. }}</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>

</template>

<style></style>
