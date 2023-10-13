
<template>
    
    <div>
        
        <h1>Profile</h1>
        <p>User Id:{{ UserId }}</p>
    </div>
</template>
<script>

    export default{
        name:'Profile',
        data(){
            return{
                UserId:this.$route.params.user_id
            }
        },
        methods:{
            updateId(){
                this.UserId = this.$route.params.user_id
            }
        },
        watch:{
            $route :'updateId'
        }
        
    }
</script>

<style scoped>

</style>