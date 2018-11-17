<template>
    <div class="navbar">
        <div class="nav-container">
          <a class="logo">E-NEWS!</a>
          <burger />
        </div>
    </div>
</template>

<script>
import Burger from "@/components/Burger";

export default {
  name: "navbar",
  props: {},
  components: {
    Burger
  }
};
</script>

<style scoped>
.navbar {
  height: 50px;
  max-width: 100%;
  background-color: #292f36;
  border-bottom: 4px solid #56e39f;
}
.nav-container {
  height: 100%;
  width: 80%;
  margin: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.logo {
  font-family: "Righteous", cursive;
  font-size: 24px;
  font-weight: bold;
  color: #56e39f;
}
</style>
