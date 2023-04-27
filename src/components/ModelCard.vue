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
        {{ i }}
      </b-card-text>
    </div>

    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
</template>

<script>
export default {
  props: {},
  data() {
    return {
      modelName: "try one",
      modelJob: "Developer",
      modelNationality: "Canada",
      modelBirthday: "27/03/95",
      modelAbout: "try one",
      modelPic: "https://picsum.photos/600/300/?image=25",
      tags: [
        "one",
        "two",
        "one",
        "two",
        "one",
        "two",
        "one",
        "two",
        "one",
        "two",
      ],
    };
  },
};
</script>


<style>
.tagsClass {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.tagsText {
  background-color: aquamarine;
  margin: 6px 4px;
  font-size: 18px;
  font-family: Cambria, sans-serif;
  padding: 2px 3px;
  box-shadow: 0 0 2px mediumblue;
}
</style>