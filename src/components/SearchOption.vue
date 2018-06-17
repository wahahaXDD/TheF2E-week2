<template>
    <div id="search" class="col-3">
        <div id="loc" class="search-item">
            <div class="form-group">
                <h5>Location</h5>
                <select class="form-control" id="loc-select">
                    <option>Taiwan</option>
                    <option>Taiwan</option>
                    <option>Taiwan</option>
                    <option>Taiwan</option>
                    <option>Taiwan</option>
                </select>
            </div>
        </div>
        <div id="pick-date" class="search-item">
            <div class="form-group">
                <h5>Date</h5>
                <div class="date-input">
                    <label for="date-from">from</label>
                    <input class="form-control" type="date" value="2018-05-24" id="date-from">
                </div>
                <div class="date-input">
                    <label for="date-from">to</label>
                    <input class="form-control" type="date" value="2018-06-01" id="date-to">
                </div>
            </div>
        </div>
        <div id="cat" class="search-item">
            <div class="form-group">
                <h5>Categories</h5>
                <div class="form-check">
                    <label class="form-check-label">
                        <input type="checkbox" class="form-check-input" id="checkboxSuccess" value="option1">
                        All
                    </label>
                    <label class="form-check-label">
                        <input type="checkbox" class="form-check-input" id="checkboxSuccess" value="option1">
                        Entertainment
                    </label>
                    <label class="form-check-label">
                        <input type="checkbox" class="form-check-input" id="checkboxSuccess" value="option1">
                        Food
                    </label>
                    <label class="form-check-label">
                        <input type="checkbox" class="form-check-input" id="checkboxSuccess" value="option1">
                        Learning
                    </label>
                    <label class="form-check-label">
                        <input type="checkbox" class="form-check-input" id="checkboxSuccess" value="option1">
                        Outdoors
                    </label>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: "search-option",
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

#search {
  margin-left: 1.5em;
  padding-left: 0;
  padding-right: 3em;
  padding-bottom: 0.2rem;
  .form-group {
    width: 85%;
    h5 {
      font-weight: bold;
    }
  }
  .search-item {
    background-color: $gray-400;
    padding-top: 1.5em;
    padding-left: 2em;
    padding-bottom: 1em;
  }
  .search-item:nth-child(2) {
    border-top: 2px solid $gray-600;
    border-bottom: 2px solid $gray-600;
  }
  .date-input {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    margin-top: 10px;
    label {
      width: 19%;
      margin-right: 10px;
      text-align: right;
    }
  }
  .form-check-label {
    display: flex;
  }
}
</style>
