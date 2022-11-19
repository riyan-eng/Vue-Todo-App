<template lang="">
    <div>
        <form @submit.prevent="onSubmit">
        <div class="d-flex mt-5">
                <input v-model="task" type="text" class="w-100 form-control" style="margin-right:5px" placeholder="Enter task">
                <input type="submit" value="Save" class="btn btn-warning">

            </div>
        </form>
    </div>
</template>
<script>
export default {
    name: "AddForm",
    data (){
        return {
            task: ""
        }
    },
    methods:{
        onSubmit (){
            if (!this.task){
                alert("isi!!!")
                return
            }
            console.log(this.task)
            this.task = ""

        }
    }
}
</script>
<style lang="">
    
</style>