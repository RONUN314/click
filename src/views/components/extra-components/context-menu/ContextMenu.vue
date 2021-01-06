<template>

 <div>
  <div class="mt-5">
    
    <vs-tabs alignment="fixed">
      <vs-tab label="Invoice">
        <div><div>
      <vs-table pagination max-items="7" search :data="users">

     <template slot="thead">
      <vs-th sort-key="email">ID</vs-th>
      <vs-th sort-key="username">Customer name</vs-th>
      <vs-th sort-key="website">Price</vs-th>
      <vs-th sort-key="id">Type</vs-th>
      <vs-th sort-key="id">Status</vs-th>
 
    </template>
    <template slot-scope="{data}">
      <vs-tr :data="tr" :key="indextr" v-for="(tr, indextr) in data">

        <vs-td :data="data[indextr].id">
          {{ data[indextr].id }}
        </vs-td>
         <vs-td :data="data[indextr].customername">
          {{ data[indextr].customername }}
        </vs-td>

        <vs-td :data="data[indextr].price">
          {{ data[indextr].price }}
        </vs-td>

        <vs-td :data="data[indextr].type">
          {{ data[indextr].type }}
        </vs-td>
        <vs-td :data="data[indextr].status">
          {{ data[indextr].status }}
        </vs-td>
      </vs-tr>
    </template>
  </vs-table>
   </div></div>
      </vs-tab>
      <vs-tab label="Invoice already">
        <div> <vs-table   pagination max-items="7" search :data="users">

    <template slot="thead">
      <vs-th sort-key="email">ID</vs-th>
      <vs-th sort-key="username">Customer name</vs-th>
      <vs-th sort-key="website">Price</vs-th>
      <vs-th sort-key="id">Type</vs-th>
      <vs-th sort-key="id">Status</vs-th>
 
    </template>
    <template slot-scope="{data}">
      <vs-tr :data="tr" :key="indextr" v-for="(tr, indextr) in data">

        <vs-td :data="data[indextr].id">
          {{ data[indextr].id }}
        </vs-td>
         <vs-td :data="data[indextr].customername">
          {{ data[indextr].customername }}
        </vs-td>

        <vs-td :data="data[indextr].price">
          {{ data[indextr].price }}
        </vs-td>

        <vs-td :data="data[indextr].type">
          {{ data[indextr].type }}
        </vs-td>
        <vs-td :data="data[indextr].status">
          {{ data[indextr].status }}
        </vs-td>
      </vs-tr>
    </template>
  </vs-table></div>
      </vs-tab>
    </vs-tabs>
  </div>
 </div>
 </template>

<script>
export default {
  data() {
    return {
      selected: [],
      'tableList': [
        'vs-th: Component',
        'vs-tr: Component',
        'vs-td: Component',
        'thread: Slot',
        'tbody: Slot',
        'header: Slot'
      ],
      users: [
        {
          "id": 1,
          "customername": "Bret",
          "price": "100.000$",
          "type": "",
          "status": "",
        },
         {
          "id": 2,
          "customername": "Bret",
          "price": "100.000$",
          "type": "",
          "status": "",
        }, {
          "id": 3,
          "customername": "Bret",
          "price": "100.000$",
          "type": "",
          "status": "",
        }, {
          "id": 4,
          "customername": "Bret",
          "price": "100.000$",
          "type": "",
          "status": "",
        }, {
          "id": 5,
          "customername": "Bret",
          "price": "100.000$",
          "type": "",
          "status": "",
        }, {
          "id": 6,
          "customername": "Bret",
          "price": "100.000$",
          "type": "",
          "status": "",
        },
      ]
    }
  },
}
</script>      
<style lang="scss">
@import "@/assets/scss/vuexy/pages/loading.scss";
</style>
