<template>
  <Title>Trefort Diákönkormányzat</Title>
  <main>
    <NavbarComponent />
    <TitleComponent />
  </main>
</template>

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
}

h1 {
  font-size: 15rem;
}

.rounded-30 {
  border-radius: 30px;
}

a {
  text-decoration: none;
  color: var(--clr-secondary-purple);
}

a.active {
  color: var(--clr-main-purple);
}
</style>