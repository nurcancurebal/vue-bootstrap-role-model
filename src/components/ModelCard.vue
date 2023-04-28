<template>
  <b-card
    :title="modelName"
    :img-src="modelPic"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem"
    class="mb-2"
  >
    <b-card-text>
      {{ modelJob }} - {{ modelNationality }} - {{ modelBirthday }}
    </b-card-text>

    <b-card-text>
      {{ modelAbout }}
    </b-card-text>

    <div class="tagsClass">
      <b-card-text class="tagsText" v-for="(i, index) in tags" :key="index">
        #{{ i }}
      </b-card-text>
    </div>

    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
</template>

<script>
export default {
  props: {
    // this.modelName, this.modelJob, this.modelNationality,  this.modelPic, this.modelBirthday,  this.modelAbout,this.tags

    modelName: String,
    modelJob: String,
    modelNationality: String,
    modelPic: String,
    modelBirthday: String,
    modelAbout: String,
    tags: Array,
  },
  data() {
    return {};
  },
};
</script>


<style>
.tagsClass {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 15px;
}

.tagsText {
  background-color: #d5ede8;
  margin: 4px;
  font-size: 18px;
  font-family: calibri, sans-serif;
  padding: 2px 10px;
  box-shadow: 0 0 3px #0e9acd;
  border-radius: 18px;
}

.card-text:last-child {
  margin-bottom: 4px !important;
}
</style>