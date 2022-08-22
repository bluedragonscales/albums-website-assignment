<template>

    <div @dragenter.prevent="toggleActive" 
        @dragleave.prevent="toggleActive"
        @dragover.prevent
        @drop.prevent="toggleActive"
        :class="{'active-dropzone': active}"
        class="dropzone"
        >
        <p>Drag or Drop File</p>
        <p>OR</p>
        <label for="dropzoneFile">Select File</label>
        <input type="file" id="dropzoneFile" class="dropzoneFile">
    </div>

</template>



<script>
    import { ref } from 'vue';

    export default {
        data() {
            return {

            }
        },
        name: "DropZone",
        setup() {
            const active = ref(false);

            const toggleActive = () => {
                active.value = !active.value;
            }

            return {active, toggleActive};
        }
    }

</script>



<style scoped>

    .dropzone {
        margin: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        row-gap: 16px;
        transition: .3s ease all;
    }

    label {
        padding: 10px 15px;
        color: white;
        background-color: green;
        transition: 0.3s ease all;
        cursor: pointer;
    }

    input {
        display: none;
    }

    .active-dropzone label{
        color: black;
        background-color: white;
    }

</style>