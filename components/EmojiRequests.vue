<template>

    <div class="emoji-list">
        <p v-for="(emoji, index) in emojis" :key="index" class="m-3">{{emoji.name}}: <span>{{emoji.htmlCode[0]}}</span></p>
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
        height: 10rem;
    }

</style>