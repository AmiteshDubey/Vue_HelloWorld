<template>
    <div>

        <h1>Date</h1>
        <h4 class="list-group-item" v-show="date"><strong>Date:</strong> {{ date }}</h4>

        <button @click="showPopUp=true">Show Time</button>

        <template  v-if="showPopUp">
            <h1>Time</h1>
        <h4 class="list-group-item" v-show="time"><strong>Time:</strong> {{ time }}</h4>
        </template>
       


    </div>
</template>

<script>
    export default {
        name:"Clock",
        data: () => ({
          date: '',
          time: '',
          showPopUp:false,
        }),
        methods: {
          printDate: function () {
            return new Date().toLocaleDateString();
          },
          printTime: function () {
            return new Date().toLocaleTimeString();
          }
        },
        mounted: function () {
          this.date = this.printDate();
          this.time = this.printTime();
        
    }
    }
</script>

<style scoped>

</style>