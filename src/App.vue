<template>
  <div id="app">
    <nav-bar />
    <full-page :options="options">
      <welcome id="home" class="section" />
      <projects
        v-for="project in projectsData"
        :key="project.id"
        :projectDetail="project"
        class="section"
      />
      <about class="section" />
      <contact class="section" />
    </full-page>
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Welcome from "./components/Welcome.vue";
import Projects from "./components/Projects.vue";
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";
import projectsData from "./assets/projects.json";
export default {
  name: "App",
  components: {
    NavBar,
    Welcome,
    Projects,
    About,
    Contact,
  },
  data() {
    return {
      projectsData,
      options: {
        menu: "#menu",
        anchors: [
          "home",
          "projects1",
          "projects2",
          "projects3",
          "about",
          "contact",
        ],
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
  transition: all 0.5s ease;
}
body {
  background-color: var(--main-blue);
}
.section {
  margin-left: 17%;
}
</style>
