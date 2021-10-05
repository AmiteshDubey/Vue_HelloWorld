<template>
  <div>
    <button type="button" style="float:left" @click="addNewRow">Add</button>
    <button type="button" style="float:left" @click="deleteAll">Delete All</button>
    <table>
      <tr>
        <th>Operation</th>
        <th>Name</th>
        <th>Job</th>
      </tr>

      <tr v-for="(job, index) in jobs" :key="index">
        <td style="width:200px">
          <button type="button" @click="deleteRow(index)">Delete</button>   
          
        </td>
        <td>
          <input type="text" v-model="job.name" />
        </td>
        <td>
          <input type="text" v-model="job.prof" />
        </td>
      </tr>

      <tr v-show="jobs.length==0">
        <td
          colspan="3"
          style="text-align:center;height:100px;vertical-align: middle;"
        >No record available</td>
      </tr>
    </table>
    <br />
  </div>
</template>
<script>
export default {
  name: " ",
 
  mounted() {
    //load the data
    this.jobs = [
      {
        name: "Ajay",
        prof: "Doctor"
      },
      {
        name: "Raj",
        prof: "Scientist"
      }
    ];
  },
  data() {
    return {
      jobs: [""]
    };
  },
  methods: {
    deleteAll() {
      this.jobs = [];
    },
    addNewRow() {
      this.jobs.push({
        name: '',
        prof: ''
      });
    },
    deleteRow(_index) {
      this.jobs.splice(_index, 1);
    },
    
  }
};
</script>