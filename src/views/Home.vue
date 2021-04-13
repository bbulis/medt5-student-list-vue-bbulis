<template>
  <div class="home">
    <StudentList v-bind:students="students" />
  </div>
</template>

<script>
// @ is an alias to /src
import StudentList from "@/components/StudentList";

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
    StudentList,
  },
};
</script>
