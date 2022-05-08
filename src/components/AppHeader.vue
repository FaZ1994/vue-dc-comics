<template>
  <header>
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="DC logo" />
    </div>
    <nav class="nav-bar">
      <ul>
        <li
          v-for="(item, index) in links"
          :key="index"
          :class="{ selected: item.active }"
        >
          {{ item.text }}
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      links: [
        {
          text: "Characters",
          link: "",
          active: false,
        },
        {
          text: "Comics",
          link: "",
          active: true,
        },
        {
          text: "Movies",
          link: "",
          active: false,
        },
        {
          text: "TV",
          link: "",
          active: false,
        },
        {
          text: "Games",
          link: "",
          active: false,
        },
        {
          text: "Collectibles",
          link: "",
          active: false,
        },
        {
          text: "Videos",
          link: "",
          active: false,
        },
        {
          text: "Fans",
          link: "",
          active: false,
        },
        {
          text: "News",
          link: "",
          active: false,
        },
        {
          text: "Shop",
          link: "",
          active: false,
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "./style/generals";
@import "./style/vars";

.nav-bar {
  ul {
    list-style: none;
    height: 100%;
    display: flex;
    justify-content: center;
    gap: 2em;

    li {
      line-height: 4.5em;
      height: 100%;
      text-transform: uppercase;
      cursor: pointer;
    }
  }
}

header {
  height: 10vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
 
 img {
    height: 3em;
  }
}

.selected {
  color: $blueDc;
  margin-bottom: 10px;
  border-bottom: 5px solid $blueDc;
}
</style>
