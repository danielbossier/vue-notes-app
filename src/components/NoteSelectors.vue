<template>
  <div class="note-selectors">
    <NoteSelector v-for="note in notes" v-bind:note="note" :key="note.id" />
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector.vue";

export default {
  components: {
    NoteSelector,
  },
  data: function () {
    return {
      notes: [
        { id: 1, body: "Thou shalt make it work", timestamp: Date.now() },
        { id: 2, body: "Thou shalt push thy code", timestamp: Date.now() },
        { id: 3, body: "Thou shalt make it cute", timestamp: Date.now() },
        { id: 4, body: "Thou shalt not put components in thy Capstone", timestamp: Date.now() },
      ],
    };
  },
};
</script>
