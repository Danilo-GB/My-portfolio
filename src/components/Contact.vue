<template>
  <div>
    <div class="w-11/12 h-5/6 relative flex flex-col justify-center">
      <div class="branding-name">GET IN TOUCH</div>
      <ul class="separator my-5 md:my-14">
        <li></li>
        <li></li>
      </ul>
      <div>
        <form
          name="contact"
          class="text-black text-md"
          netlify
          netlify-honeypot="bot-field"
        >
          <input type="text" name="bot-field" hidden />
          <input
            type="text"
            name="name"
            placeholder="Enter Your Name"
            class="w-full md:w-1/3 h-16 px-4 py-2 block my-10 rounded-lg"
          />
          <input
            type="email"
            name="email"
            placeholder="Enter Your Email"
            class="w-full md:w-1/2 px-4 py-2 h-16 block my-10 rounded-lg"
          />
          <input
            type="textarea"
            name="message"
            placeholder="Enter Your message"
            class="w-full px-4 py-2 h-16 block my-10 rounded-lg"
          />
          <button
            type="submit"
            class="contact-button text-white cursor-pointer"
          >
            SEND
          </button>
        </form>
      </div>
    </div>
  </div>
</template>
