<template>
  <div class="home">
    <h1 class="text-5xl font-semibold">Welcome to Ideas.io</h1>
    <IdeaCreate/>
    <Ideas/>
  </div>
</template>

<script>
import Ideas from '@/components/Ideas' ;
import IdeaCreate from '@/components/IdeaCreate';

export default {
  name: "home",
  components: {
    Ideas,
    IdeaCreate,
  },
};
</script>
