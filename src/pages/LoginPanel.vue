<template>
<div>
   <!-- TOOLBAR -->
  <v-toolbar color="indigo darken-4" flat fixed dark>
      <v-toolbar-title>
        <v-icon left color="white">local_hospital</v-icon>
        <span style="color:white">Pocket Hospital</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat>Log In</v-btn>
          <v-btn class="black" >
            <v-icon left>account_box</v-icon>Sign Up
          </v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <!-- LOGIN -->
    <v-flex xs12 sm6 offset-sm3 class="mt-5 pt-5">
      <v-card img="https://www.webpackaging.com/up/comp/3210/header-image.jpg">
          <div style="height:185px"></div>
          </v-card>
      <v-card>
        
        <v-card-title primary-title>
          <div>
            <h3 class="display-1 mb-4">Login</h3>
            <v-container fluid>
                <v-layout row wrap>
                    <v-flex xs12>
                        <v-text-field
                            prepend-icon="email"
                            class="mx-5 mr-5 input-group--focused"
                            name="input-1"
                            label="Username or E-mail"
                            id="testing"
                            v-model="email"
                            :rules="emailRules"
                        ></v-text-field>
                    </v-flex>
                </v-layout>
                <v-layout row>
                    <v-flex xs12>
                        <v-text-field
                            name="input-10-1"
                            prepend-icon="security"
                            class="ml-5 mr-5 input-group--focused"
                            label="Password"
                            :append-icon="e1 ? 'visibility' : 'visibility_off'"
                            :append-icon-cb="() => (e1 = !e1)"
                            :type="e1 ? 'text' : 'password'"
                            id="testing"
                        ></v-text-field>
                    </v-flex>
                </v-layout>
            </v-container>
          </div>
        </v-card-title>
        <v-card-actions>
          <v-btn flat color="blue" class="ml-5"> <v-icon small class="mr-2">done</v-icon><b>Login</b></v-btn>
          <v-btn flat color="red"> <v-icon small class="mr-2">cancel</v-icon><b>Cancel</b></v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>

</div>
</template>

<script>
export default {
  data(){
      return {
          e1: false,
          password: 'Password'
      }
  }
}
</script>