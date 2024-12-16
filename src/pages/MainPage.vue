<template>
  <div :class="$style.friendsRewardActive">
    <main :class="$style.frameParent">
      <section :class="$style.frameContainer">
        <div :class="$style.referralMessageParent">
          <div :class="$style.referralMessage">
            <h1 :class="$style.inviteFriends">invite friends!</h1>
            <h3 :class="$style.youAndYour">
              You and your friend will receive bonuses!
            </h3>
          </div>
          <FrameComponent />
          <div :class="$style.friendsListContentParent">
            <div :class="$style.friendsListContent">
              <h3 :class="$style.listOfYour">List of your friends</h3>
            </div>
            <div @click="handleClaimClick" :class="$style.friendItem">
              <div :class="$style.buttonsCurrency">
                <div :class="$style.border">
                  <img :class="$style.uiIcon" alt="" src="../assets/ui.svg" />
                </div>
                <div :class="$style.friendItemInfo">
                  <h3 :class="$style.title">Claim</h3>
                  <div :class="$style.currency">
                    <div :class="$style.icons1212">
                      <img
                        :class="$style.dsaddasdas5Icon"
                        loading="lazy"
                        alt=""
                        src="../assets//dsaddasdas-5-1@2x.png"
                      />
                    </div>
                    <div :class="$style.title1">12.5k</div>
                  </div>
                </div>
                <div :class="$style.border1">
                  <div :class="$style.border2">
                    <div :class="$style.borderChild" />
                  </div>
                </div>
              </div>
            </div>
            <div :class="$style.friendsContainer">
              <FriendItem
                v-for="(item, index) in friends"
                :key="index"
                :name="item.name"
                :level="item.level"
                :isMedal="item.isMedal"
              />
            </div>
          </div>
        </div>
      </section>
    </main>
    <div :class="$style.friendsRewardActiveItem" />
    <div :class="$style.friendsRewardActiveInner">
      <div :class="$style.frameChild" />
    </div>
    <div :class="$style.hover" />
    <div :class="$style.cardPopup">
      <ClaimRewards v-show="isPopupDisplayed" @onClick="handleClaimClick" />
    </div>
  </div>
</template>
<script>
import { defineComponent, ref } from "vue";
import FrameComponent from "../components/FrameComponent.vue";
import ClaimRewards from "../components/ClaimRewards.vue";
import FriendItem from "../components/FriendItem.vue";

export default defineComponent({
  name: "FriendsRewardActive",
  components: { FrameComponent, ClaimRewards, FriendItem },
  emits: ["onClick"],
  setup() {
    const isPopupDisplayed = ref(false); // Инициализация переменной состояния

    const handleClaimClick = () => {
      isPopupDisplayed.value = !isPopupDisplayed.value;
    };

    return {
      handleClaimClick,
      isPopupDisplayed,
    };
  },
  data() {
    return {
      friends: [
        { name: "Anastacia V", level: 1 },
        { name: "Anastacia V", level: 1 },
        { name: "Dmitro", level: 1 },
        { name: "Diana", level: 15 },
        { name: "Nikita", level: 99 },
        { name: "Nikita", level: 99 },
        { name: "Nikita", level: 99, isMedal: true },
        { name: "Nikita", level: 99, isMedal: true },
        { name: "Nikita", level: 99, isMedal: true },
      ],
    };
  },
});
</script>
<style module>
.friendsRewardActive {
  width: 100%;
  height: 100vh;
  position: relative;
  background: radial-gradient(50% 50% at 50% 50%, #41aee7, #054ba7);
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  padding: 0px 0px 25px;
  box-sizing: border-box;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  font-size: 13px;
  color: var(--m-white);
  font-family: var(--font-sf-pro-text);
}
.frameParent {
  align-self: stretch;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  gap: 23px;
  flex-shrink: 0;
  max-width: 100%;
}
.frameContainer {
  align-self: stretch;
  margin-top: 30px;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: flex-start;
  padding: 0px 7px;
  box-sizing: border-box;
  max-width: 100%;
  text-align: center;
  font-size: 24px;
  color: #facb46;
  font-family: var(--font-movavi-grotesque);
}
.referralMessageParent {
  flex: 1;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-xs);
  max-width: 100%;
}
.referralMessage {
  width: 302px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}
.inviteFriends {
  margin: 0;
  align-self: stretch;
  position: relative;
  font-size: inherit;
  text-transform: uppercase;
  font-weight: 900;
  font-family: inherit;
  text-shadow:
    1px 0 0 #1f1f1f,
    0 3px 0 #1f1f1f,
    -1px 0 0 #1f1f1f,
    0 -1px 0 #1f1f1f;
}
.youAndYour {
  margin: 0;
  width: 289px;
  position: relative;
  font-size: var(--font-size-sm);
  font-weight: 600;
  font-family: var(--font-lato);
  color: var(--m-white);
  display: inline-block;
  text-shadow: 0px 1px 0px #000;
}
.friendsListContentParent {
  align-self: stretch;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-9xs);
  font-size: var(--font-size-base);
  color: var(--m-white);
  font-family: var(--font-lato);
}
.friendsListContent {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: var(--padding-9xs) var(--padding-10xs);
}
.listOfYour {
  margin: 0;
  position: relative;
  font-size: inherit;
  font-weight: 900;
  font-family: inherit;
  text-shadow: var(--shadow-counter);
}
.friendItem {
  margin-bottom: 5px;
}
.buttonsCurrency {
  box-shadow:
    0px 1px 1px rgba(0, 0, 0, 0.25),
    0px 2px 0px #ffeeba inset,
    0px -2px 0px #7a5d00 inset;
  border-radius: var(--br-xs);
  background: linear-gradient(180deg, #f7cb40, #ddad1c);
  height: 30px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 0px var(--padding-9xs);
  box-sizing: border-box;
  min-height: 30px;
}
.border {
  width: 10px;
  height: 30px;
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
.title {
  margin: 0;
  height: 10px;
  position: relative;
  font-size: inherit;
  line-height: 20px;
  font-weight: 900;
  font-family: inherit;
  display: flex;
  align-items: center;
  justify-content: center;
  text-shadow: var(--button-shadow);
}
.currency {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: var(--gap-9xs);
  font-size: var(--font-size-3xs);
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
.dsaddasdas5Icon {
  width: 12px;
  height: 12px;
  position: relative;
  object-fit: cover;
}
.title1 {
  height: 7px;
  position: relative;
  letter-spacing: 0.05em;
  line-height: 16px;
  text-transform: capitalize;
  font-weight: 900;
  display: flex;
  align-items: center;
  justify-content: center;
  text-shadow: var(--button-shadow);
}
.friendsContainer {
  align-self: stretch;
  box-shadow: 0px 4px 4.5px rgba(0, 3, 6, 0.5) inset;
  border-radius: var(--br-xs) var(--br-xs) 0px 0px;
  background: radial-gradient(50% 50% at 50% 50%, #3081b4, #19488c);
  border-right: 1px solid var(--color-steelblue);
  border-bottom: 1px solid var(--color-steelblue);
  border-left: 1px solid var(--color-steelblue);
  box-sizing: border-box;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  max-height: 50vh;
  text-align: left;
  font-size: var(--font-size-3xs);
}
.cardPopup {
  align-self: stretch;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 0px 0px 24px;
  flex-shrink: 0;
  font-size: var(--font-size-xl);
  font-family: var(--font-movavi-grotesque);
}

.friendsRewardActiveInner {
  width: 100%;
  margin: 0 !important;
  position: absolute;
  right: 0px;
  bottom: 0px;
  left: 0px;
  background-color: #151e27;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: center;
  padding: 3.5px var(--padding-xl);
  box-sizing: border-box;
}

.frameChild {
  height: 5px;
  width: 110px;
  position: relative;
  border-radius: 2px;
  background-color: #6a6f75;
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
  height: 29px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
}
</style>
