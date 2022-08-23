<template>
    <!-- Rendering the list of emojis received from the external API: https://github.com/cheatsnake/emojihub -->
    <div class="emoji-list">
        <div v-for="(emoji, index) in emojis" :key="index" class="m-3">
            <p>{{emoji.htmlCode[0]}}</p>
        </div>
    </div>

</template>





<script>
    import axios from 'axios';

    export default {
        data() {
            return {
                // The array of emoji HTML codes from the external API.
                emojis: []
            }
        },
        methods: {
            loadEmojis() {
                // Fetched the external API with the npm package "axios".
                axios.get('https://emojihub.herokuapp.com/api/all/group_animal_bird').then(response => {
                    this.emojis = response.data;
                    console.log(this.emojis);
                }).catch(error => {
                    console.log(error);
                })
            }
        },
        mounted() {
            this.loadEmojis();
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
        height: 8rem;
        width: auto;
    }

</style>