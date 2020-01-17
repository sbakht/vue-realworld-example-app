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
        :to="{ name: 'article-edit' }"
      >
        <i class="ion-compose"></i>&nbsp;New Article
      </router-link>
    </li>
    <li class="nav-item">
      <router-link
        class="nav-link"
        active-class="active"
        exact
        :to="{ name: 'settings' }"
      >
        <i class="ion-gear-a"></i>&nbsp;Settings
      </router-link>
    </li>
    <li class="nav-item" v-if="user.username">
      <router-link
        class="nav-link"
        active-class="active"
        exact
        :to="{
              name: 'profile',
              params: { username: user.username }
            }"
      >
        {{ user.username }}
      </router-link>
    </li>
  </ul>
</template>

<script>
  export default {
    name: "UserHeader",
    props: ["user"]
  };
</script>
