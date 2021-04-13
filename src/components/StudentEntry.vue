<template>
    <div class="student">
        <div class="col s12 m6">
            <div class="card blue-grey darken-1">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "StudentEntry",
    props: {
        id: Number,
        firstname: String,
        lastname: String,
        age: Number,
        phone: String
    }
};
</script>

<style scoped>

</style>