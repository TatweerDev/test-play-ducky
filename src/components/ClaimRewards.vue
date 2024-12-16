<template>
  <div :class="$style.cardPopup">
    <div class="frameParent">
      <div class="frameGroup">
        <div class="unionWrapper" @click="handleClick">
          <img
            class="icon"
            style="
              width: 50px;
              height: 50px;
              display: block;
              margin: 0 0 0 auto;
            "
            alt=""
            src="../assets/union-3@2x.png"
          />
        </div>
        <h2 class="claimYourRewars">Claim your rewars</h2>
      </div>
      <img style="width: 100%" alt="" src="../assets/frame-2131329041@2x.png" />
      <footer :class="$style.rewardDescription">
        <div :class="$style.rewardTypes">
          <div :class="$style.rewardForNew">reward for new friends</div>
          <div :class="$style.soft">
            <img
              :class="$style.dsaddasdas5Icon1"
              alt=""
              src="../assets/dsaddasdas-5@2x.png"
            />
            <div :class="$style.emptyPlaceholder">12,200</div>
          </div>
        </div>
        <div :class="$style.rewardTypes">
          <div :class="$style.rewardForNew">reward for friends level-up</div>
          <div :class="$style.soft">
            <img
              :class="$style.dsaddasdas5Icon1"
              alt=""
              src="../assets/dsaddasdas-5-2@2x.png"
            />
            <div :class="$style.emptyPlaceholder">12,200</div>
          </div>
        </div>
        <div :class="$style.buttonsCurrency1">
          <div :class="$style.border3">
            <img :class="$style.uiIcon" alt="" src="../assets/ui.svg" />
          </div>
          <div :class="$style.friendItemInfo">
            <h3 :class="$style.title2">Take</h3>
            <div :class="$style.currency1">
              <img
                :class="$style.dsaddasdas5Icon1"
                alt=""
                src="../assets/dsaddasdas-5@2x.png"
              />
              <div :class="$style.title3">1</div>
            </div>
          </div>
          <div :class="$style.border4">
            <div :class="$style.border5">
              <div :class="$style.borderChild" />
            </div>
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ClaimRewards",
  emits: ["onClick"],
  setup(_, { emit }) {
    const handleClick = () => {
      emit("onClick");
    };

    return {
      handleClick,
    };
  },
});
</script>
<style module>
.cardPopup {
  position: fixed;
  top: 40px;
  box-shadow:
    0px -10px 30px #113e76,
    0px 30px 20.7px rgba(0, 0, 0, 0.25) inset,
    0px 3px 0px #63aded inset;
  border-radius: var(--br-2xl) var(--br-2xl) 0px 0px;
  background: linear-gradient(180deg, #124682, #0f2c5b);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 0px 0px 24px;
  gap: 27px;
  flex-shrink: 0;
  font-size: var(--font-size-xl);
  font-family: var(--font-movavi-grotesque);
  z-index: 10000;
}

.unionWrapper {
  align-self: stretch;
  height: 25px;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: flex-end;
  padding: 0px 0px 0px;
  box-sizing: border-box;
}
.claimYourRewars {
  margin: 0;
  width: 255px;
  color: #facb46 !important;
  position: relative;
  font-size: 30px;
  text-transform: uppercase;
  font-weight: 400;
  font-family: inherit;
  display: inline-block;
  text-shadow:
    1px 0 0 #1f1f1f,
    0 1px 0 #1f1f1f,
    -1px 0 0 #1f1f1f,
    0 -1px 0 #1f1f1f;
}
.frameGroup {
  align-self: stretch;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}

.frameParent {
  align-self: stretch;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  gap: var(--gap-3xs);
  text-align: center;
  font-size: var(--font-size-9xl);
  color: var(--color-gold-100);
  font-family: var(--font-changa-one);
}

.rewardTypes {
  align-self: stretch;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  padding: 10px;
  font-weight: 200;
}
.rewardDescription {
  margin: 20px 10px;
  align-self: stretch;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  text-align: left;
  font-size: var(--font-size-xs);
  color: var(--m-white);
  font-family: var(--font-lato);
}

.rewardForNew {
  display: block;
  flex: 1;
  position: relative;
  text-transform: uppercase;
  font-weight: 500;
  text-shadow: 0px 2px 0px rgba(0, 0, 0, 0.5);
}

.soft {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  padding: 0px var(--padding-lgi) 0px 0px;
  gap: var(--gap-9xs);
  font-size: var(--font-size-sm);
  font-family: var(--font-movavi-grotesque);
}

.buttonsCurrency1 {
  box-shadow:
    0px 1px 1px rgba(0, 0, 0, 0.25),
    0px 2px 0px #ffeeba inset,
    0px -2px 0px #7a5d00 inset;
  border-radius: var(--br-lg);
  background: linear-gradient(180deg, #facf45, #d5a512);
  height: 40px;
  width: 150px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 0px 8px;
  box-sizing: border-box;
  gap: var(--gap-2xs);
  min-height: 30px;
  margin: 20px auto;
}

.border3 {
  width: 10px;
  height: 40px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: center;
}
.uiIcon {
  width: 14px;
  position: relative;
  height: 14px;
  display: none;
}

.friendItemInfo {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-5xs);
}

.dsaddasdas5Icon1 {
  height: 20px;
  width: 20px;
  position: relative;
  object-fit: cover;
}

.title2 {
  margin: 0;
  position: relative;
  font-size: 20px;
  font-weight: 900;
  line-height: 20px;
  font-family: inherit;
  text-shadow: var(--button-shadow);
  padding-bottom: 5px;
}

.currency1 {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-9xs);
}

.border5 {
  width: 10px;
  height: 10px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
}

.title3 {
  font-size: 18px;
  text-shadow: var(--button-shadow);
}

h2 {
  margin: 0 0 20px 0;
  color: #facb46 !important;
  font-size: 30px;
  text-transform: uppercase;
  font-weight: 400;
  font-family: inherit;
  display: inline-block;
  text-shadow:
    1px 0 0 #1f1f1f,
    0 1px 0 #1f1f1f,
    -1px 0 0 #1f1f1f,
    0 -1px 0 #1f1f1f;
}
</style>
