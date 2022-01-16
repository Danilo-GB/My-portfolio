<template>
  <div id="app">
    <nav-bar />
    <full-page :options="options">
      <welcome class="section" />
      <projects class="section" />
      <projects class="section" />
      <projects class="section" />
      <contact class="section" />
    </full-page>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Welcome from "./components/Welcome.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
export default {
  name: "App",
  components: {
    NavBar,
    Welcome,
    Projects,
    Contact,
  },
  data() {
    return {
      options: {
        menu: "#menu",
        anchors: ["home", "projects1", "projects2", "projects3", "contact"],
      },
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&display=swap");
:root {
  --main-blue: #030c18;
  --complementary-blue: #072142;
  --main-red: #ff4d5a;
}
* {
  font-family: "Oswald", sans-serif;
  color: #fff;
  background-color: var(--main-blue);
}
.section {
  margin-left: 17%;
}
</style>
