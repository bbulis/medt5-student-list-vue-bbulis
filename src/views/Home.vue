<template>
  <div class="home">
    <AddStudent v-on:addStudent="addItem" />
    <StudentList v-bind:students="students" v-on:delete="deleteItem" />
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
      counter: 2,
    };
  },
  components: {
    AddStudent,
    StudentList,
  },
  methods: {
    addItem(object) {
      object.id = this.counter;
      this.counter += 1;
      this.students.push(object);
      console.table(this.students);
    },
    deleteItem(id) {
      let i = this.students.map((item) => item.id).indexOf(id);
      this.students.splice(i, 1);
      console.table(this.students);
    },
  },
};
</script>

<style scoped></style>
