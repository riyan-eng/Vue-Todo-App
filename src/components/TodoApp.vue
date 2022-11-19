<template lang="">
    <div class="container" style="max-width:600px">
        <h2 class="text-center mt-5">My vue todo app</h2>
        <AddForm/>
        <div class="mt-3">
            <Table/>
        </div>
    </div>
</template>
<script>
import AddForm from "./Add.vue"
import Table from "./Table.vue"

export default {
    components:{
        AddForm,
        Table
    },
    name: 'TodoApp',
}
</script>
<style lang="">
    
</style>