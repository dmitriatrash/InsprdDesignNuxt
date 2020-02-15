<template>
  <div class="container">
    <div>
      <Header />
      <main class="pa4 black-80">
        <form class="measure center vh-50">
          <fieldset id="contact" class="ba b--transparent ph0 mh0">
            <legend class="f4 fw6 ph0 mh0">
              Contact us
            </legend>
            <div class="mt3">
              <label class="db fw6 lh-copy f6" for="name">Name</label>
              <input id="name" class="pa2 input-reset ba bg-transparent hover-bg-black hover-white w-100" type="text" name="name">
            </div>
            <div class="mt3">
              <label class="db fw6 lh-copy f6" for="email-address">Email</label>
              <input id="email-address" class="pa2 input-reset ba bg-transparent hover-bg-black hover-white w-100" type="email" name="email-address">
            </div>
            <div class="mt3">
              <label class="db fw6 lh-copy f6" for="phone">Phone</label>
              <input id="phone" class="pa2 input-reset ba bg-transparent hover-bg-black hover-white w-100" type="text" name="phone">
            </div>
            <div>
              <label for="comment" class="f6 b db mb2">Comments <span class="normal black-60">(optional)</span></label>
              <textarea id="comment" name="comment" class="pa2 input-reset ba bg-transparent hover-bg-black hover-white w-100 vh-25" aria-describedby="comment-desc" />
              <small id="comment-desc" class="f6 black-60">Helper text for a form control. Can use this text to <a href="#" class="link underline black-80 hover-blue">link to more info.</a></small>
            </div>
          </fieldset>
          <div class="submit">
            <input class="b ph3 pv2 input-reset ba b--black bg-transparent grow pointer f6 dib" type="submit" value="Send">
          </div>
        </form>
      </main>
    </div>
  </div>
</template>

<script>
/*
import Logo from '~/components/Logo.vue'
*/
import Header from '~/components/Header.vue'
export default {
  components: {
    Header
  }
}
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background-image: url("https://cdn.pixabay.com/photo/2017/01/18/15/51/paper-1990111_1280.jpg");
    background-size: cover;
  }
</style>
