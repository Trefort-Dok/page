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
  <DevOnly>
    <div :id="'cardWrapper'">
      <div
        :id="'cardImage'"
        :style="{ backgroundImage: `url(${props.imgSrc})` }"
      >
        <div :id="'cardInner'">
          <h3 :id="'cardInnerName'">{{ props.name }}</h3>
          <div :id="'cardInnerRank'">{{ props.rank }}</div>
        </div>
      </div>
      <a :id="'contactLink'" :href="props.contactLink" :target="'_blank'">
        <img :src="props.contactIcon" :alt="'Instagram'" />
        <div :id="'contactText'">{{ props.contactText }}</div>
      </a>
    </div>
  </DevOnly>
</template>

<style scoped>
a,
h3 {
  text-decoration: none;
  color: inherit;
  padding: 0;
  margin: 0;
}

a {
  color: rgba(30, 0, 75, 1);
  text-align: center;
  cursor: pointer;
  width: 146px;
  height: 32px;
  border: 1px solid #1e004b;
  padding: 4px 12px;
  margin: 0 auto;
  border-radius: 50px;
}

#cardWrapper {
  display: grid;
  grid-template-rows: repeat(2, 1fr);
  gap: 1rem;
  width: 276.83px;
  height: 329.63px;
  padding: 1rem;
  color: white;
  border-radius: 30px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}

#cardImage {
  position: relative;
  min-width: 100%;
  height: 239.63px;
  border-radius: 20px 20px 10px 10px;
  background-repeat: no-repeat no-repeat;
  background-size: cover;
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
  color: #451de3;
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
</style>