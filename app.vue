<template>
  <Title>Trefort Diákönkormányzat</Title>
  <main>
    <NavbarComponent :nav-items="navbar" />
    <TitleComponent id="homePage" />
    <LeaderComponent data-aos="fade-up" id="leaders" />
  </main>
</template>

<script lang="ts" setup>
const navbar = [
  {title: 'Kezdőlap', id: 'homePage'},
  {title: 'Vezetőség', id: 'leaders'},
  ]
</script>

<style scoped>
main {
  min-height: 100vh;
}
</style>

<style>
@import url("https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&display=swap");

:root {
  --clr-main-purple: #451DE3;
  --clr-dark-purple: #1E004B;
  --clr-secondary-purple: #6D5E84;
  --clr-gray-text: #8F8F8F;

}

* {
  font-family: "DM Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  margin: 0;
  padding: 0;

  scroll-behavior: smooth;
}

h1 {
  font-size: 15rem;
}

.rounded-30 {
  border-radius: 30px;
}

</style>