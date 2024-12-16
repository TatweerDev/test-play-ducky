<template>
  <div class="friendsRow">
    <div class="friendsItems">
      <img class="iconQuestion" loading="lazy" :alt="name" :src="imageSrc" />
    </div>
    <div class="name">{{ name }}</div>
    <div class="gamepads">
      <img v-if="isMedal" class="unionIcon" alt="" src="../assets/union.svg" />
      <div class="lvl">{{ level }} lvl</div>
    </div>
  </div>
</template>

<script>
import { defineComponent, computed } from "vue";

export default defineComponent({
  name: "FriendItem",
  props: {
    name: {
      type: String,
      required: true,
      default: "unknown",
    },
    image: {
      type: String,
      required: false,
    },
    level: {
      type: Number,
      required: true,
      default: 1,
    },
    isMedal: {
      type: Boolean,
      required: true,
      default: false,
    },
  },
  setup(props) {
    const imageSrc = computed(
      () => props.image || require("@/assets/icon-question@2x.png")
    );

    return {
      imageSrc,
    };
  },
});
</script>

<style>
.friendsRow {
  align-self: stretch;
  height: 42px;
  background: radial-gradient(50% 50% at 50% 50%, #3081b4, #19488c);
  border-bottom: 1px solid transparent;
  border-image: linear-gradient(
    to right,
    rgba(167, 222, 253, 0) 0%,
    #a7defd 50%,
    rgba(167, 222, 253, 0) 100%
  );
  border-image-slice: 1;
  box-sizing: border-box;
  overflow-y: auto;
  flex-shrink: 0;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  padding: var(--padding-7xs) var(--padding-54xl) var(--padding-9xs)
    var(--padding-9xs);
  max-height: 440px;
  margin-bottom: 10px;
}
.friendsItems {
  height: 30px;
  box-shadow: 0px 1px 4px rgba(0, 174, 229, 0.5);
  border-radius: var(--br-9xs);
  background-color: var(--color-darkslateblue);
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-9xs);
  box-sizing: border-box;
}

.name {
  flex: 1;
  position: relative;
  padding-left: 10px;
  font-weight: 900;
  text-shadow:
    0.3px 0 0 #000,
    0 0.3px 0 #000,
    -0.3px 0 0 #000,
    0 -0.3px 0 #000;
}

.gamepads {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  font-size: var(--font-size-base);
}

.iconQuestion {
  height: 34px;
  width: 21px;
  position: relative;
  object-fit: cover;
}
.lvl {
  position: relative;
  font-weight: 900;
  text-shadow: var(--shadow-counter);
}

.unionIcon {
  height: 26px;
  width: 28px;
  position: relative;
}
</style>
