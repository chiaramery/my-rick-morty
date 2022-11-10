<script>
import { store } from "../store";
import AppCard from './AppCard.vue';
export default {
    name: "AppMain",
    components: {
        AppCard,
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="wrap">
        <div class="row row-cols-2 row-cols-md-4 g-2">
            <div class="col" v-for="character in store.characters" :key="character.id">
                <AppCard :character="character" />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.wrap {
    width: 90%;
    margin: 2em auto;
}
</style>