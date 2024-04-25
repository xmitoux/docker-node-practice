<script setup lang="ts">
import { ref } from 'vue';

const members: Aqours[] = [
    'Chika',
    'Riko',
    'Kanan',
    'Dia',
    'You',
    'Yoshiko',
    'Hanamaru',
    'Mari',
    'Ruby',
];

const selectedMember = ref<Aqours | null>(null);

const emit = defineEmits<{ change: [selectedMember: Aqours | null] }>();
</script>

<template>
    <select
        v-model="selectedMember"
        @change="emit('change', selectedMember)"
        class="aqours-selector"
    >
        <option :value="null">Select a member</option>
        <option v-for="member in members" :key="member">{{ member }}</option>
    </select>
</template>

<style scoped>
.aqours-selector {
    padding: 10px 15px;
    border-radius: 5px;
    border: 1px solid #ccc;
    font-size: 1em;
}
</style>
