<template>
  <nav class="navbar navbar-expand-lg fixed-top">
    <slot name="nav-content">
      <h1 class="navbar-brand">
        <router-link class="homeLink" v-bind:to="'/'">
          TRAINSET<img id="logo" src="/static/trainset_logo.png" />
        </router-link>
      </h1>
      <h1 style="color:white;margin-right: 1rem;">+</h1>
      <a href="https://raphaelnussbaumer.com/GeoPressureR/">
        <img style="height:56px;" src="/static/logo_geopressurer_sm.png" />
      </a>
      <div class="navbar-nav ml-auto">
        <router-link class="nav-link" v-bind:to="'/help'">Help</router-link>
        <router-link class="nav-link" v-bind:to="'/license'">
          License
        </router-link>
      </div>
    </slot>
  </nav>
</template>

<script>
export default {
  name: "BaseNavbar"
};
</script>

<style scoped>
.navbar {
  background: #7e4c64;
}
>>> .nav-link,
.navbar-brand {
  color: #f4f4f4;
  cursor: pointer;
}
.nav-link {
  margin-right: 1em !important;
}
.nav-link:hover {
  background: #f4f4f4;
  color: #7e4c64;
}
.navbar-toggler {
  background: #fff !important;
}
.navbar-nav {
  float: right;
}
.homeLink {
  text-decoration: none;
  color: inherit;
}
.homeLink:hover {
  text-decoration: none;
  color: inherit;
}
#logo {
  max-height: 30px !important;
}
</style>
