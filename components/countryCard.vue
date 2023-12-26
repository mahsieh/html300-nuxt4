<script>
export default {
    props: {
        country: Object
    }
}

</script>

<template>
    <article class="card">
        <img :src="country.flag" :alt="country.name" class="card_img">
        <h2 class="card_title">{{ country.name }}</h2>
        <p class="card_copy">{{ country.subregion }}</p>
    </article>
</template>

<style>
.card {
    margin: 1rem;
    border: 1px solid black;
    padding: 1.5rem;
    max-width: 200px;
    min-height: 200px;

    &__img {
        display: block;
        margin-bottom: 1rem;
    }

    &__title {
        font-size: 1rem;
        margin-bottom: 0.25rem;
    }

    &__copy {
        font-size: 0.875rem;
    }
}</style>