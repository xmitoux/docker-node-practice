<script setup lang="ts">
import { ref } from 'vue';
import AqoursSelector from '@/components/AqoursSelector.vue';

defineProps<{ msg: string }>();

const selectedMember = ref<Aqours | null>(null);
const onSelectAqours = (member: Aqours | null) => (selectedMember.value = member);
</script>

<template>
    <div class="home-container">
        <h1>{{ msg }}</h1>
        <div class="selector-container">
            <div class="horizontal-container">
                <p>Who's your wife?</p>
                <AqoursSelector @change="onSelectAqours" />
            </div>
            <p v-if="selectedMember === 'Riko'" class="highlight">NO!😠 RIKO IS MY WIFE!!!😡😡😡</p>
            <p v-else>Your wife is {{ selectedMember ? `${selectedMember}!` : '?' }}</p>
        </div>
    </div>
</template>

<style scoped>
.home-container {
    text-align: center;
    padding: 20px;
}

.selector-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    margin-top: 20px;
}

.horizontal-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 10px;
}

.selector-container p {
    margin: 0;
    font-size: 1.2em;
}

.highlight {
    color: red;
    font-weight: bold;
    font-size: 1.5em;
    animation: pulse 1s infinite;
}

@keyframes pulse {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.2);
    }
    100% {
        transform: scale(1);
    }
}
</style>
