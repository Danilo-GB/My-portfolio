<template>
  <div
    class="nav-bar flex flex-col justify-evenly md:justify-between fixed left-0 h-full w-1/6 py-4 md:py-8 z-10"
  >
    <div class="item">
      <a href="#home">
        <img src="../assets/LogoPersonal.svg" alt="logo" />
      </a>
    </div>
    <div class="item">
      <ul id="menu">
        <li v-for="anchor in anchors" :key="anchor" :data-menuanchor="anchor">
          <a :href="`#${anchor}`"></a>
        </li>
      </ul>
    </div>
    <div class="item">
      <a
        href="mailto:rubendanilo.garcia@gmail.com"
        target="_blank"
        rel="noopener noreferrer"
        ><img
          src="https://img.icons8.com/carbon-copy/100/ffffff/new-post.png" /></a
      ><a
        href="https://github.com/Danilo-GB"
        target="_blank"
        rel="noopener noreferrer"
        ><img
          src="https://img.icons8.com/carbon-copy/100/ffffff/github-squared.png" /></a
      ><a
        href="https://www.linkedin.com/in/danilogarciab/"
        target="_blank"
        rel="noopener noreferrer"
        ><img
          src="https://img.icons8.com/carbon-copy/100/ffffff/linkedin.png" /></a
      ><a
        href="https://www.instagram.com/_danilogb_/"
        target="_blank"
        rel="noopener noreferrer"
        ><img
          src="https://img.icons8.com/carbon-copy/100/ffffff/instagram-new--v2.png"
      /></a>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    anchors: {
      type: Array,
    },
  },
};
</script>
<style>
.nav-bar .item {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
#menu {
  position: relative;
  top: 25%;
}
#menu li {
  position: relative;
  width: 30%;
  height: 3px;
  margin: 1rem 20%;
}
#menu a {
  position: absolute;
  width: 30%;
  height: 100%;
  background-color: white;
}
#menu li.active a {
  width: 60%;
}
.item a img {
  margin: 0 auto;
  width: 45px;
  height: 45px;
}
@media (min-width: 768px) {
  .item a img {
    margin: 0 15%;
  }
}
.item a img:hover {
  width: 60px;
  height: 60px;
}
#menu {
  position: relative;
  top: 10%;
}
</style>
