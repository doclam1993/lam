<template>
  <div class="content p-5">
    <button
      class="mr-3 bg-yellow-500 hover:bg-yellow-400 text-white font-bold py-2 px-4 border-b-4 border-yellow-700 hover:border-yellow-500 rounded"
      v-for="(obj, index) in objects"
      :key="index"
      @click="$stage.lookAt({ index, zoom:obj.zoom })"
    >{{ obj.name }}</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      objects: [
        {
          name: "Cube",
          zoom: 1.5
        },
        {
          name: "Ico"
        },
        {
          name: "Sphere",
          zoom: 1.8
        }
      ]
    };
  },
  mounted() {
    console.log(this.$stage);
  }
};
</script>
