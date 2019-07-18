<template>
  <v-form v-model="valid">
      <v-container>
        <v-layout row wrap>
        <v-flex xs12 md6 sm6>
       <v-card max-width="500px">
         <v-card-text>
           <h2>Profile Information</h2>
          <v-text-field
            v-model="name"
            :rules="nameRules"
            :counter="20"
            label="Name"
            required
            class="centered-input text--darken-3 mt-3"
          ></v-text-field>

          <v-text-field
            v-model="designation"
            :rules="designationRules"
            :counter="20"
            label="Designation"
            required
          ></v-text-field>

          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
          <h3>Profile Picture</h3>
          <v-avatar size="100">
            <img
              src="https://cdn.vuetifyjs.com/images/john.jpg"
              alt="John"
            >
          </v-avatar>
          <v-btn color="pink">update</v-btn>
       </v-card-text>
      </v-card>
        </v-flex>

      <v-flex xs12 md6 sm6>
       <v-card max-width="500px">
         <v-card-text>
           <h2>Change Password</h2>
          <v-text-field
            v-model="oldpassword"
            :type="'password'"
            :rules="oldpasswordRules"
            label="Old Password"
            required
            class="centered-input text--darken-3 mt-3"
          ></v-text-field>

          <v-text-field
            v-model="newpassword"
            :type="'password'"
            :rules="newpasswordRules"
            label="New Password"
            required
          ></v-text-field>

          <v-text-field
            v-model="confirmpassword"
            :type="'password'"
            :rules="confirmpasswordRules"
            label="Confirm Password"
            required
          ></v-text-field>
           <v-btn color="pink">Change Password</v-btn>
       </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
    </v-container>

  </v-form>
</template>

<style scoped>
h3{
  margin-bottom: 10px;
  margin-top: 10px;
}
.v-btn {
  color: white !important;
}
</style>

<script>
export default {
  data: () => ({
    valid: false,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 20 || 'Name must be less than 20 characters'
    ],
    designation: '',
    designationRules: [
      v => !!v || 'Designation is required',
      v => v.length <= 20 || 'Name must be less than 20 characters'
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid'
    ],
    password: '',
    oldpasswordRules: [
      value => !!value || 'Required.'

    ],
    password: '',
    newpasswordRules: [
      value => !!value || 'Required.',
      v => v.length >= 8 || 'Min 8 characters'
    ],
    password: '',
    confirmpasswordRules: [
      value => !!value || 'Required.',
      v => v.length >= 8 || 'Min 8 characters'
    ]
  })
}
</script>
