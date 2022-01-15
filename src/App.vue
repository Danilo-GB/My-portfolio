<template>
  <div id="app">
    <full-page>
      <welcome class="section" />
      <projects class="section" />
      <contact class="section" />
    </full-page>
  </div>
</template>

<script>
import Welcome from "./components/Welcome.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
export default {
  name: "App",
  components: {
    Welcome,
    Projects,
    Contact,
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
}
</style>
