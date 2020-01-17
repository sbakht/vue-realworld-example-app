<template>
  <nav class="navbar navbar-light">
    <div class="container">
      <router-link class="navbar-brand" :to="{ name: 'home' }">
        PogChamp
      </router-link>


      <div v-if="!isAuthenticated">
        <guest />
      </div>

      <div v-else >
        <user v-bind:user="currentUser"/>
      </div>

    </div>
  </nav>
</template>

<script>
import { mapGetters } from "vuex";
import GuestHeader from "@/components/GuestHeader";
import UserHeader from "@/components/UserHeader";


export default {
  name: "RwvHeader",
  components: {
    guest: GuestHeader,
    user: UserHeader
  },
  computed: {
    ...mapGetters(["currentUser", "isAuthenticated"])
  }
};
</script>
