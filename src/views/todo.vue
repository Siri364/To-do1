<template >
  <div >
    <todoo @Input="addTodo"></todoo>
    <deletee :additem="additem"></deletee>
  </div>
</template>


<script>
import todoo from "../components/todoo.vue";
import deletee from "../components/deletee.vue";
export default {
  data: () => ({
    additem: [],
  }),
  additem: "Input",
  methods: {
    addTodo(subject, work) {
      this.additem.push({
        work: subject + " " + work,
      });
    },
  },
  components: {
    todoo,deletee,
  },
};
</script>