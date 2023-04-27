<template>
  <div>
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="4">
          <AddRoleModel @fromAddRoleModel="updateCard($event)" />
        </b-col>
        <b-col sm="8">
          <ModelCard />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import globalComponents from "./components/globalComponents";

export default {
  components: {
    ...globalComponents,
  },

  data() {
    return {
      card: [],
    };
  },

  methods: {
    updateCard(e) {
      this.card.push(e);
      console.log(this.card);
    },
  },
};
</script>

<style>
</style>
