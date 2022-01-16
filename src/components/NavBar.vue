<template>
  <div
    class="nav-bar flex flex-col justify-between items-center fixed left-0 h-full w-1/6 py-4 md:py-8 z-10"
  >
    <div class="item text-xl text-center">Danilo Garcia</div>
    <div class="item">
      <ul id="menu">
        <li data-menuanchor="home" class="active">
          <a href="#home"></a>
        </li>
        <li data-menuanchor="projects1"><a href="#projects1"></a></li>
        <li data-menuanchor="projects2"><a href="#projects2"></a></li>
        <li data-menuanchor="projects3"><a href="#projects3"></a></li>
        <li data-menuanchor="contact"><a href="#contact"></a></li>
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

<style>
.nav-bar .item {
  width: 100%;
  height: 33%;
}

#menu li {
  position: relative;
  width: 30%;
  height: 3px;
  margin: 30px 20%;
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
  width: 50px;
  height: 50px;
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
</style>
