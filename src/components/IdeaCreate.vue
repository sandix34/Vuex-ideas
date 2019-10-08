<template>
  <div>
    <form @submit.prevent="create">
      <label for="idea-title">Ideas's title</label><br>
      <input type="text" id="idea-title" v-model="title" />
      <button type="submit">create</button>
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
			console.log(this.title);
			this.title = "";
			
		}
  }
};
</script>

<style scoped>
</style>