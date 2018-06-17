<template>
  <div id="search-result">
    <div>
      <h4>Showing <span>15</span> results by...</h4>
      <ResultItem text="Koahsiung"></ResultItem>
      <ResultItem text="Entertainment"></ResultItem>
    </div>
    <div id="cards">
      <Card></Card>
      <Card></Card>
      <Card></Card>
      <Card></Card>
      <Card></Card>
      <Card></Card>
    </div>
  </div>
</template>

<script>
import ResultItem from "./ResultItem";
import Card from "./Card";
export default {
  name: "search-result",
  components: {
    ResultItem,
    Card
  },
  computed: {},
  data() {
    return {};
  },
  methods: {}
};
</script>

<style lang="scss">
@import "../sass/custom-bootstrap";
@import "node_modules/bootstrap/scss/bootstrap.scss";

#search-result {
  width: 70%;
  margin-top: 0.8em;
  h4 {
    span {
      font-weight: 600;
      color: $secondary;
    }
  }
}
</style>
