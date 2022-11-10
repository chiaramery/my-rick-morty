<script>
export default {
    name: "AppCard",
    props: {
        character: Object
    }
}
</script>

<template>
    <div class="item">
        <img class="rounded-circle" :src="character.image" alt="">
        <div class="name text-center">{{ character.name.toUpperCase() }}</div>
    </div>
</template>

<style lang="scss" scoped>
.item {
    padding: .3em;
    display: flex;
    align-items: center;
    flex-direction: column;
    color: white;
    background-color: rgb(47 71 50);
    border: 1px solid white;

    img {
        width: 90%;
        border: 1px solid white;
    }
}
</style>