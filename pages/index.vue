<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="You did the web development thing..!" />

      <!--added NuxtLinks for additional pages-->
      <nav>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/accordion">Accordion</NuxtLink>
        <NuxtLink to="/images">Images</NuxtLink>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
