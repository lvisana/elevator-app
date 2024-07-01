<template>
  <h1>Elevator App</h1>
  <div class="building-area-container">
    <div class="add">
      <img
        src="https://www.svgrepo.com/show/2087/plus.svg"
        width="30"
        height="30"
      />
    </div>
    <BuildingArea />
  </div>
</template>

<script>
import BuildingArea from "./components/BuildingArea.vue";

export default {
  name: "App",
  components: {
    BuildingArea,
  },
};
</script>
