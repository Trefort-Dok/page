<script lang="ts" setup>
import lCardComponent from "./lCardComponent.vue";
</script>

<template>
  <div id="leaderComponent" style="flex-direction: column">
    <img src="/leaderTitle.svg" />
    <h4 :id="'leaderMotivationText'" :class="'MOBILE'">
      Osszátok meg velünk gondolataitokat, és biztosak lehettek benne, hogy
      minden tőlünk telhetőt megteszünk a helyzet javítása érdekében. 😉
    </h4>
    <div id="cardsWrapper" style="flex-direction: row">
      <lCardComponent
        :name="'Gombos Roland'"
        :rank="'Alelnök'"
        :imgSrc="'/images/leaders/gombos_roland.png'"
        :contactIcon="'/instagram.svg'"
        :contactLink="'https://www.instagram.com/roland.gombos/'"
        :contactText="'roland.gombos'"
      />
      <div id="cardAndText" style="flex-direction: column">
        <h4 :id="'leaderMotivationText'" :class="'PC'">
          Osszátok meg velünk gondolataitokat, és biztosak lehettek benne, hogy
          minden tőlünk telhetőt megteszünk a helyzet javítása érdekében. 😉
        </h4>
        <div id="cardandtextinner" style="gap: 4rem">
          <lCardComponent
            :name="'Petrovszki Gergő'"
            :rank="'Alelnök'"
            :imgSrc="'/images/leaders/petrovszki_gergo.png'"
            :contactIcon="'/instagram.svg'"
            :contactLink="'https://www.instagram.com/ptrvszkgrgptrk/'"
            :contactText="'ptrvszkgrgptrk'"
          />
          <div :id="'translatedDiv'">
            <lCardComponent
              :name="'Kucsa Dávid'"
              :rank="'Elnök'"
              :imgSrc="'/images/leaders/kucsa_david.png'"
              :contactIcon="'/instagram.svg'"
              :contactLink="'https://www.instagram.com/ddvokcs/'"
              :contactText="'ddvokcs'"
            />
          </div>
          <lCardComponent
            :name="'Kovács Levente'"
            :rank="'Alelnök'"
            :imgSrc="'/images/leaders/kovacs_levente.png'"
            :contactIcon="'/instagram.svg'"
            :contactLink="'https://www.instagram.com/levente__kovacs/'"
            :contactText="'levente__kovacs'"
          />
        </div>
      </div>
      <lCardComponent
        :name="'Rácz Attila'"
        :rank="'Segítő tanár'"
        :imgSrc="'/images/leaders/racz_attila.png'"
        :contactIcon="'/facebook-f.svg'"
        :contactLink="'https://www.facebook.com/attila.racz.946/'"
        :contactText="'attila.racz.946'"
      />
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&display=swap");

#leaderComponent {
  font-family: "DM Sans", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}

#leaderComponent,
#cardsWrapper,
#cardandtextinner {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

#cardsWrapper {
  height: 800px;
  gap: 4rem;
}

#translatedDiv {
  transform: translateY(50px);
}

#leaderMotivationText {
  text-align: center;
  width: 490px;
  font-size: 20px;
  margin: 0 auto;
}
.PC {
margin-bottom: 2rem !important;
}

.MOBILE {
  display: none;
}

@media only screen and (max-width: 1024px) {
  #leaderMotivationText {
    width: 350px;
  }

  #translatedDiv {
    transform: translateY(0px);
  }

  .PC {
    display: none !important;
    margin: 0rem !important;
  }

  .MOBILE {
    display: block !important;
    margin-bottom: 1rem !important;
  }
}
</style>
