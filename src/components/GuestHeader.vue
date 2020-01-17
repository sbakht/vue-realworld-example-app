<template>
  <ul class="nav navbar-nav pull-xs-right">
    <li class="nav-item">
      <router-link
        class="nav-link"
        active-class="active"
        exact
        :to="{ name: 'home' }"
      >
        Home
      </router-link>
    </li>
    <li class="nav-item">
      <router-link
        class="nav-link"
        active-class="active"
        exact
        :to="{ name: 'login' }"
      >
        <i class="ion-compose"></i>Sign in
      </router-link>
    </li>
    <li class="nav-item">
      <router-link
        class="nav-link"
        active-class="active"
        exact
        :to="{ name: 'register' }"
      >
        <i class="ion-compose"></i>Sign up
      </router-link>
    </li>
  </ul>
</template>

<script>
  export default {
    name: "GuestHeader",
  };
</script>
