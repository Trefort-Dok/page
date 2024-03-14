<script lang="ts">
export default {
  data() {
    return {
      hoveredIndex: -1,
      leaders: [
        {
          name: 'Gombos Roland',
          rank: 'Alelnök',
          imgSrc: '/images/leaders/gombos_roland.png',
          contactIcon: '/public/svg/instagram.svg',
          contactLink: 'https://www.instagram.com/roland.gombos/',
          contactText: 'roland.gombos'
        },
        {
          name: 'Petrovszki Gergő',
          rank: 'Alelnök',
          imgSrc: '/images/leaders/petrovszki_gergo.png',
          contactIcon: '/svg/instagram.svg',
          contactLink: 'https://www.instagram.com/ptrvszkgrgptrk/',
          contactText: 'ptrvszkgrgptrk'
        },
        {
          name: 'Kucsa Dávid',
          rank: 'Elnök',
          imgSrc: '/images/leaders/kucsa_david.png',
          contactIcon: '/svg/instagram.svg',
          contactLink: 'https://www.instagram.com/ddvokcs/',
          contactText: 'ddvokcs'
        },
        {
          name: 'Kovács Levente',
          rank: 'Alelnök',
          imgSrc: '/images/leaders/kovacs_levente.png',
          contactIcon: '/svg/instagram.svg',
          contactLink: 'https://www.instagram.com/levente__kovacs/',
          contactText: 'levente__kovacs'
        },
        {
          name: 'Rácz Attila',
          rank: 'Segítő tanár',
          imgSrc: '/images/leaders/racz_attila.png',
          contactIcon: '/svg/facebook-f.svg',
          contactLink: 'https://www.facebook.com/attila.racz.946/',
          contactText: 'attila.racz.946'
        }
      ]
    };
  },

  methods: {
    handleCardHover(index: number) {
      this.hoveredIndex = index;
    },
    handleCardLeave() {
      this.hoveredIndex = -1;
    },
    handleOpacity(index: number) {
      return this.hoveredIndex === -1 || this.hoveredIndex === index ? 1 : 0.75;
    },
    handleTransform(index: number) {
      return this.hoveredIndex === -1 || this.hoveredIndex === index ? '0deg' : index + (index * 0.2) + 'deg';
    }
  }
};
</script>

<template>
  <div :id="'leaderWrapper'" :class="'parent'">
    <div class="container">
      <div class="titleContainer">
        <img src="/svg/leaderTitle.svg" />
      </div>
      <div class="motivationTextContainer">
        Osszátok meg velünk gondolataitokat, és biztosak lehettek benne, hogy
        minden tőlünk telhetőt megteszünk a helyzet javítása érdekében. 😉
      </div>
      <lCardComponent 
          v-for="(leader, index) in leaders"
          :key="index" :name="leader.name"
          :rank="leader.rank"
          :imgSrc="leader.imgSrc" 
          :contactIcon="leader.contactIcon"
          :contactLink="leader.contactLink"
          :contactText="leader.contactText"
          @mouseover="handleCardHover(index)" 
          @mouseleave="handleCardLeave"
          :class="'cardContainer cardContainer' + (index + 1)"
          :style="{ 'transform': index === hoveredIndex ? 'scale(1) rotateZ(1.25deg)' : 'scale(.85) ' + 'rotateZ(' + handleTransform(index) + ')', 'opacity': handleOpacity(index),  }" />
    </div>
  </div>
</template>

<style scoped>
#leaderWrapper {
  margin: 0 auto;
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

.cardContainer {
  cursor: pointer;
  transition: all 300ms cubic-bezier(0,1.53,1,.99) 50ms;
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

@media only screen and (max-width: 1260px) {
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