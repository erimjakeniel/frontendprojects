<template>
  <v-container fluid>
    <v-data-table :headers="headers" :items="org">
    </v-data-table>

    
  </v-container>
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
        { text: "Address", value: "address",sortable: false, },
        { text: "Contact", value: "contact",sortable: false, },
        { text: "Action", value: "event" ,sortable: false,}
      ]
    };
  },

  methods: {
    addOrg() {
      var org = [];
      var event = "Birthday";
      this.axios
        .post("http://localhost:8000/retrieveOneEvent/"+ event,)
        .then(response => {
          console.log(response);
          var dataT = response.data;
          // this.org = dataT
          var counter = 0;

          for (counter; counter < dataT.length; counter++) {
            org.push({
              name: dataT[counter].name,
              address: dataT[counter].address,
              contact: dataT[counter].contact,
              event: dataT[counter].event
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