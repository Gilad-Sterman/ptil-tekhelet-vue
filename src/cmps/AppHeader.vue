<template>
    <section class="app-header">
        <button @click="nav('/')">
            <img src="https://res.cloudinary.com/dollaguij/image/upload/v1700476247/eng1_rpfhk8.png" alt="">
        </button>
        <button @click="nav('/heb')">
            <img src="https://res.cloudinary.com/dollaguij/image/upload/v1700476247/heb1_rmybm6.png" alt="">
        </button>
    </section>
</template>

<script>
export default {
    methods: {
        nav(to) {
            this.$router.push(to)
            window.scrollTo(0, 0)
        }
    }
}
</script>

<style lang="scss">
.app-header {
    position: sticky;
    top: 0;
    padding: .5rem;
    display: flex;
    align-items: center;
    gap: .5rem;
    z-index: 10;
    height: 65px;
    background-color: white;

    button {
        background-color: transparent;
        border: none;

        &:hover {
            scale: 1.05;
        }
    }

    img {
        width: 48px;
        border-radius: .25rem;
    }
}
</style>