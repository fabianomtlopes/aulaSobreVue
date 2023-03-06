
<template>
  <div>
    <v-col cols="12">
      <v-text-field
        v-model="campoInput"
        label="Qual sua tarefa?"
        outlined
        clearable
        @keyup.enter="handleAddTarefa"
      ></v-text-field>
    </v-col>
  </div>
</template>

<script>
export default {
    data() {
    return {
      campoInput: null,
    };
  },
   methods: {
    handleAddTarefa() {
      // this.$store.commit("adicionaTarefa", this.campoInput);
      //quando se trabalha com actions se usa dispatch para atulizar em tempo real os dados.
      this.$store.dispatch("adicionaTarefa", this.campoInput);
      this.campoInput = null;
    },
  },
};
</script>

<style>
</style>