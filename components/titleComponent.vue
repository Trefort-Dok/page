<template>
    <section>
        <img id="title" src="/titles/trefort.svg">
        <img moveable id="stabImg" class="rounded-30" src="/img/stab.bmp?url" alt="stab">
        <img moveable id="lolImg" class="rounded-30" src="/img/lol.bmp?url" alt="lol">
        <img moveable id="kotelImg" class="rounded-30" src="/img/kotel.bmp?url" alt="kotel">

    </section>
</template>

<style scoped>
img {
    width: 300px;
}

section {
    position: relative;
    display: grid;
    place-items: center;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    width: 100vw;
    height: 80vh;
}

h1 {
    text-shadow: 0px 0px 20px rgba(0, 0, 0, 1);
    position: relative;
    z-index: 10;
    color: var(--clr-main-purple);
}


#title {
    position: absolute;
    left: 50%;
    top: 50%;
    width: 890.622px;
    transform: translate(-50%, -50%);
}
</style>
