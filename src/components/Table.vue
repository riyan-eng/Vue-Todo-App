<template lang="">
    <div>
        <table class="table table-bordered">
            <thead>
                <tr>
                  <th scope="col">#</th>
                  <th scope="col">Name</th>
                  <th scope="col">Action</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <th scope="row">1</th>
                  <td>Mark</td>
                  <td>
                    <router-link to="/detail">
                      <button>Detail</button>
                    </router-link>
                    <router-link to="/update">
                      <button>Update</button>
                    </router-link>
                    <button @click="onDelete">Delete</button>
                  </td>
                </tr>
                <tr>
                  <th scope="row">2</th>
                  <td>Jacob</td>
                  <td>@fat</td>
                </tr>
             
              </tbody>
        </table>
    </div>
</template>
<script>
export default {
    name: "Table",
    methods:{
      onDelete(){
        console.log("hapus")
      }
    }
}
</script>
<style lang="">
    
</style>