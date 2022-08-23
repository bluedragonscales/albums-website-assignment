<template>

    <div class="emoji-list">

    </div>

</template>



<script>
    import axios from 'axios';

    export default {
        data() {
            return {
                emojis: []
            }
        },
        methods: {
            loadEmojis() {
                axios.get('https://emojihub.herokuapp.com/api/category_animals_and_nature').then(response => {
                    console.log(response.data);
                    this.emojis = response.data;
                }).catch(error => {
                    console.log(error);
                })
            }
        }
    }

</script>




<style scoped>

    .emoji-list {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        overflow-x: scroll;
    }

</style>