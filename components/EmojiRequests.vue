<template>

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
                emojis: []
            }
        },
        methods: {
            loadEmojis() {
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