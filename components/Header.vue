<template>
  <div id="header" class="header">
    <nav class="db dt-l w-100 border-box pa3">
      <a class="db dtc-l v-mid mid-gray link dim w-100 w-25-l tc tl-l mb2 mb0-l logo-link" href="/" title="Home">
        <img src="../assets/images/insprd11-11.svg" class="dib w2 h2 br-100 nameIcon" alt="Site Name">
      </a>
      <div class="outer-menu">
        <input class="checkbox-toggle" type="checkbox">
        <div class="hamburger">
          <div />
        </div>
        <div class="menu">
          <div>
            <div>
              <ul>
                <li><a href="/">Home</a></li>
                <li><a href="#">Portfolio</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">About</a></li>
                <li><a href="/contact">Contact</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<style scoped>
  .logo-link{
    width: 100px;
  }
  .nameIcon{
    width: 100px;
    height: 100px;
  }
  .header{
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    padding: 10px;
  }
  a,
  a:visited,
  a:hover,
  a:active {
    color: inherit;
    text-decoration: none;
  }
  .outer-menu {
    position: fixed;
    top: 5vh;
    right: 10vh;
    z-index: 1;
  }
  .outer-menu .checkbox-toggle {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 2;
    cursor: pointer;
    width: 60px;
    height: 60px;
    opacity: 0;
  }
  .outer-menu .checkbox-toggle:checked + .hamburger > div {
    -webkit-transform: rotate(135deg);
    transform: rotate(135deg);
  }
  .outer-menu .checkbox-toggle:checked + .hamburger > div:before,
  .outer-menu .checkbox-toggle:checked + .hamburger > div:after {
    top: 0;
    -webkit-transform: rotate(90deg);
    transform: rotate(90deg);
  }
  .outer-menu .checkbox-toggle:checked + .hamburger > div:after {
    opacity: 0;
  }
  .outer-menu .checkbox-toggle:checked ~ .menu {
    pointer-events: auto;
    visibility: visible;
  }
  .outer-menu .checkbox-toggle:checked ~ .menu > div {
    -webkit-transform: scale(1);
    transform: scale(1);
    -webkit-transition-duration: 0.75s;
    transition-duration: 0.75s;
  }
  .outer-menu .checkbox-toggle:checked ~ .menu > div > div {
    opacity: 1;
    -webkit-transition: opacity 0.4s ease 0.4s;
    transition: opacity 0.4s ease 0.4s;
  }
  .outer-menu .checkbox-toggle:hover + .hamburger {
    box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.1);
  }
  .outer-menu .checkbox-toggle:checked:hover + .hamburger > div {
    -webkit-transform: rotate(225deg);
    transform: rotate(225deg);
  }
  .outer-menu .hamburger {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 60px;
    height: 60px;
    padding: 0.5em 1em;
    background: rgba(18, 18, 18, 0.75);
    border-radius: 0 0.12em 0.12em 0;
    cursor: pointer;
    -webkit-transition: box-shadow 0.4s ease;
    transition: box-shadow 0.4s ease;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    display: -webkit-box;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
  }
  .outer-menu .hamburger > div {
    position: relative;
    -webkit-box-flex: 0;
    flex: none;
    width: 100%;
    height: 2px;
    background: #FEFEFE;
    -webkit-transition: all 0.4s ease;
    transition: all 0.4s ease;
    display: -webkit-box;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
  }
  .outer-menu .hamburger > div:before,
  .outer-menu .hamburger > div:after {
    content: '';
    position: absolute;
    z-index: 1;
    top: -10px;
    left: 0;
    width: 100%;
    height: 2px;
    background: inherit;
    -webkit-transition: all 0.4s ease;
    transition: all 0.4s ease;
  }
  .outer-menu .hamburger > div:after {
    top: 10px;
  }
  .outer-menu .menu {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    visibility: hidden;
    overflow: hidden;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    outline: 1px solid transparent;
    display: -webkit-box;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
  }
  .outer-menu .menu > div {
    width: 200vw;
    height: 200vw;
    color: #FEFEFE;
    background: #aaaaaadb;
    border-radius: 50%;
    -webkit-transition: all 0.4s ease;
    transition: all 0.4s ease;
    -webkit-box-flex: 0;
    flex: none;
    -webkit-transform: scale(0);
    transform: scale(0);
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    overflow: hidden;
    display: -webkit-box;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
  }
  .outer-menu .menu > div > div {
    text-align: center;
    max-width: 90vw;
    max-height: 100vh;
    opacity: 0;
    -webkit-transition: opacity 0.4s ease;
    transition: opacity 0.4s ease;
    overflow-y: auto;
    -webkit-box-flex: 0;
    flex: none;
    display: -webkit-box;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
  }
  .outer-menu .menu > div > div > ul {
    list-style: none;
    padding: 0 1em;
    margin: 0;
    display: block;
    max-height: 100vh;
  }
  .outer-menu .menu > div > div > ul > li {
    padding: 0;
    margin: 1em;
    font-size: 24px;
    display: block;
  }
  .outer-menu .menu > div > div > ul > li > a {
    position: relative;
    display: inline;
    cursor: pointer;
    -webkit-transition: color 0.4s ease;
    transition: color 0.4s ease;
  }
  .outer-menu .menu > div > div > ul > li > a:hover {
    color: #e5e5e5;
  }
  .outer-menu .menu > div > div > ul > li > a:hover:after {
    width: 100%;
  }
  .outer-menu .menu > div > div > ul > li > a:after {
    content: '';
    position: absolute;
    z-index: 1;
    bottom: -0.15em;
    left: 0;
    width: 0;
    height: 2px;
    background: #e5e5e5;
    -webkit-transition: width 0.4s ease;
    transition: width 0.4s ease;
  }
</style>
