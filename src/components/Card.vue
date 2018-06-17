<template>
<div class="card">
    <img src="https://khh.travel/FileArtPic.ashx?id=705&amp;w=1280&amp;h=960">
    <div class="card-des">
        <h4 class="title">Kogi Cosby sweater.</h4>
        <p class="describe">
            Donec euismod scelerisque ligula. Maecenas eu varius risus, eu aliquet arcu. Curabitur fermentum suscipit est, tincidunt mattis lorem luctus id. Donec eget massa a diam condimentum pretium. Aliquam erat volutpat. Integer ut tincidunt orci. Etiam tristique, elit ut consectetur iaculis, metus lectus mattis justo, vel mollis eros neque quis augue. Sed lobortis ultrices lacus, a placerat metus rutrum sit amet. Aenean ut suscipit justo.
        </p>
        <h5 class="category">
            Entertainment
        </h5>
        <div class="detail-info">
            <div class="place">
                <font-awesome-icon :icon="['fas','map-marker-alt']" size="lg"></font-awesome-icon>
                <h5>Kaohsiung City</h5>
            </div>
            <div class="activity-date">
                <font-awesome-icon :icon="['far','calendar-alt']" size="lg"></font-awesome-icon>
                <h5>2018/5/24 - 2018/5/31</h5>
            </div>
        </div>
    </div>
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
  name: "card",
  props: ['img-src','title','describe','cat','place','date'],
  components: {
    "font-awesome-icon": FontAwesomeIcon
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
.card {
  margin-top: 20px;
  margin-bottom: 20px;
  background-color: white;
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.15);
  flex-direction: row;
  img {
    max-width: 30%;
    border-radius: 0.25rem 0 0 0.25rem;
  }
  .card-des {
    padding-top: 15px;
    padding-left: 15px;
    .title {
      margin-bottom: 15px;
      font-weight: 700;
      color: $secondary;
    }
    .describe {
      height: 40%;
      width: 95%;
      margin-bottom: 15px;
      overflow: hidden;
    }
    .detail-info {
      display: flex;
      & > div {
        margin-right: 25px;
        display: flex;
        h5 {
          margin-left: 5px;
          color: $gray-800;
        }
      }
    }
    .category {
      display: inline-block;
      font-size: 16px;
      font-style: italic;
      font-weight: 600;
      color: white;
      padding: 3px 15px;
      background-color: $gray-600;
      border-radius: 100px;
      margin-bottom: 15px;
    }
  }
}
</style>
