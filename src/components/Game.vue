<template>
    <tr>
      <th scope="row">{{id}}</th>
      <td>{{name}}</td>
      <td class="d-flex justify-content-center"><button class="p-2" @click="eliminar">eliminar</button></td>
    </tr>
    
</template>

<script>
export default {
    name: 'game-component',
    props: {
        id:{
            type:Number,
            required:true,
        },
        name:{
            type:String,
            required:true,
        }
    },
    data: function(){
        return {}
    },
    // computed: {},
    methods: {
        eliminar(){
            this.$emit('eliminar',this.id)
        }
    }
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
td,th{
    border: 1px solid white;
}
button{
    border: none;
    border-radius: 3px;
    width: 40%;
    background-color: rgb(206, 25, 25);
    color: white;

}
</style>