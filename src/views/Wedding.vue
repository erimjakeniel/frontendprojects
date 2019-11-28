<template>
  <v-data-table
    :headers="headers"
    :items="org"
    sort-by="calories"
    class="elevation-1"
    
  >
    <template v-slot:items.action="{ items }">
      <v-icon
        small
        class="mr-2"
        @click="editItem(items)"
      >
        mdi-login
      </v-icon>
      <v-icon
        small
        @click="deleteItem(items)"
      >
        delete
      </v-icon>
    </template>
    
  </v-data-table>
</template>
<script>
export default {
  data() {
    return {
      org: [],
      headers: [
        {
          text: "Name",
          align: "left",
          sortable: false,
          value: "name"
        },
        { text: "Address", value: "address", sortable: false },
        { text: "Contact", value: "contact", sortable: false },
        { text: "Action", value: "event", sortable: false }
      ]
    };
  },

  methods: {
    addOrg() {
      var org = [];
      var event = "wedding";
      this.axios
        .post("http://localhost:8000/retrieveOneEvent/" + event)
        .then(response => {
          console.log(response);
          var dataT = response.data;
          // this.org = dataT
          var counter = 0;

          for (counter; counter < dataT.length; counter++) {
            org.push({
              name: dataT[counter].name,
              address: dataT[counter].address,
              contact: dataT[counter].contact
            });
          }
          // console.log(org);
          this.org = org;
        })
        .catch(error => {
          console.log(error);
        });

      return org;
    }
  },
  mounted() {
    this.addOrg();
  }
};
</script>