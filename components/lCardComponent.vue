<script lang="ts" setup>
const props = defineProps({
  rank: {
    type: String,
    require: true,
  },
  name: {
    type: String,
    require: true,
  },
  contactLink: String,
  contactText: String,
  contactIcon: String,
  imgSrc: {
    type: String,
    require: true,
  },
});
</script>

<template>
  <div :id="'cardWrapper'" :class="'card'">
    <div :id="'cardImage'" :style="{ backgroundImage: `url(${props.imgSrc})` }">
      <div :id="'cardInner'">
        <h3 :id="'cardInnerName'">{{ props.name }}</h3>
        <span :id="'cardInnerRank'">{{ props.rank }}</span>
      </div>
    </div>
    <a :id="'contactLink'" :href="props.contactLink" :target="'_blank'">
      <img :src="props.contactIcon" :alt="'Instagram'" />
      <span :id="'contactText'">{{ props.contactText }}</span>
    </a>
  </div>
</template>

<style scoped>
:root {
  --clr-main-purple: #451DE3;
  --clr-dark-purple: #1E004B;
  --clr-secondary-purple: #6D5E84;
  --clr-gray-text: #8F8F8F;
  --clr-bg-color: #F7F8FD;
}

a,
h3 {
  text-decoration: none;
  color: inherit;
  padding: 0;
  margin: 0;
}

a {
  color: var(--clr-dark-purple);
  text-align: center;
  cursor: pointer;
  width: 146px;
  height: 32px;
  border: 1px solid var(--clr-dark-purple);
  padding: 4px 24px;
  margin: 0 auto;
  border-radius: 50px;
}

#cardWrapper {
  display: grid;
  grid-template-rows: repeat(2, 1fr);
  gap: 1rem;
  width: 220px;
  height: 329.63px;
  padding: 1rem;
  color: white;
  border-radius: 30px;
  box-shadow: #63636340 0px 2px 8px 0px;
}

#cardWrapper:nth-child(2) {
  margin-top: 4rem;
}

#cardImage {
  position: relative;
  min-width: 100%;
  height: 239.63px;
  border-radius: 20px 20px 10px 10px;
  background-repeat: no-repeat no-repeat;
  background-size: cover;
  background-position: top;
}

#cardInner {
  position: absolute;
  top: 16px;
  left: 16px;
}

#contactLink {
  display: flex;
  align-self: center;
  justify-content: center;
}

#contactLink img {
  height: 24px;
  display: flex;
  align-self: center;
}

#cardInnerRank {
  color: var(--clr-main-purple);
  size: 16px;
}

#contactText {
  display: flex;
  align-items: center;
  margin-left: 8px;
}

#cardInnerName {
  padding: 4px;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 4px 4px 4px 0px;
}

#cardInnerRank {
  width: max-content;
  padding: 0px 4px;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 0px 0px 4px 4px;
}

@media only screen and (max-width: 1024px) {
  #cardWrapper:nth-child(2) {
    margin-top: 0rem;
  }
}
</style>
