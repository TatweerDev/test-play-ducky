<template>
  <div :class="$style.icons2424" :data-color="color" :data-icon="icon">
    <img
      :class="$style.dsaddasdas5Icon"
      alt=""
      src="../assets/dsaddasdas-5-4@2x.png"
    />
  </div>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IconRight",
  props: {
    color: { type: String, default: "Blue" },
    icon: { type: String, default: "Gamepad" },
  },
});
</script>
<style module>
.dsaddasdas5Icon {
  width: 22px;
  height: 22px;
  position: relative;
  object-fit: cover;
}
.icons2424 {
  width: 24px;
  height: 24px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-12xs);
  box-sizing: border-box;
}
</style>
