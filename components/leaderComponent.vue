<script lang="ts">
import lCardComponent from "./lCardComponent.vue";
</script>

<template>
  <div :id="'leaderWrapper'" :class="'parent'">
    <div class="container">
      <div class="titleContainer">
        <img src="/leaderTitle.svg" />
      </div>
      <div class="motivationTextContainer">
        Osszátok meg velünk gondolataitokat, és biztosak lehettek benne, hogy
        minden tőlünk telhetőt megteszünk a helyzet javítása érdekében. 😉
      </div>
      <div class="cardContainer1 cardContainer">
        <lCardComponent :name="'Gombos Roland'" :rank="'Alelnök'" :imgSrc="'/images/leaders/gombos_roland.png'"
          :contactIcon="'/instagram.svg'" :contactLink="'https://www.instagram.com/roland.gombos/'"
          :contactText="'roland.gombos'" />
      </div>
      <div class="cardContainer2 cardContainer">
        <lCardComponent :name="'Petrovszki Gergő'" :rank="'Alelnök'" :imgSrc="'/images/leaders/petrovszki_gergo.png'"
          :contactIcon="'/instagram.svg'" :contactLink="'https://www.instagram.com/ptrvszkgrgptrk/'"
          :contactText="'ptrvszkgrgptrk'" />
      </div>
      <div class="cardContainer3 cardContainer">
        <lCardComponent :name="'Kucsa Dávid'" :rank="'Elnök'" :imgSrc="'/images/leaders/kucsa_david.png'"
          :contactIcon="'/instagram.svg'" :contactLink="'https://www.instagram.com/ddvokcs/'" :contactText="'ddvokcs'" />
      </div>
      <div class="cardContainer4 cardContainer">
        <lCardComponent :name="'Kovács Levente'" :rank="'Alelnök'" :imgSrc="'/images/leaders/kovacs_levente.png'"
          :contactIcon="'/instagram.svg'" :contactLink="'https://www.instagram.com/levente__kovacs/'"
          :contactText="'levente__kovacs'" />
      </div>
      <div class="cardContainer5 cardContainer">
        <lCardComponent :name="'Rácz Attila'" :rank="'Segítő tanár'" :imgSrc="'/images/leaders/racz_attila.png'"
          :contactIcon="'/facebook-f.svg'" :contactLink="'https://www.facebook.com/attila.racz.946/'"
          :contactText="'attila.racz.946'" />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&display=swap");

#leaderWrapper {
  margin: 0 auto;
  font-family: "DM Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}

.container {
  display: grid;
  grid-template-rows: auto auto auto auto auto;
  grid-auto-flow: row;
  grid-template-areas:
    "titleContainer titleContainer titleContainer titleContainer titleContainer"
    "cardContainer1 motivationTextContainer motivationTextContainer motivationTextContainer cardContainer5"
    "cardContainer1 cardContainer2 cardContainer3 cardContainer4 cardContainer5"
    ". cardContainer2 cardContainer3 cardContainer4 .";
  width: min-content;
  margin: 0 auto;
}

.titleContainer {
  margin: 0 auto;
  grid-area: titleContainer;
}

.motivationTextContainer {
  grid-area: motivationTextContainer;
  height: 66px;
  width: 490.28px;
  text-align: center;
  margin: 0 auto;
  color: #1E004B;
}

.cardContainer1,
.cardContainer2,
.cardContainer3,
.cardContainer4,
.cardContainer5 {
  padding: 1rem;
  transform: scale(1);
  opacity: 1;
}

.cardContainer1 {
  grid-area: cardContainer1;
}

.cardContainer2 {
  grid-area: cardContainer2;
  height: min-content;
}

.cardContainer3 {
  grid-area: cardContainer3;
  height: min-content;
  margin-top: 4rem;
}

.cardContainer4 {
  grid-area: cardContainer4;
  height: min-content;
}

.cardContainer5 {
  grid-area: cardContainer5;
}

@media only screen and (max-width: 1200px) {
  .container {
    gap: 6px 0px;
    grid-template-areas:
      "titleContainer"
      "motivationTextContainer"
      "cardContainer1"
      "cardContainer2"
      "cardContainer3"
      "cardContainer4"
      "cardContainer5";
    width: auto;
  }

  .cardContainer3 {
    grid-area: cardContainer3;
    margin-top: 0rem;
  }

  .cardContainer1,
  .cardContainer2,
  .cardContainer3,
  .cardContainer4,
  .cardContainer5 {
    margin: 0 auto;
  }

  .motivationTextContainer {
    width: 390px;
  }
}
</style>
