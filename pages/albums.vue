<template>
    <NavBar></NavBar>

    <div class="container text-center">
        <!-- Bootstrap Grid section. -->
        <h2 class="p-3">Create Your Albums</h2>

        <!-- These are the little color boxes at the top to choose a background color. Click on them to activate the method "changeColor"-->
        <div class="container text-start">
            <div class="row">
                <div class="col">
                    <p>Choose your background color:</p>
                </div>
                <div class="col">
                    <div class="color-box" @click="changeColor('#fff')"></div>
                </div>
                <div class="col">
                    <div class="color-box bg-primary" @click="changeColor('#0D6EFD')"></div>
                </div>
                <div class="col">
                    <div class="color-box bg-info" @click="changeColor('#0DCAF0')"></div>
                </div>
                <div class="col">
                    <div class="color-box bg-dark" @click="changeColor('#000')"></div>
                </div>
                <div class="col">
                    <div class="color-box bg-warning" @click="changeColor('#FFC107')"></div>
                </div>
            </div>
        </div>


        <!-- Main canvas for creating the album. -->
        <div class="main-canvas text-center m-3" id="canvas" style="height: 100vh; width: auto; border: 5px solid black;"></div>


        <!-- Buttons for adding pages, deleting pages, and publishing your album. -->
        <div class="text-center p-3">
            <button type="button" name="button" class="btn btn-outline-info m-2" data-bs-toggle="tooltip" data-bs-placement="top" data-bs-custom-class="custom-tooltip" title="Click here to add a new page to your album.">Add Page</button>
            <button type="button" name="button" class="btn btn-outline-info m-2" data-bs-toggle="tooltip" data-bs-placement="top" data-bs-custom-class="custom-tooltip" title="Click here to delete the current page of your album.">Delete Page</button>
            <button type="button" name="button" class="btn btn-outline-info m-2" data-bs-toggle="tooltip" data-bs-placement="top" data-bs-custom-class="custom-tooltip" title="Click here to publish your album so you can start sharing it with friends and family.">Publish Album</button>
        </div>
    </div>

</template>



<script>

    export default {
        data() {
            return {
            }
        },
        methods: {
            changeColor(color) {
                // Captured the main canvas div element.
                const mainCanvas = document.getElementById('canvas');
                // Changing the background color depending on which color is clicked on in the color divs at the top.
                mainCanvas.style.background = color;
            }
        }
    }

</script>




<style scoped>

    .color-box {
        width: 30px;
        height: 30px;
        border: 1px solid black;
    }

</style>