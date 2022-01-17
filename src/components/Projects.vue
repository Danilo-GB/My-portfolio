<template>
  <div>
    <div id="home" class="w-full h-full relative flex flex-col justify-center">
      <div class="background-circle"></div>
      <img
        :src="`/img/${projectDetail.img}`"
        alt="Project image"
        class="project-image"
      />
      <div class="project-name">{{ projectDetail.name }}</div>
      <ul class="separator my-14">
        <li></li>
        <li></li>
      </ul>
      <div class="project-detail">{{ projectDetail.type }}</div>
      <div class="project-detail">
        <a class="see-more-button" href="mailto:rubendanilo.garcia@gmail.com"
          >See more</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    projectDetail: {
      type: Object,
    },
  },
};
</script>

<style>
.project-name {
  font-size: 5rem;
  letter-spacing: 1rem;
  text-shadow: 10px 1px rgba(0, 0, 0, 0.5), 1px 1px rgba(0, 0, 0, 0.5);
}
.project-detail {
  font-size: 1.3rem;
  text-shadow: 1px 1px rgba(0, 0, 0, 0.5);
}

.see-more-button {
  display: block;
  width: 10rem;
  padding: 0.5rem 0.5rem;
  border-radius: 1rem;
  margin-top: 3rem;
  text-align: center;
  background-color: var(--main-red);
}
.separator {
  width: 150px;
  height: 20px;
}

.separator li:nth-child(1) {
  float: left;
  width: 75%;
  height: 5px;
  border-radius: 10px;
  background-color: var(--main-red);
}

.separator li:nth-child(2) {
  float: right;
  width: 75%;
  height: 5px;
  border-radius: 10px;
  margin: 10px 0;
  background-color: var(--main-red);
}

.background-circle {
  position: absolute;
  top: calc(8rem);
  right: -10rem;
  width: 60%;
  height: 40rem;
  background-color: rgba(7, 33, 66, 1);
  border-radius: 40rem;
  z-index: -1;
  box-shadow: 0px 0px 0px 0px rgb(245, 245, 245),
    0px 0px 0px 80px rgba(7, 33, 66, 0.8),
    0px 0px 0px 160px rgba(7, 33, 66, 0.5),
    0px 0px 0px 240px rgba(7, 33, 66, 0.3),
    0px 0px 0px 320px rgba(7, 33, 66, 0.2),
    0px 0px 0px 400px rgba(7, 33, 66, 0.1);
}
.project-image {
  position: absolute;
  right: 4rem;
  top: calc(50% - 280px);
  width: 700px;
  height: 563px;
  z-index: -1;
  filter: saturate(180%) contrast(120%);
  object-fit: contain;
}
/* RESPONSIVE */
@media (max-width: 768px) {
  .project-name {
    margin-top: auto;
    font-size: 3rem;
    text-align: right;
  }
  .project-detail {
    font-size: 1rem;
    text-align: right;
  }

  .separator {
    width: 100px;
    height: 20px;
    margin-left: auto;
  }
  .background-circle {
    top: 0;
    right: -10rem;
    width: 50%;
    height: 40rem;
  }
  .project-image {
    top: 0;
    width: 80%;
    height: 50%;
  }
  .see-more-button {
    margin-left: auto;
    width: 6rem;
  }
}
@media (max-width: 414px) {
  #home {
    padding: 2rem;
  }
  .project-name {
    margin-top: auto;
    font-size: 2rem;
    text-align: right;
  }
  .project-detail {
    font-size: 1rem;
    text-align: right;
  }

  .separator {
    width: 100px;
    height: 20px;
    margin-left: auto;
  }
}
/* ANIMATIONS */

.see-more-button:hover {
  background-color: #fff;
  color: var(--main-blue);
  letter-spacing: 0.1rem;
}
</style>
