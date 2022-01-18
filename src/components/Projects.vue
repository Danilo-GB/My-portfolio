<template>
  <div>
    <div class="w-full h-5/6 mt-4 relative flex flex-col justify-center">
      <img
        :src="require(`../assets/${projectDetail.img}`)"
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
        <a
          class="see-more-button"
          :href="`https://${projectDetail.id}.netlify.app`"
          target="_blank"
          ref="noreferer noopener"
          >View website</a
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
  padding: 0.5rem 1rem;
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

.project-image {
  position: absolute;
  right: 0;
  top: calc(60% - 280px);
  width: 700px;
  height: 563px;
  z-index: -1;
  filter: saturate(150%);
  background-color: var(--complementary-blue);
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
  .project-image {
    top: 0;
    width: 80%;
    height: 50%;
  }
  .see-more-button {
    margin-left: auto;
    width: 8rem;
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
