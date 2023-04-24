<template>
  <div>
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="4">
          <AddRoleModel />
        </b-col>
        <b-col sm="8"></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import AddRoleModel from "./components/AddRoleModel";

export default {
  components: {
    AddRoleModel,
  },
};
</script>

<style>
</style>
