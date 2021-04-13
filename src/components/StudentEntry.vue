<template>
  <li class="collection-item avatar item-style">
    <i class="material-icons circle">person</i>
    <span class="title">{{ student.firstname }} {{ student.lastname }}</span>
    <p>
      Alter: {{ student.age }} <br />
      Telefonnummer: {{ student.phone }}
    </p>
    <a v-on:click="$emit('delete', student.id)" class="secondary-content">
      <i class="material-icons">delete_forever</i>
    </a>
  </li>
</template>

<script>
export default {
  name: "StudentEntry",
  props: {
    student: Object,
  },
};
</script>

<style scoped>
span {
  font-size: 25px !important;
}

.item-style {
  padding: 20px;
}
</style>
