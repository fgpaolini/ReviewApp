<template>
    <div >
        <Card style="width: 25rem; overflow: hidden">
            <template #header>
                <img alt="user header" src="/assets/demo/images/products/placeholder.avif" />
            </template>
            <template #title>{{ name }}</template>
            <template #subtitle>{{ category }}</template>
            <template #content>
                <Rating :modelValue="rating" />
            </template>
            <template #footer>
                <div class="flex gap-3 mt-1">
                    <Button label="Ver" class="w-full" @click="navigateTo(`/products/${to}`)" />
                </div>
            </template>
        </Card>
    </div>
</template>

<script setup lang="ts">

const prop = defineProps({
    name: {
        type: String,
        default: 'Lorem Ipsum'
    },
    category: {
        type: String,
        default: 'Category'
    },
    rating: {
        type: Number,
        default: 0
    },
    to: {
        type: String,
        default: '/'
    }
})

const value = ref<number>()

</script>

<style scoped>
a {
    cursor: pointer;
}

</style>