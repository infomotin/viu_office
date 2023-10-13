<template>
    <div>
        <nav>
            <ul>
                <li><router-link to="/">home</router-link></li>
                <li><router-link to="/about">About</router-link></li>
                <li><router-link to="/contact">contact</router-link></li>
            </ul>
        </nav>
        <div>
            <ul>
                <li v-for="(id,index) in userIds" :key="index">
                    <router-link :to="{name:'Profile',params:{user_id:id}}">Profile {{ id }}</router-link>
                </li>
            </ul>

            <button @click="Contrac">Contrac</button>
            <button @click="About">About</button>
        </div>
    </div>

    
</template>

<script>
export default {
    name: 'NavBar',
    data() {
        return {
            userIds:['1','2','3','4','5','6','7','8','9']
        }
    },
    methods:{
        Contrac(){
            this.$router.push({name:'Contract'})
            console.log('Button Press')
        },
        About(){
            this.$router.push({name:'About'})
            console.log('Button Press About')
        }
    }
}
</script>

<style scoped>
nav {
    text-align: center;
}

nav ul {
    padding: 0;
}

nav li {
    display: inline-block;
    list-style-type: none;
    margin: 0;
    padding: 8px;
}
</style>