<template >
  <v-container>
    <v-from>
      <v-card>
        <v-row>
          <v-simple-table>
            <tbody>
              <tr v-for="(item, index) in additem" :key="index">
                <td>{{ index + 1 }}</td>
                <td>{{ item.work }}</td>
                <td>
                  <v-btn @click="deleteTodo(index)" color="red accent-1"> Delete </v-btn>
                </td>
              </tr>
            </tbody>
          </v-simple-table>
        </v-row>
      </v-card>
    </v-from>
  </v-container>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["additem"],
  methods: {
    deleteTodo(index) {
      this.additem.splice(index, 1);
    },
  },
};
</script>

<style></style>