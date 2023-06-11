<template>
    <div>
    <h1>Hello from home component</h1>
    <!-- <h3>{{data}}</h3> -->
    <button v-on:click="hello" >Click hello function</button>

    <h1 v-if="show">Conditional rendering in Vue js</h1>
    <h1 v-else> Conditional rendering else block. </h1>
    <button v-on:click="display">Toggle element</button>

    <table border="1px">
        <tr>
            <td>id</td>
            <td>name</td>
            <td>email</td>
        </tr>

        <tr v-for="user in users" :key="user.id" >
            <td>{{user.id}}</td>
            <td>{{user.name}}</td>
            <td>{{user.email}}</td>
        </tr>

    </table>

    </div>
</template>

<script>
export default {
    name: 'HomeName',
    props: {
        data: String
    },
    methods: {
        hello() {
            console.log("Hello console called.")
        },
        display() {
            this.show = !this.show
        }
    },data()
    {
        return {
            show:true,
            users: [
                {id:1, name:'Peter', email:'Peter@email.com'},
                {id:2, name:'Ashish', email:'Ashish@email.com'},
                {id:3, name:'Rahul', email:'Rahul@email.com'},
                {id:4, name:'Sachin', email:'Sachin@email.com'}
            ]
            }
    }
}
</script>
