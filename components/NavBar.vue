<template>

    <!-- Navbar that turns into an accordion on small screen sizes with the help of Bootstrap. -->
    <nav class="navbar navbar-expand-lg bg-light">
        <div class="container-fluid">
            <!-- Main logo which can be clicked to go back to home page and reload the website. -->
            <a class="navbar-brand text-info p-4" href="/">Famous Albums</a>
            <!-- The nav button that is folded on smaller screens. -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- All of the different links to get to each webpage. Router links are used instead of anchors or buttons. -->
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="/">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/templates">Album Templates</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/content">Your Content</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/albums">Your Albums</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

</template>