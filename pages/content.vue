<template>
    <NavBar></NavBar>

    <div class="container text-center">
        <h2 class="p-3">Your Content</h2>

        <!-- The accordion section for photos, videos, and finished albums. -->
        <div class="accordion p-5" id="accordionExample">
            <div class="accordion-item">
                <h2 class="accordion-header" id="headingOne">
                    <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                    Your Photos
                    </button>
                </h2>
                <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
                    <div class="accordion-body">
                        <div class="text-center">
                            <!-- Dynamically looping through the misc images using the "v-for" vue directive. -->
                            <img v-for="(item, i) in miscImages" :key="i" :src="require(`../assets/content-images/${item}.jpg`)" alt="Misc pictures" class="img-fluid p-3" width="150" height="150">
                        </div>
                    </div>
                </div>
            </div>
            <div class="accordion-item">
                <h2 class="accordion-header" id="headingTwo">
                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Your Videos
                    </button>
                </h2>
                <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#accordionExample">
                    <div class="accordion-body">
                        <!-- If there are no videos in the video data (script below) then show this strong message. -->
                    <strong v-if="!this.videos.length">You do not currently have any stored videos.</strong>
                    </div>
                </div>
            </div>
            <div class="accordion-item">
                <h2 class="accordion-header" id="headingThree">
                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                    Your Published Albums
                    </button>
                </h2>
                <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionExample">
                    <div class="accordion-body">
                        <!-- The two fake albums that the user might have already created. -->
                        <div class="text-center">
                            <img src="../assets/images/album1.jpg" alt="Album template" class="img-fluid p-3" width="300" height="300">
                            <img src="../assets/images/album2.jpg" alt="Album template" class="img-fluid p-3" width="300" height="300">
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>

</template>



<script>

    export default {
        data() {
            return {
                videos: [],
                miscImages: [
                    'Beach7',
                    'Hotel2',
                    'Hotel5',
                    'pic1',
                    'pic2',
                    'pic3',
                    'pic4',
                    'pic5',
                    'pic6',
                    'pic7',
                    'pic8',
                    'pic9',
                    'pic10',
                    'pic11'
                ]
            }
        }
    }

</script>