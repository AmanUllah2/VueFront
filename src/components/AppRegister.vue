<template>
    <div>
   <app-toolbar></app-toolbar>
   <v-container>
        <v-form action="http://localhost:3800/users/register" method = "POST">
        <v-text-field
        label = "Name"
        v-model= "name"
        name="name"
        >
        </v-text-field>
        <v-text-field
        label = "Email"
        v-model= "email"
        type = "email"
        name="email"
        >
        </v-text-field>
        <v-text-field
        label = "Password"
        v-model= "password"
        name = "password"
        type="password"
        required
        >
        </v-text-field>
        <v-btn color="indigo" type="submit" dark>Register</v-btn>
        </v-form>
    </v-container>
    <app-footer></app-footer>
    </div>
</template>

<script>
import AppFooter from './AppFooter'
import AppToolbar from './AppToolbar'


export default {
    components: {AppFooter, AppToolbar},
    methods: {
       addUser() {
             let uri = 'http://localhost:3500/users/register';
            this.axios.post(uri, this.users).then((response) => {
               console.log(response);
            });
       }
    }
    
}
</script>