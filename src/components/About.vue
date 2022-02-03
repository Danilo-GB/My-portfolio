<template>
  <div>
    <div class="w-full h-full relative flex flex-col justify-start">
      <div class="section-name">ABOUT ME</div>

      <div class="flex flex-row w-full h-1/3 justify-center">
        <div class="w-1/4 title">WHO I AM</div>
        <div class="w-3/4 detail">
          Hi, I'm Danilo, Junior software developer and Telecommunications
          engineer student, passionate about Frontend and Backend,
          application of good practices and quality development, I love teamwork
          and always maintain a good work environment.
        </div>
      </div>
      <div class="flex flex-row w-full h-1/3 justify-center">
        <div class="w-1/4 title">PASSION</div>
        <div class="w-3/4 detail">
          <ul>
            <li>
              Frontend: My greatest field of experience, bringing to
              reality ui and ux designs with clean and readable code.
            </li>
            <li>
              Backend: My beginnings of programming with php and python,
              implementing connections with databases and generating api rest
              services.
            </li>
            <li>Chess: Yep, I love it but I'm not very good at playing it.</li>
          </ul>
        </div>
      </div>
      <div class="flex flex-row w-full h-1/3 justify-center">
        <div class="w-1/4 title">SKILL SET</div>
        <div class="w-3/4 detail flex flex-row justify-evenly">
          <div class="inline">
            <img
              width="50"
              height="50"
              src="https://img.icons8.com/color/48/000000/vue-js.png"
            />
          </div>
          <div class="inline">
            <img
              width="50"
              height="50"
              src="https://img.icons8.com/fluency/48/000000/laravel.png"
            />
          </div>
          <div class="inline">
            <img
              width="50"
              height="50"
              src="https://img.icons8.com/color/48/000000/mysql-logo.png"
            />
          </div>
          <div class="inline">
            <img
              width="50"
              height="50"
              src="https://img.icons8.com/color/48/000000/html-5--v1.png"
            />
          </div>
          <div class="inline">
            <img
              width="50"
              height="50"
              src="https://img.icons8.com/color/48/000000/css3.png"
            />
          </div>
          <div class="inline">
            <img
              width="50"
              height="50"
              src="https://img.icons8.com/color/48/000000/javascript--v1.png"
            />
          </div>
        </div>
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

<style scoped>
.section-name {
  font-size: 5rem;
  letter-spacing: 1rem;
  text-shadow: 10px 1px rgba(0, 0, 0, 0.5), 1px 1px rgba(0, 0, 0, 0.5);
}
.title {
  font-size: 2rem;
  text-align: center;
  margin: auto 0;
  border-bottom: 1px solid var(--main-red);
}
.detail {
  font-size: 1.1rem;
  font-weight: 300;
  padding: 3rem;
}
li {
  margin-bottom: 1rem;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .section-name {
    margin-top: auto;
    font-size: 3rem;
    text-align: right;
  }
  .title {
    font-size: 1rem;
    transform: rotate(-90deg);
  }
  .detail {
    font-size: 0.7rem;
    font-weight: 300;
    padding: 0 1rem;
    margin: auto 0;
    border-left: 1px solid var(--main-red);
  }
}
</style>
