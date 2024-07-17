<template>
  <h1>Elevator App</h1>
  <div class="building-area-container">
    <div @click="addBuilding" class="add">
      <img
        src="https://www.svgrepo.com/show/2087/plus.svg"
        width="30"
        height="30"
      />
    </div>
    <div id="buildingArea" class="flex-container">
      <BuildingsComponent :buildings="buildings" />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import BuildingsComponent from "./components/BuildingsComponent.vue";

const currentBuildings = ref(1);
const buildings = ref([
  {
    id: 1,
    elevatorsQty: 2,
    floors: [
      {
        1: {
          ele_position: 1,
        },
      },
      {
        1: {
          ele_position: 2,
        },
      },
    ],
  },
]);

console.log(buildings.value);

const addBuilding = () => {
  currentBuildings.value += 1;
  let newBuilding = {
    id: currentBuildings.value,
    elevatorsQty: 1,
    floors: [{ 1: { position: 1 } }],
  };
  buildings.value.push(newBuilding);
};
</script>
