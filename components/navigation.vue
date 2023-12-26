<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <h1>Travel Buddy</h1>
        <div class="container-fluid">
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                aria-controls="#navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item">
                        <NuxtLink to="/" class="nav-link">Home</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink to="/accordion" class="nav-link">Accordion</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink to="/images" class="nav-link">Images</NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink to="/about" class="nav-link">About</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'navigation',
}
</script>