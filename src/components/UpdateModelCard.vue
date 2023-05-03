<template>
  <div>
    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <b-form-input
        class="mt-2"
        v-model="modelName"
        placeholder="What is your role model name"
      ></b-form-input>

      <b-form-input
        class="mt-2"
        v-model="modelJob"
        placeholder="What is his job"
      ></b-form-input>

      <b-form-input
        class="mt-2"
        v-model="modelNationality"
        placeholder="What is his nationality"
      ></b-form-input>

      <b-form-input
        class="mt-2"
        v-model="modelPic"
        placeholder="Add his picture link"
      ></b-form-input>

      <label class="mt-3">Choose his birthday</label>
      <b-form-datepicker
        v-model="modelBirthday"
        class="mb-2"
      ></b-form-datepicker>

      <b-form-textarea
        class="mt-2"
        v-model="modelAbout"
        placeholder="Note about him..."
        rows="3"
        max-rows="6"
      ></b-form-textarea>

      <b-form-tags
        input-id="tags-basic"
        v-model="tags"
        class="mt-2"
      ></b-form-tags>

      <b-button class="mt-3" variant="outline-danger" block @click="hideModal"
        >Close Me</b-button
      >

      <b-button
        class="mt-2"
        variant="outline-warning"
        block
        @click="toggleModal"
        >Toggle Me</b-button
      >
    </b-modal>
  </div>
</template>

<script>
export default {
  props: {
    modelName: String,
    modelJob: String,
    modelNationality: String,
    modelPic: String,
    modelBirthday: String,
    modelAbout: String,
    tags: Array,
    index: Number,
  },
  methods: {
    showModal() {
      this.$refs["my-modal"].show();
    },
    hideModal() {
      this.$refs["my-modal"].hide();
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs["my-modal"].toggle("#toggle-btn");
      this.$emit("closeModel");
    },
    mounted() {
      this.showModal();
    },
  },
};
</script>