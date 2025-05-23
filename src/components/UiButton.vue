<template>
    <button :class='classe' @click="emitEvtClick">
        {{ title }}
    </button>
</template>

<script setup>

defineProps({
    title: {
        type: String,
        required: true,
    },
    classe: {
        type: String,
        default: "",
    },
});

const emit = defineEmits(['evtClick']) // Define the emit event

function emitEvtClick() { // Emit the event when the button is clicked
  emit('evtClick') // Emit the event
}

</script>

<style scoped>
.btn {
    background-color: #42b983;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 5px;
}

.btn2 {
    background-color: red;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 5px;
}
</style>
