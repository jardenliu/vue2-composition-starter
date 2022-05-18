<template>
    <div>
        <input v-model="count"/>
        {{count}}
        <button @click="count++">+</button>
        <button @click="count--">-</button>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "@vue/composition-api"
import { useLocalStorage } from '@vueuse/core'
export default defineComponent({
    setup () {
        const count = useLocalStorage('vue-count', 1)

        return {
            count
        }
    }
})

</script>