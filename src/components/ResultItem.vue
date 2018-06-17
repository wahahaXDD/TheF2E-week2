<template>
    <div class="result-card" :style="cardStyle" @mouseover="hover()" @mouseout="out()" @click="clicked()">
        <span><i>{{text}}</i></span>
        <font-awesome-icon :icon="['far','times-circle']" :style="iconStyle"/>
    </div>
</template>

<script>
import fontawesome from "@fortawesome/fontawesome";
import FontAwesomeIcon from "@fortawesome/vue-fontawesome";
import solid from "@fortawesome/fontawesome-free-solid";
import regular from "@fortawesome/fontawesome-free-regular";
import brands from "@fortawesome/fontawesome-free-brands";

fontawesome.library.add(solid);
fontawesome.library.add(regular);
fontawesome.library.add(brands);
export default {
  name: "result-item",
  components: {
    "font-awesome-icon": FontAwesomeIcon
  },
  props: ['text'],
  computed: {},
  data() {
    return {
      iconStyle: { color: "#9013FE" },
      cardStyle: { color: "#9013FE", backgroundColor: "transparent" }
    };
  },
  methods: {
    hover() {
      this.iconStyle.color = "white";
      this.cardStyle = {
        color: "white",
        backgroundColor: "#9013FE"
      };
    },
    out() {
      this.iconStyle.color = "#9013FE";
      this.cardStyle = { color: "#9013FE", backgroundColor: "transparent" };
    },
    clicked() {
      this.$emit("result-card-clicked");
    }
  }
};
</script>

<style lang="scss">
@import "../sass/custom-bootstrap";
@import "node_modules/bootstrap/scss/bootstrap.scss";
.result-card {
  display: inline-block;
  padding: 0.3rem 1rem;
  border: 1px solid $secondary;
  border-radius: 100px;
  cursor: pointer;
}
</style>
