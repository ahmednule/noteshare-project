<template>
<v-app>
    <!--the Navbar-->
    <v-app-bar app color="E1C2BB" text-white dark>
      <v-toolbar dark prominent>
         <v-app-bar-nav-icon  @click="toogleDrawer"></v-app-bar-nav-icon>
         <v-toolbar-title class="toolbar-title">Noteshare</v-toolbar-title>
         <v-spacer></v-spacer>
            <v-btn text @click="logout" flat>back</v-btn>
        </v-toolbar>
    </v-app-bar>
  <v-container fluid fill-height>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="6">
        <v-card outlined>
          <v-card-title>Login</v-card-title>
          <v-card-text>
            <v-text-field
              label="Username"
              v-model="username"
              required
            ></v-text-field>
            <v-text-field
              label="Password"
              type="password"
              v-model="password"
              required
            ></v-text-field>
            <div class="mt-4">
              <v-checkbox v-model="rememberMe" label="Remember Me"></v-checkbox>
            </div>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" @click="login" :disabled="!username || !password">
              Login
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  <v-footer fixed>
    <v-btn><i class="fa fa-facebook" aria-hidden="true"></i></v-btn>
    <v-spacer></v-spacer>
    <v-btn><i class="fa fa-home" aria-hidden="true"></i></v-btn>
    <v-spacer></v-spacer>

    <span>Sharing knowledge worldwide</span>
  </v-footer>
  </v-app>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      password: '',
      rememberMe: false,
    };
  },
  methods: {
    async login() {
      try {
        const response = await axios.post('/api/auth/login/', {
          username: this.username,
          password: this.password,
        });
        // Handle successful login (e.g., store token, redirect to dashboard)
      } catch (error) {
        console.error('Error logging in:', error);
      }
    },
  },
};
</script>

<style scoped>
.mt-4 {
  margin-top: 1rem;
}
</style>