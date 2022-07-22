<template>
    <div class="app">
        <div class="card">
            <h5>Full Name: {{data.FirstName}} {{data.LastName}}</h5>
            <p>Description: {{data.Comment}}</p>
            <h3>{{data.name}}</h3>
            <p>{{data.description}}</p>
            <div class="btn d-flex justify-content-start">
                <button class="btn btn-danger ml-2" v-for="skill of data.skills" :key="skill">{{skill}}</button>
            </div>
        </div> 
    </div>
</template>
<script>
 export default {
    props: {
        data: Object
    }
  }
</script>

<style scoped>
.app {
    margin-top: 10px;
    display: flex;
    justify-content: center;
}
.card  {
    padding: 10px;
    border-top: 4px solid rgb(196, 33, 77);
    width: 41%;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}
</style>