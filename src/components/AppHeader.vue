<script>
export default {
    name: "Appheader"
}
</script>

<template>
    <header>
        <div class="title">
            <h1>Rick and Morty</h1>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100%;

    .title {
        width: 90%;
        margin: .4em auto;
        text-align: center;
        padding: 1.2em;
        background-color: whitesmoke;
        box-shadow: 5px 10px black;
    }
}
</style>