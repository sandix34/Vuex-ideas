<template>
  <div>
    <h1>Ideas</h1>
    <ul>
      <draggable >
        <Idea v-for="idea in allIdeas" :key="idea.id" :item="idea"/>
      </draggable>
    </ul>
  </div>
</template>

<script>
import draggable from 'vuedraggable';
import Idea from '@/components/Idea';

export default {
  components: {
    draggable,
    Idea,
  },
  computed: {
    allIdeas() {
      return this.$store.getters.allIdeas; 
    }
  },
};
</script>

<style lang="scss" scoped>
</style>