<template>
  <div>
    <div class="w-11/12 h-5/6 relative flex flex-col justify-center">
      <div class="background-circle">
        <img
          src="../assets/brand-img-2.png"
          alt="PersonalImage"
          class="brand-img"
        />
      </div>
      <div class="branding-name">
        DANILO <br />
        GARCIA
      </div>
      <ul class="separator my-14">
        <li></li>
        <li></li>
      </ul>
      <div class="sub-branding">&#60; Fullstack web developer /&#62;</div>
      <div class="sub-branding">
        <a class="contact-button" href="#contact">Hire me!</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.branding-name {
  font-size: 5rem;
  letter-spacing: 1rem;
  text-shadow: 1px 1px rgba(0, 0, 0, 0.5);
}
.sub-branding {
  font-size: 2rem;
  text-shadow: 1px 1px rgba(0, 0, 0, 0.5);
}

.contact-button {
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
  overflow: hidden;
  z-index: -1;
  box-shadow: 0px 0px 0px 0px rgb(245, 245, 245),
    0px 0px 0px 80px rgba(7, 33, 66, 0.8),
    0px 0px 0px 160px rgba(7, 33, 66, 0.5),
    0px 0px 0px 240px rgba(7, 33, 66, 0.3),
    0px 0px 0px 320px rgba(7, 33, 66, 0.2),
    0px 0px 0px 400px rgba(7, 33, 66, 0.1);
}
.brand-img {
  position: absolute;
  left: 0;
  bottom: -1rem;
  filter: contrast(140%) drop-shadow(0 0 20px #f5f5f5);
  pointer-events: none;
}
/* RESPONSIVE */
@media (max-width: 768px) {
  #home {
    padding: 5rem;
  }
  .branding-name {
    margin-top: auto;
    font-size: 3rem;
    text-align: right;
  }
  .sub-branding {
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
  .brand-img {
    display: none;
  }
  .contact-button {
    margin-left: auto;
    width: 6rem;
  }
}
@media (max-width: 414px) {
  #home {
    padding: 2rem;
  }
  .branding-name {
    margin-top: auto;
    font-size: 2rem;
    text-align: right;
  }
  .sub-branding {
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

.contact-button:hover {
  background-color: #fff;
  color: var(--main-blue);
  letter-spacing: 0.1rem;
}
</style>
