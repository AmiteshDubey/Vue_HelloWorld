<template>
<table>
      <thead>
          <tr>
              <th>ID</th>
              <th>Name</th>
             <th>Phone</th>
          </tr>
      </thead>
      <tbody>
          <tr v-for="(item, index) in items" :key="index">
              <td>{{item.id}}</td>
              <td>{{item.name}}</td>
             <td>{{item.job}}</td>
          </tr>
      </tbody>
    </table>
  
</template>
<script>
export default {
    data(){
        return {
            items: [
        {
            'id':'1',
            'name': 'John',
            'job': 'Doctor',
        },
        {
            'id':'2',
            'name': 'Zack',
            'job': 'Engineer',
        },
        {
            'id':'3',
            'name': 'Amit',
            'job': 'Scientist',
        }
            ],

        }
        
    },
    
}
</script>