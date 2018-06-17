<template>
  <div>
    <Nav></Nav>
    <div class="row">
      <SearchOption></SearchOption>
      <SearchResult></SearchResult>
    </div>
  </div>
</template>

<script>
import Nav from "./components/Nav";
import SearchOption from "./components/SearchOption";
import SearchResult from "./components/SearchResult";
export default {
  name: "app",
  components: {
    Nav,
    SearchOption,
    SearchResult
  },
  data() {
    return {};
  }
};
</script>

<style lang="scss">
.row {
  width: 100%;
  margin: 0 !important;
}
</style>
