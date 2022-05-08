<template>
  <section class="cards">
    <div class="cardsContainer">
      <ul>
        <li v-for="(item, index) in cardsItems" :key="index">
          <img :src="item.icon" alt="" />
          <span>{{ item.text }}</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppNavCard",
  data() {
    return {
      cardsItems: [
        {
          icon: require("../assets/img/buy-comics-digital-comics.png"),
          text: "Digital comics",
        },
        {
          icon: require("../assets/img/buy-comics-merchandise.png"),
          text: "Dc merchandise",
        },
        {
          icon: require("../assets/img/buy-comics-shop-locator.png"),
          text:"Comic shop locator" ,
        },
        {
          icon: require("../assets/img/buy-comics-subscriptions.png"),
          text:  "Subscriptions",
        },
        {
          icon: require("../assets/img/buy-dc-power-visa.svg"),
          text: "Dc power visa",
        },
      ],
    };
  },
  props: {
    msg: String,
  },
};
</script>

<style lang="scss" scoped>
@import "./style/vars";
@import "./style/generals";
.cards {
  height: 8em;
  display: flex;
  align-items: center;
  background-color: $blueDc;
  color: $fontMain;
}
.cardsContainer {
  width: 80vw;
  margin: 0 auto;
  ul {
    display: flex;
    justify-content: space-around;
    li {
      display: flex;
      align-items: center;
      justify-content: space-around;
      gap: 1em;
      text-transform: uppercase;
    }
  }
  img {
    height: 50px;
    max-width: 50px;
  }
}
</style>
