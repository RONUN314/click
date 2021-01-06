
<template>

 <div>
  <div class="mt-5">
    
    <vs-tabs alignment="fixed">
      <vs-tab label="Quotation">
        <div><div>
      <vs-table multiple v-model="selected" pagination max-items="7" search :data="users">

    <template slot="thead">
      <vs-th sort-key="email">ID</vs-th>
      <vs-th sort-key="username">Contact person</vs-th>
      <vs-th sort-key="website">Product name</vs-th>
      <vs-th sort-key="id">Email</vs-th>
      <vs-th sort-key="id">Tel</vs-th>
      <vs-th sort-key="id">Status</vs-th>
      <vs-th sort-key="id">Price</vs-th>
      <vs-th sort-key="id">Start date</vs-th>
      <vs-th sort-key="id">End date</vs-th>

    </template>
    <template slot-scope="{data}">
      <vs-tr :data="tr" :key="indextr" v-for="(tr, indextr) in data">

        <vs-td :data="data[indextr].id">
          {{ data[indextr].id }}
        </vs-td>
         <vs-td :data="data[indextr].contactperson">
          {{ data[indextr].contactperson }}
        </vs-td>

        <vs-td :data="data[indextr].productname">
          {{ data[indextr].productname }}
        </vs-td>

        <vs-td :data="data[indextr].email">
          {{ data[indextr].email }}
        </vs-td>
        <vs-td :data="data[indextr].tel">
          {{ data[indextr].tel }}
        </vs-td>
          <vs-td :data="data[indextr].status">
          {{ data[indextr].status }}
        </vs-td>

        <vs-td :data="data[indextr].price">
          {{ data[indextr].price }}
        </vs-td>
        <vs-td :data="data[indextr].startdate">
          {{ data[indextr].startdate }}
        </vs-td>
        <vs-td :data="data[indextr].enddate">
          {{ data[indextr].enddate }}
        </vs-td>

      </vs-tr>
    </template>
  </vs-table>
   </div></div>
      </vs-tab>
      <vs-tab label="Quotation already">
        <div> <vs-table multiple v-model="selected" pagination max-items="7" search :data="users">

    <template slot="thead">
      <vs-th sort-key="email">ID</vs-th>
      <vs-th sort-key="username">Contact person</vs-th>
      <vs-th sort-key="website">Product name</vs-th>
      <vs-th sort-key="id">Email</vs-th>
      <vs-th sort-key="id">Tel</vs-th>
      <vs-th sort-key="id">Status</vs-th>
      <vs-th sort-key="id">Price</vs-th>
      <vs-th sort-key="id">Start date</vs-th>
      <vs-th sort-key="id">End date</vs-th>

    </template>
    <template slot-scope="{data}">
      <vs-tr :data="tr" :key="indextr" v-for="(tr, indextr) in data">

        <vs-td :data="data[indextr].id">
          {{ data[indextr].id }}
        </vs-td>
         <vs-td :data="data[indextr].contactperson">
          {{ data[indextr].contactperson }}
        </vs-td>

        <vs-td :data="data[indextr].productname">
          {{ data[indextr].productname }}
        </vs-td>

        <vs-td :data="data[indextr].email">
          {{ data[indextr].email }}
        </vs-td>
        <vs-td :data="data[indextr].tel">
          {{ data[indextr].tel }}
        </vs-td>
          <vs-td :data="data[indextr].status">
          {{ data[indextr].status }}
        </vs-td>

        <vs-td :data="data[indextr].price">
          {{ data[indextr].price }}
        </vs-td>
        <vs-td :data="data[indextr].startdate">
          {{ data[indextr].startdate }}
        </vs-td>
        <vs-td :data="data[indextr].enddate">
          {{ data[indextr].enddate }}
        </vs-td>

      </vs-tr>
    </template>
  </vs-table></div>
      </vs-tab>
    </vs-tabs>
  </div>
  <vs-button @click="$router.push('/apps/calendar/vue-simple-calendar')" type="filled" >Product</vs-button>
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
          "contactperson": "Leanne Graham",
          "productname": "Bret",
          "email": "Sincere@april.biz",
          "tel": "02058788888",
          "status": "",
          "price": "50.000$",
          "startdate": "17/10/2020",
          "enddate": "02/01/2021",
        },
       {
          "id": 1,
          "contactperson": "Leanne Graham",
          "productname": "Bret",
          "email": "Sincere@april.biz",
          "tel": "02058788888",
          "status": "",
          "price": "50.000$",
          "startdate": "17/10/2020",
          "enddate": "02/01/2021",
        }, {
          "id": 2,
          "contactperson": "Leanne Graham",
          "productname": "Bret",
          "email": "Sincere@april.biz",
          "tel": "02058788888",
          "status": "",
          "price": "50.000$",
          "startdate": "17/10/2020",
          "enddate": "02/01/2021",
        }, {
          "id": 3,
          "contactperson": "Leanne Graham",
          "productname": "Bret",
          "email": "Sincere@april.biz",
          "tel": "02058788888",
          "status": "",
          "price": "50.000$",
          "startdate": "17/10/2020",
          "enddate": "02/01/2021",
        }, {
          "id": 4,
          "contactperson": "Leanne Graham",
          "productname": "Bret",
          "email": "Sincere@april.biz",
          "tel": "02058788888",
          "status": "",
          "price": "50.000$",
          "startdate": "17/10/2020",
          "enddate": "02/01/2021",
        }, {
          "id": 5,
          "contactperson": "Leanne Graham",
          "productname": "Bret",
          "email": "Sincere@april.biz",
          "tel": "02058788888",
          "status": "",
          "price": "50.000$",
          "startdate": "17/10/2020",
          "enddate": "02/01/2021",
        },
      ]
    }
  },
}
</script>      
<style>
</style>