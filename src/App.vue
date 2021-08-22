<template>
  <div id="nav">
    <!-- <router-link to="/">Home</router-link> | -->

    <div class="container">
        <div class="logo-container">
            <img src="https://res.cloudinary.com/mindset/image/upload/v1629629758/logo_vilxls.svg" alt="logo" class="logo">
        </div>
        <div class="hero-container">
            <img src="https://res.cloudinary.com/mindset/image/upload/v1629629758/hero-desktop_y9gcvm.jpg" alt="hero-desktop" class="hero-desktop">
            <img src="https://res.cloudinary.com/mindset/image/upload/v1629629758/hero-mobile_jdlrvp.jpg" alt="hero mobile" class="hero-mobile">
        </div>
        <div class="content-wrapper">
            <div class="desktop-logo">
                <img src="https://res.cloudinary.com/mindset/image/upload/v1629629758/logo_vilxls.svg" alt="logo" class="logo">
            </div>

            <div class="title">
                We're
            </div>
            <div class="coming-soon">
                Coming soon
            </div>
            <div class="description">
                Hello fellow shoppers! We're currently building our new fashion store. Add your email below to stay up-to-date with announcements and our launch deals
            </div>
            <form id="form">
                <div class="input-container">
                    <input type="email" name="email" id="email" placeholder="Email Address">
                    <img src="/images/icon-error.svg" alt="error-icon" class="danger-button" id="danger-button">
                    <button class="button" type="submit">
                        <img src="https://res.cloudinary.com/mindset/image/upload/v1629629758/icon-arrow_goabkf.svg" alt="arrow">
                    </button>
                </div>

                <div class="danger-text" id="danger-text">
                    Please provide a valid email
                </div>
            </form>
        </div>
    </div>

    <footer>
        <p class="attribution">
            Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. Coded by <a href="https://www.instagram.com/vanjregautham/">Gautham</a>.
        </p>
    </footer>
  </div>
  <!-- <router-view/> -->
</template>



<script>
export default {
  
  mounted (){

let email = document.getElementById("email");
let dangerIcon = document.getElementById("danger-button");
let dangerText = document.getElementById("danger-text");
let form = document.getElementById("form");

form.addEventListener("submit", (e) => {
    if (email.validity.typeMismatch) {
        e.preventDefault();
        dangerIcon.style.opacity = 1;
        dangerText.style.opacity = 1;

    } else {
        dangerIcon.style.opacity = 0;
        dangerText.style.opacity = 0;
    }
})

  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

/* #nav {
  padding: 30px;
} */

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}







/* lijhgfd */
.attribution {
            font-size: 11px;
            text-align: center;
        }
        
        .attribution a {
            color: hsl(228, 45%, 44%);
        }


.container {
  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
  height: 100vh;
}

.hero-container {
  display: flex;
}

.hero-desktop {
  width: 100%;
  min-width: 600px;
  margin-top: -10px
}

.hero-mobile {
  display: none;
  width: 100%;
}

.content-wrapper {
  background: url("https://res.cloudinary.com/mindset/image/upload/v1629629758/bg-pattern-desktop_lxcvgw.svg");
  background-size: cover;
  padding: 5em 2em 0 10em;
}

.desktop-logo {
  display: block;
  margin-top: -10px
}

.logo-container {
  display: none;
}

.logo {
  -o-object-fit: contain;
     object-fit: contain;
}

.title {
  margin: 2.5em 0 0 0;
  font-size: 3rem;
  font-weight: 300;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #ce9797;
  line-height: 1.2em;
}

.coming-soon {
  color: #413a3a;
  font-size: 3rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.3em;
  margin-bottom: 0.5em;
  width: 50%;
  line-height: 1.2em;
}

.description {
  color: #ce9797;
  width: 60%;
  min-width: 400px;
  line-height: 1.5em;
  margin-bottom: 2em;
}

form {
  width: 100%;
  position: relative;
}

.input-container {
  width: 65%;
  min-width: 400px;
}

#email {
  border: 1px solid #ce9797;
  border-radius: 50px;
  background: transparent;
  padding: 0.6em;
  margin-left: 0.2em;
  height: 50px;
  width: 70%;
  outline: none;
}

.danger-button {
  background: #f96262;
  position: absolute;
  height: 25px;
  width: 25px;
  border-radius: 50%;
  top: 20px;
  right: 63%;
  transition: 0.5s;
  opacity: 0;
}

.danger-text {
  font-size: 12px;
  font-weight: 600;
  color: #ce9797;
  padding: 0.8em 2rem;
  transition: 0.5s;
  opacity: 0;
}

.button {
  background: linear-gradient(135deg, #f8bfbf, #ee8c8c);
  height: 55px;
  border: none;
  border-radius: 50px;
  outline: none;
  width: 90px;
  transform: translate(-55%, 3px);
  box-shadow: 0 10px 30px -5px #ce9797;
  cursor: pointer;
}

input::-moz-placeholder {
  color: #ce9797;
}

input:-ms-input-placeholder {
  color: #ce9797;
}

input::placeholder {
  color: #ce9797;
}

.button:active {
  background: linear-gradient(135deg, #ffebeb, #fbb1b1);
}

@media screen and (max-width: 1000px) {
  .hero-desktop {
    min-width: 400px;
  }
}
@media screen and (max-width: 768px) {
  .container {
    height: initial;
    flex-direction: column;
  }

  .content-wrapper {
    padding: 0;
  }

  .logo-container {
    display: block;
  }

  .desktop-logo {
    display: none;
  }

  .logo {
    padding: 2em;
  }

  .title {
    font-size: 2.5rem;
    margin: 1.5em 0 0 0;
    text-align: center;
    width: 100%;
  }

  .hero-desktop {
    display: none;
  }

  .hero-mobile {
    display: block;
  }

  .coming-soon {
    width: 100%;
    font-size: 2.5rem;
    text-align: center;
    padding: 0.1em;
  }

  .description {
    text-align: center;
    font-size: 0.8rem;
    width: 100%;
    padding: 0 3.5em;
  }

  .input-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
  }

  .danger-button {
    top: 13px;
    right: 34%;
  }

  .danger-text {
    text-align: center;
  }

  .button {
    position: absolute;
    height: 50px;
    transform: translate(-55%);
    right: 0;
  }
}
@media screen and (max-width: 400px) {
  .button {
    position: relative;
    right: 0;
  }

  #email {
    padding: 0.8em;
    width: 60%;
  }
}/*# sourceMappingURL=style.css.map */


</style>
