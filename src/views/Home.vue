<template>
  <div class="home">
    <h1>Welcome to Ideas.io</h1>
    <Ideas/>
    <IdeaCreate/>
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
