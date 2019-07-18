 <template>
     <div>
   <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile to="/">
          <v-list-tile-action>
            <v-icon>dashboard</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Dashboard</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <p>Administrating</p>
        <v-spacer></v-spacer>
        <v-list-tile to="/RoleManager">
          <v-list-tile-action>
            <v-icon>security</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Role Manager</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

        <v-list-tile to="/AdminUser">
          <v-list-tile-action>
            <v-icon>verified_user</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Admin User</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>

        <v-list-tile to="/UsersManager">
          <v-list-tile-action>
            <v-icon>supervised_user_circle</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Users Manager</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar color="primary" dark fixed app>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-spacer></v-spacer>
      <v-layout justify-end>
        <v-toolbar-items class="hidden-sm-and-down">
         <v-icon left medium>search</v-icon>
         <v-icon medium>email</v-icon>
            <v-avatar>
            <img
              src="https://cdn.vuetifyjs.com/images/john.jpg"
              alt="John"
            >
          </v-avatar>
       </v-toolbar-items>
      </v-layout>
  </v-toolbar>
</div>
</template>

<style scoped>
.v-avatar {
  margin-left: 10px;
}
p{
  font-size: 18px;
  margin: 10px;
  margin-left: 20px;
}
</style>

<script>
export default {
  data: () => ({
    drawer: true
  }),
  props: {
    source: String
  }
}
</script>
