<template>
    <section>
        <img id="title" src="/titles/trefort.svg">
        <img moveable id="stabImg" class="rounded-30" src="/img/stab.bmp?url" alt="stab">
        <img moveable id="lolImg" class="rounded-30" src="/img/lol.bmp?url" alt="lol">
        <img moveable id="kotelImg" class="rounded-30" src="/img/kotel.bmp?url" alt="kotel">

    </section>
</template>

<style scoped>
img[moveable] {
    width: 300px;
}

section {
    position: relative;
    display: grid;
    place-items: center;
    grid-template-columns: repeat(3, 1fr);
    /* grid-template-rows: repeat(3, 1fr); */
    width: 100%;
    height: 80vh;
}
img[moveable]   {
    position: absolute;
    box-shadow: 0 0 25px 1px rgba(0, 0, 0, 0.15);
}
section img:nth-child(2n){
    top: 50%;
}
section img:nth-child(2){
    left: 20%;
    transform: rotate(-10deg) translate(-50%, -50%);
}
section img:nth-child(3){
    left: 50%;
    transform: rotate(5deg) translate(-50%, -50%);
}
section img:nth-child(4){
    right: 1%;
    transform: rotate(-13deg) translate(-50%, -50%);
}

#title {
    position: absolute;
    left: 50%;
    top: 50%;
    width: 890.622px;
    transform: translate(-50%, -50%);
    z-index: 99;
}
</style>
