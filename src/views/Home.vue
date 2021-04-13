<template>
  <div class="home">
    <AddStudent />
    <StudentList v-bind:students="students" v-on:delete="deleteItem" />
    <a class="btn-floating btn-large waves-effect waves-light add-button right">
      <i class="material-icons">add</i>
    </a>
  </div>
</template>

<script>
// @ is an alias to /src
import StudentList from "@/components/StudentList";
import AddStudent from "@/components/AddStudent";

export default {
  name: "Home",
  data() {
    return {
      students: [
        {
          id: 0,
          firstname: "Benjamin",
          lastname: "Bulis",
          age: 21,
          phone: "0664/3398741",
        },
        {
          id: 1,
          firstname: "Florian",
          lastname: "Medved",
          age: 22,
          phone: "0664/0012345",
        },
      ],
    };
  },
  components: {
    AddStudent,
    StudentList,
  },
  methods: {
    deleteItem(id) {
      let i = this.students.map((item) => item.id).indexOf(id);
      this.students.splice(i, 1);
      console.table(this.students);
    },
  },
};
</script>

<style scoped>
.add-button {
  color: #44b78b;
}
</style>
