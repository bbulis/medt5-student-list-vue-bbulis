<template>
  <div class="row">
    <form class="col s12">
      <div class="row">
        <div class="input-field col s6">
          <input placeholder="Vorname" id="firstname" type="text" />
        </div>
        <div class="input-field col s6">
          <input placeholder="Nachname" id="lastname" type="text" />
        </div>
      </div>
      <div class="row">
        <div class="input-field col s6">
          <input placeholder="Alter" id="age" type="number" />
        </div>
        <div class="input-field col s6">
          <input placeholder="Telefonnumer" id="phone" type="text" />
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "AddStudent",
};
</script>

<style scoped></style>
