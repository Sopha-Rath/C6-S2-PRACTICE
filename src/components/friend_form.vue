<template>
<div class="container">
     <form class="form" @submit.prevent="addItem">
        <div class="form-group d-flex justify-content-center">
            <li class="fa fa-user-circle-o"></li>
        </div>
        <div class="form-group">
            <input type="text" class="form-control" placeholder="First Name" v-model="firstname" required>
        </div>
        <div class="form-group">
            <input type="text" class="form-control" placeholder="Last Name" v-model="lastname" required>
        </div>
        <div class="form-group">
            <input type="text" class="form-control" placeholder="Comment" v-model="comment" required>
        </div>
        <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" value="HTML" v-model="checkvalue">
            <label class="form-check-label" for="inlineCheckbox1">HTML</label>
        </div>
        <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" value="CSS" v-model="checkvalue"> 
            <label class="form-check-label" for="inlineCheckbox2">CSS</label>
        </div>
        <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" value="OOP" v-model="checkvalue">
            <label class="form-check-label" for="inlineCheckbox2">OOP</label>
        </div>
         <div class="form-check form-check-inline">
            <input class="form-check-input" type="checkbox" value="JAVA" v-model="checkvalue">
            <label class="form-check-label" for="inlineCheckbox2">JAVA</label>
        </div>
        <div class="form-group mt-4">
            <button type="submit" class="btn btn-primary">ADD</button>
        </div>
    </form>
</div>
</template>

<script>
    export default {
        emits: "add-data",
        data() {
            return {
                firstname: '',
                lastname: '',
                comment: '',
                checkvalue: [],
            }
        },
        methods: {
            addItem() {
               this.$emit('add-data', this.firstname, this.lastname, this.comment, this.checkvalue),
               this.firstname = '',
               this.lastname = '',
               this.comment = '',
               this.checkvalue = ''
            }
        }
    }
</script>

<style scoped>
.fa-user-circle-o {
    color: rgb(210, 96, 96);
}
.container  {
    display: flex;
    justify-content: center;
}
.form {
    background: #fff;
    padding: 30px;
    width: 50%;
    margin-top: 7rem;
    border-radius: 5px;
    box-shadow: rgba(14, 30, 37, 0.12) 0px 2px 4px 0px, rgba(14, 30, 37, 0.32) 0px 2px 16px 0px;
}
.btn {
    width: 100%;
}
h4 {
    margin-top: 10px;
}
.fa-user-circle-o{
    font-size: 50px;
}
</style>