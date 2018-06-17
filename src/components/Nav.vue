<template>
  <nav class="navbar navbar-expand-lg navbar-lightht">
    <div class="col-3">
      <a class="navbar-brand" href="#">
        <img src="../assets/logo.png" alt="">
      </a>
    </div>
    <div class="col-9">
      <div id="navbarSupportedContent">
        <form class="form-inline my-2 my-lg-0">
          <div class="input-group">
            <div class="input-group-prepend" :class="{active:isActive}">
              <font-awesome-icon :icon="icon" size="lg" style="color:white;margin-right:5px;margin-bottom:5px;"/>
            </div>
            <input type="text" class="form-control" placeholder="Explore your own activities" aria-label="" aria-describedby="basic-addon1" @focus="bgwhite()" @focusout="bgwhite()">
          </div>
        </form>
      </div>
    </div>
  </nav>
</template>

<script>
import FontAwesomeIcon from "@fortawesome/vue-fontawesome";
import faSearch from "@fortawesome/fontawesome-free-solid/faSearch";
export default {
  name: "nav",
  components: { FontAwesomeIcon },
  computed: {
    icon() {
      return faSearch;
    }
  },
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    bgwhite() {
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style lang="scss">
@import "../sass/custom-bootstrap";
@import "node_modules/bootstrap/scss/bootstrap.scss";
nav {
  background-color: $primary;
  &.navbar {
    padding-top: 1.2rem;
    padding-bottom: 1.5rem;
    padding-left: 1.5rem;
  }
  a {
    color: white;
  }
  .input-group {
    border-bottom: 1px solid white;
  }
  input.form-control {
    background-color: transparent;
    color: rgba(255, 255, 255, 0.7);
    border: 0px;
  }
  .input-group-prepend {
    align-items: flex-end;
  }
  .input-group-prepend.active {
    background-color: rgba(255, 255, 255, 0.7);
  }
}
</style>
