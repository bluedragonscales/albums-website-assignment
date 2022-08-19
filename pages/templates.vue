<template>
    <NavBar></NavBar>

    <div class="container text-center">
        <!-- Section for listing out all the album templates available for creating albums. -->
        <h2 class="p-3">Album Templates</h2>
        <p class="text-info">These are the templates available when you create your own album.</p>

        <!-- Dynamically rendered images using the "v-for" vue directive. Used props to pass these images from main App file to this child component, including binding the source, alt, and title attributes from the image objects. -->
        <div class="text-center">
            <img v-for="item in templates" v-bind:key="item" :src="require('../assets' + item.source + '.png')" :alt="item.alt" :title="item.title" class="img-fluid p-3" width="250" height="250">
        </div>
    </div>

</template>



<script>

    export default {
        data() {
            return {
                
            }
        },
        // Injecting items from the main App file to this child component via props.
        props: {
            templates: Array
        },
        // Used a mixin to add a border to any image that is clicked on.
        // mixins: [borderMixin]
    }
</script>



<style scoped>

    .border-for-image {
        border: 3px solid #67D9F7;
    }

</style>