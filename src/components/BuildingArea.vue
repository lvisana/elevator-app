<template>
  <div id="buildingArea" class="flex-container">
    <div class="building-container">
      <div class="info flex-container">
        <img
          class="settings"
          width="20"
          height="20"
          src="https://svgsilh.com/svg/98446.svg"
        />
      </div>
      <div class="building">
        <div class="floor">
          <span class="floor-number">2</span>
          <ElevatorsArea />
        </div>
        <div class="floor">
          <span class="floor-number">1</span>
          <ElevatorsArea />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ElevatorsArea from "./ElevatorsArea.vue";

export default {
  name: "BuildingArea",
  // props: {
  //   msg: String
  // }
  components: {
    ElevatorsArea,
  },
};
</script>
