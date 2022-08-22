<template>
    <NavBar></NavBar>

    <div class="container text-center">
        <!-- Section for listing out all the album templates available for creating albums. -->
        <h2 class="p-3">Album Templates</h2>
        <p class="text-info">These are the templates available when you create your own album.</p>

        <!-- Dynamically rendered images using the "v-for" vue directive. Used props to pass these images from main App file to this child component, including binding the source, alt, and title attributes from the image objects. -->
        <div class="text-center">
            <img v-for="(image, i) in templates" :key="i" :src="require(`~/assets/${image}.png`)" alt="Album template" title="Album template" class="img-fluid p-3" width="250" height="250">
        </div>
    </div>

</template>



<script>

    export default {
        data() {
            return {
                templateImages: [
                    'template-blank',
                    'template1',
                    'template2',
                    'template3',
                    'template4',
                    'template5'
                ]
            }
        }
    }
</script>