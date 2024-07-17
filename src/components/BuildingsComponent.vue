<template>
  <div v-for="(building, buildingId) in buildings" :key="buildingId">
    <ModalComponent
      :buildingId="building.id"
      :elevators="building.elevatorsQty"
      :floors="building.floors.length"
    />
    <div class="building-container">
      <div class="info flex-container space-between">
        <h2>Building {{ building.id }}</h2>
        <img
          class="settings"
          width="20"
          height="20"
          src="https://svgsilh.com/svg/98446.svg"
        />
      </div>
      <div class="building">
        <div v-for="(floor, floorId) in building.floors" :key="floorId">
          <div class="floor">
            <span class="floor-number">{{
              building.floors.length - floorId
            }}</span>
            <div class="elevator-section flex-container">
              <div
                v-for="(elevator, elevatorId) in building.floors"
                :key="elevatorId"
              >
                <span class="current-floor">{{ elevator.ele_position }}</span>
                <div class="flex-container elevators">
                  <img width="auto" height="70" :src="elevatorImg" />
                  <div class="flex-container buttons">
                    <button type="button" class="up flex-container">
                      <img
                        width="10"
                        height="10"
                        src="https://www.svgrepo.com/show/93813/up-arrow.svg"
                      />
                    </button>
                    <button type="button" class="down flex-container">
                      <img
                        width="10"
                        height="10"
                        src="https://www.svgrepo.com/show/80156/down-arrow.svg"
                      />
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import ModalComponent from "../components/ModalComponent.vue";

const elevatorImg = require("@/assets/img/Automatic-Door.png");

defineProps({
  buildings: {
    type: Array,
    required: true,
  },
});
</script>

<style scoped>
button {
  background-color: transparent;
  border: none;
  padding: 0;
}
</style>
