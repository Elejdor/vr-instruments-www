<template>
  <div class="container-fluid">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#"></a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="container">
        <div class="d-flex">
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="/">PL</a>
              </li>
              <li class="nav-item">
                <a class="nav-link active" href="?lang=en">EN</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>

<style lang="scss">
$primary: #25408f;
$secondary: #8f5325;
$success: #3e8d63;
$info: #13101c;
$warning: #945707;
$danger: #d62518;
$light: #c4c4c4;
$dark: #343a40;

$body-bg: #343a40;
$body-color: #fff;

// @import '../node_modules/bootstrap/scss/bootstrap';
@import '../node_modules/bootstrap/scss/functions';
@import '../node_modules/bootstrap/scss/mixins';
@import '../node_modules/bootstrap/scss/variables';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 1.2rem;
}
</style>
