<template>
  <v-continer>
    <div c>
      <v-form v-model="valid" class="container col-md-8">
    <v-card >
      <v-row>
       <h1>HomeWork</h1>
      <v-col >
        <v-select
          v-model="subject"
          :items="items"
          label="รายการ"
          required
        ></v-select>
      </v-col>

      <v-col >
        <v-text-field
          v-model="work"
          label="work"
          required
        ></v-text-field>
      </v-col>

      <v-col >
        <v-btn
          :disabled="!valid"
          color="primary"
          class="mr-4"
          @click="addTodo"
        >
          Add
        </v-btn>
        <v-btn @click="clear"
        color="primary">
      clear
    </v-btn>
      </v-col>
    </v-row>
    </v-card>
  </v-form>
    </div>
  </v-continer>
  
</template>

<script>
export default {
  data() {
    return {
      valid: true,
      work: "",
      subject: null,
      items: ["วิชา Web", " วิชา SA", " วิชา ML", "อื่นๆ"],
    };

  },
  methods: {
    addTodo() {
      this.$emit("Input", this.subject, this.work);
    },
  },
};
</script>

<style>
.v-card{
  margin-top: 3rem;
  
}
</style>