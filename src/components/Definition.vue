<template>
    <div>
        definition
    </div>
</template>

<script setup>
import axios from 'axios'
import { watch, ref } from 'vue'

const props = defineProps({
    searchWord: String
})

watch(() => props.searchWord, getData)
const result = ref([])

async function getData(word) {
    const url = `https://api.dictionaryapi.dev/api/v2/entries/en/${word}`
    try {
        const data = await axios.get(url)
        result.value = data.data
    } catch (err) {
        console.log(err)
    }
}

</script>

<style>
</style>
