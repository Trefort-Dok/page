<template>
    <section>
        <div>
            <h3>BSC Trefort <br> Diákönkományzat</h3>
        </div>
        <nav>
            <a v-for="item in props.navItems" :key="item.id" :href="'#' + item.id">{{ item.title }}</a>
        </nav>
    </section>
</template>
<script lang="ts" setup>

interface NavItem {
    title: string,
    id: string
}
const props = defineProps({
    navItems: Array<NavItem>
})
</script>
<style scoped>
section {
    display: flex;
    justify-content: space-between;
    padding: 3rem;
}

nav {
    display: flex;
    gap: 1rem;
}

a {
    position: relative;
    text-decoration: none;
    color: var(--clr-secondary-purple);
}

a::after {
    content: '';
    position: absolute;
    left: 0px;
    top: 2ch;
    width: 100%;
    height: 3px;
    transform: scaleX(0);
    transform-origin: right;
    background-color: var(--clr-main-purple);
    transition: transform .3s;
}

a:hover::after,
a:focus-within::after {
    transform: scaleX(1);
    transform-origin: left;
}

/* Ez nem működik még most se, de na prioritások XDD */
a.active {
    color: var(--clr-main-purple);
    transform: scaleX(1);
}
</style>