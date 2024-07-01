<template>
  <div class="elevator-container flex-container">
    <div>
      <span class="current-floor">1</span>
      <div class="flex-container elevators">
        <img width="auto" height="70" :src="elevatorImg" />
        <div class="flex-container buttons">
          <div class="up flex-container">
            <img
              width="10"
              height="10"
              src="https://www.svgrepo.com/show/93813/up-arrow.svg"
            />
          </div>
          <div class="down flex-container">
            <img
              width="10"
              height="10"
              src="https://www.svgrepo.com/show/80156/down-arrow.svg"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ElevatorsArea",
  // props: {
  //   msg: String
  // }
  data() {
    return {
      elevatorImg: require("@/assets/img/Automatic-Door.png"),
    };
  },
};
</script>
