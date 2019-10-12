<template>
  <div>
    <form @submit.prevent="create">
      <label for="idea-title">Ideas's title</label><br>
      <input class=" border border-green-600 p-1 rounded-sm" type="text" id="idea-title" v-model="title" />
      <button class="bg-green-700 text-white p-1 ml-1 rounded-sm " type="submit">create</button>
    </form>
  </div>
</template>

<script>
export default {
	data() {
		return {
			title: ""
		}
	},
  methods: {
    create() {
			const idea = {
        createdAt: new Date(),
        title: this.title,
      };
      // this.$store.commit('CREATE_IDEAS', idea);
      this.$store.dispatch('createIdea', idea);
			this.title = "";	
		}
  }
};
</script>
