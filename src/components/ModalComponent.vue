<template>
  <div class="modal">
    <form action="" method="POST">
      <button type="button" class="close">
        <img
          width="20"
          height="20"
          src="https://cdn.icon-icons.com/icons2/2518/PNG/512/x_icon_150997.png"
        />
      </button>
      <h3>Building {{ buildingId }} Settings</h3>
      <div class="flex-container input-container space-between">
        <div class="flex-container flex-column align-center">
          <div><label for="elevators_qty">Elevators Quantity</label></div>
          <div>
            <input
              type="number"
              :value="elevators"
              name="elevators_qty"
              id="elevators_qty"
            />
          </div>
        </div>
        <div class="flex-container flex-column align-center">
          <div><label for="floors_qty">Floors Quantity</label></div>
          <div>
            <input
              type="number"
              :value="floors"
              name="floors_qty"
              id="floors_qty"
            />
          </div>
        </div>
      </div>
      <div class="flex-container space-between" style="gap: 8px">
        <div><button class="danger" type="button">Remove Building</button></div>
        <div><button class="primary" type="submit">Save Changes</button></div>
      </div>
    </form>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  buildingId: {
    type: Array,
    required: true,
  },
  elevators: {
    type: Number,
    required: true,
  },
  floors: {
    type: Number,
    required: true,
  },
});
</script>
