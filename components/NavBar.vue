<template>

    <!-- Navbar that turns into an accordion on small screen sizes with the help of Bootstrap. -->
    <nav class="navbar navbar-expand-lg bg-light">
        <div class="container-fluid">
            <!-- Main logo which can be clicked to go back to home page and reload the website. -->
            <NuxtLink class="navbar-brand text-info p-4" to="/">Famous Albums</NuxtLink>
            <!-- The nav button that is folded on smaller screens. -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- All of the different links to get to each webpage. Router links are used instead of anchors or buttons. -->
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <NuxtLink class="nav-link active" to="/">Home</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink class="nav-link" to="/templates">Album Templates</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink class="nav-link" to="/content">Your Content</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink class="nav-link" to="/albums">Your Albums</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

</template>