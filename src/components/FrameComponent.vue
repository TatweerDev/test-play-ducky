<template>
  <div :class="$style.frameParent">
    <div :class="$style.frameWrapper">
      <div :class="$style.frameContainer">
        <div :class="$style.buttonsCurrencyWrapper">
          <button :class="$style.buttonsCurrency">
            <div :class="$style.border">
              <img :class="$style.uiIcon" alt="" src="/ui.svg" />
            </div>
            <div :class="$style.titleParent">
              <div :class="$style.title">more bonuses</div>
              <div :class="$style.currency">
                <div :class="$style.icons1212">
                  <img
                    :class="$style.dsaddasdas5Icon"
                    alt=""
                    src="../assets/dsaddasdas-5@2x.png"
                  />
                </div>
                <div :class="$style.title1">1</div>
              </div>
            </div>
            <div :class="$style.border1">
              <div :class="$style.border2">
                <div :class="$style.borderChild" />
              </div>
            </div>
          </button>
        </div>
      </div>
    </div>
    <div :class="$style.frameDiv">
      <div :class="$style.buttonsCurrencyParent">
        <button :class="$style.buttonsCurrency1">
          <div :class="$style.border">
            <img :class="$style.uiIcon" alt="" src="/ui.svg" />
          </div>
          <div :class="$style.titleGroup">
            <div :class="$style.title2">Referal link</div>
            <div :class="$style.currency1">
              <div :class="$style.icons1616">
                <img :class="$style.vectorIcon" alt="" src="/vector.svg" />
              </div>
              <div :class="$style.title3">Invite</div>
            </div>
          </div>
          <div :class="$style.border1">
            <div :class="$style.border5">
              <div :class="$style.borderItem" />
            </div>
          </div>
        </button>
        <div :class="$style.buttonsCurrency2">
          <div :class="$style.border">
            <img :class="$style.uiIcon" alt="" src="/ui.svg" />
          </div>
          <div :class="$style.titleGroup">
            <div :class="$style.title4">Referal link</div>
            <div :class="$style.currency2">
              <div :class="$style.icons1212">
                <img
                  :class="$style.vectorIcon1"
                  loading="lazy"
                  alt=""
                  src="../assets/vector-1.svg"
                />
              </div>
              <div :class="$style.title5">1</div>
            </div>
          </div>
          <div :class="$style.border1">
            <div :class="$style.border5">
              <div :class="$style.borderItem" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "FrameComponent",
});
</script>
<style module>
.uiIcon {
  width: 14px;
  position: relative;
  height: 14px;
  display: none;
}
.border {
  width: 10px;
  height: 30px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: center;
}
.title {
  height: 9px;
  position: relative;
  font-size: var(--font-size-xs);
  line-height: 20px;
  text-transform: capitalize;
  font-weight: 900;
  font-family: var(--font-movavi-grotesque);
  color: var(--m-white);
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-shadow:
    0.3px 0 0 #1f1f1f,
    0 0.3px 0 #1f1f1f,
    -0.3px 0 0 #1f1f1f,
    0 -0.3px 0 #1f1f1f;
}
.dsaddasdas5Icon {
  width: 12px;
  position: relative;
  height: 12px;
  object-fit: cover;
}
.icons1212 {
  width: 12px;
  height: 16px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-12xs);
  box-sizing: border-box;
}
.title1 {
  height: 7px;
  position: relative;
  font-size: var(--font-size-3xs);
  letter-spacing: 0.05em;
  line-height: 16px;
  text-transform: capitalize;
  font-weight: 900;
  font-family: var(--font-movavi-grotesque);
  color: var(--m-white);
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-shadow: var(--button-shadow);
}
.currency {
  display: none;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-9xs);
}
.titleParent {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  padding: 0px 0px var(--padding-11xs);
  gap: var(--gap-5xs);
}
.borderChild {
  width: 8.3px;
  position: relative;
  border-radius: 50%;
  background-color: var(--color-moccasin);
  height: 4.5px;
  transform: rotate(22.7deg);
}
.border2 {
  width: 10px;
  height: 9px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
}
.border1 {
  width: 10px;
  height: 30px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
}
.buttonsCurrency {
  cursor: pointer;
  border: none;
  padding: 0px var(--padding-9xs);
  background-color: transparent;
  height: 30px;
  box-shadow:
    0px 1px 1px rgba(0, 0, 0, 0.25),
    0px 2px 0px #ffeeba inset,
    0px -2px 0px #7a5d00 inset;
  border-radius: var(--br-xs);
  background: linear-gradient(180deg, #f7cb40, #ddad1c);
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  gap: var(--gap-9xs);
  min-height: 30px;
}
.buttonsCurrencyWrapper {
  width: 149px;
  backdrop-filter: blur(1px);
  height: 36px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.frameContainer {
  align-self: stretch;
  backdrop-filter: blur(1px);
  height: 40px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-3xs);
  box-sizing: border-box;
}
.frameWrapper {
  width: 160px;
  border-radius: var(--br-xs);
  height: 115px;
  overflow: hidden;
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  background-image: url("../assets/frame-2131329026@3x.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
}
.title2 {
  position: relative;
  font-size: var(--font-size-xs);
  line-height: 20px;
  text-transform: capitalize;
  font-weight: 900;
  font-family: var(--font-movavi-grotesque);
  color: var(--m-white);
  text-align: center;
  display: none;
  text-shadow:
    0.3px 0 0 #1f1f1f,
    0 0.3px 0 #1f1f1f,
    -0.3px 0 0 #1f1f1f,
    0 -0.3px 0 #1f1f1f;
}
.vectorIcon {
  width: 16px;
  position: relative;
  height: 16px;
}
.icons1616 {
  width: 12px;
  height: 16px;
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-12xs);
  box-sizing: border-box;
}
.title3 {
  height: 9px;
  position: relative;
  font-size: var(--font-size-xs);
  letter-spacing: 0.05em;
  line-height: 16px;
  text-transform: capitalize;
  font-weight: 900;
  font-family: var(--font-movavi-grotesque);
  color: var(--m-white);
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-shadow: var(--button-shadow);
}
.currency1 {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-9xs);
}
.titleGroup {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-5xs);
}
.borderItem {
  width: 8.3px;
  position: relative;
  border-radius: 50%;
  background-color: var(--color-lightblue);
  height: 4.5px;
  transform: rotate(22.7deg);
}
.border5 {
  width: 10px;
  height: 13px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
}
.buttonsCurrency1 {
  cursor: pointer;
  border: none;
  padding: 0px var(--padding-9xs);
  background-color: transparent;
  height: 30px;
  box-shadow:
    0px 1px 1px rgba(0, 0, 0, 0.25),
    0px 2px 0px #bee3ff inset,
    0px -2px 0px #155388 inset;
  border-radius: var(--br-xs);
  background: linear-gradient(180deg, #44a2e5, #2e7ec2);
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  gap: var(--gap-9xs);
  min-height: 30px;
}
.title4 {
  position: relative;
  line-height: 20px;
  text-transform: capitalize;
  font-weight: 900;
  display: none;
  text-shadow:
    0.3px 0 0 #1f1f1f,
    0 0.3px 0 #1f1f1f,
    -0.3px 0 0 #1f1f1f,
    0 -0.3px 0 #1f1f1f;
}
.vectorIcon1 {
  width: 16px;
  height: 16px;
  position: relative;
}
.title5 {
  position: relative;
  letter-spacing: 0.05em;
  line-height: 16px;
  text-transform: capitalize;
  font-weight: 900;
  display: none;
  text-shadow: var(--button-shadow);
}
.currency2 {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-9xs);
  font-size: var(--font-size-3xs);
}
.buttonsCurrency2 {
  box-shadow:
    0px 1px 1px rgba(0, 0, 0, 0.25),
    0px 2px 0px #bee3ff inset,
    0px -2px 0px #155388 inset;
  border-radius: var(--br-xs);
  background: linear-gradient(180deg, #44a2e5, #2e7ec2);
  height: 30px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-9xs);
  box-sizing: border-box;
  gap: var(--gap-9xs);
  min-height: 30px;
}
.buttonsCurrencyParent {
  width: 149px;
  backdrop-filter: blur(1px);
  height: 40px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: var(--gap-base);
}
.frameDiv {
  width: 160px;
  border-radius: var(--br-lg);
  height: 115px;
  overflow: hidden;
  flex-shrink: 0;
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  justify-content: center;
  padding: 0px var(--padding-9xs);
  box-sizing: border-box;
  background-image: url("../assets/frame-2131329169@3x.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
}
.frameParent {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: center;
  gap: var(--gap-xs);
  text-align: center;
  font-size: var(--font-size-xs);
  color: var(--m-white);
  font-family: var(--font-movavi-grotesque);
}
</style>
