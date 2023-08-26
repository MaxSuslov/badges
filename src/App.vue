<template>
  <div>
    <!-- With PascalCase you can use it as a self-closing tag -->
    <!-- <TheHeader /> -->
    <!-- Modern JS will automatically translate TheHeader into the-header -->
    <the-header></the-header>
    <badge-list></badge-list>
    <user-info
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></user-info>
  </div>
</template>

<script>
// Instead of importing and registering components globally in main.js, you can import and register them locally in the component where you are going to use them
import TheHeader from "./components/TheHeader.vue";
import BadgeList from "./components/BadgeList.vue";
import UserInfo from "./components/UserInfo.vue";
export default {
  components: {
    TheHeader,
    BadgeList,
    UserInfo
  },
  data() {
    return {
      activeUser: {
        name: "Max Suslov",
        description: "Site owner and admin",
        role: "admin"
      }
    };
  }
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>
