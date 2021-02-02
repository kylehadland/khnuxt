<template>
  <div>
    <Nav />
    <b-container style="margin: 25px auto">
      <b-jumbotron>
    <Nuxt />
      </b-jumbotron>
    </b-container>
    <!-- <Footer /> -->
  </div>
</template>

<style>

h1 {
  margin-bottom: 2rem;
}

html, body {
  height: 500px;
}
html {
  background: rgb(38,38,38);
}
body {
  background: rgb(38,38,38);
  background: linear-gradient(360deg, rgba(38,38,38,1) 0%, rgba(9,9,121,1) 56%, rgba(0,212,255,1) 100%);
  background-repeat: no-repeat;
}

/* html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
} */
</style>
