<template>
  <div class="row">
    <h3>Schüler hinzufügen</h3>
    <form class="col s12">
      <div class="row">
        <div class="input-field col s6">
          <input
            placeholder="Vorname"
            ref="firstname"
            id="firstname"
            type="text"
          />
        </div>
        <div class="input-field col s6">
          <input
            placeholder="Nachname"
            ref="lastname"
            id="lastname"
            type="text"
          />
        </div>
      </div>
      <div class="row">
        <div class="input-field col s6">
          <input placeholder="Alter" ref="age" id="age" type="number" />
        </div>
        <div class="input-field col s6">
          <input
            placeholder="Telefonnumer"
            ref="phone"
            id="phone"
            type="text"
          />
        </div>
      </div>
      <div class="row">
        <a
          class="btn-floating btn-large waves-effect waves-light add-button right"
          v-on:click="getFormValues"
        >
          <i class="material-icons">add</i>
        </a>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "AddStudent",
  data: function () {
    return {
      output: {
        id: 0,
        firstname: "",
        lastname: "",
        age: 0,
        phone: "",
      },
    };
  },
  methods: {
    getFormValues() {
      let vm = this;
      this.output.firstname = this.$refs.firstname.value;
      this.output.lastname = this.$refs.lastname.value;
      this.output.age = this.$refs.age.value;
      this.output.phone = this.$refs.phone.value;
      vm.$emit("addStudent", this.output);
    },
  },
};
</script>

<style scoped>
.add-button {
  color: #44b78b;
}
</style>
