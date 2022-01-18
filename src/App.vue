<template>
  <div id="app">
    <floating-shapes />
    <nav-bar :anchors="options.anchors" />
    <full-page :options="options">
      <welcome class="section" />
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
import FloatingShapes from "./components/FloatingShapes.vue";
import NavBar from "./components/NavBar.vue";
import Welcome from "./components/Welcome.vue";
import Projects from "./components/Projects.vue";
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";
import projectsData from "./assets/projects.json";
export default {
  name: "App",
  components: {
    FloatingShapes,
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
        anchors: ["home", "about", "contact"],
        scrollingSpeed: 500,
      },
    };
  },
  created() {
    this.projectsData.forEach((project, idx) => {
      this.options.anchors.splice(idx + 1, 0, project.id);
    });
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
  margin-right: 5%;
}
</style>
