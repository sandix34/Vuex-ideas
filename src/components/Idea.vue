<template>
  <div class="flex items-stretch  border border-grey-500 rounded-sm w-56 h-16 m-2 cursor-move shadow-lg">
    <h3 class="self-center flex-1 ">{{ item.title }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  }
};
</script>
