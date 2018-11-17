<template>
    <div>
        <button @click="toogle" class="menu-btn">&#9776;</button>
        <transition 
            name="fade"
        >
            <div v-if="show" class="menu-content" >
              <div class="content-container">
                <a class="menu-item">HOME</a>
                <a class="menu-item">BROWSE CATEGORY</a>
                <a class="menu-item">TOP NEWS</a>
                <a class="menu-item">SIGN UP</a>
                <a class="menu-item">LOGIN</a>
              </div>
            </div>
        </transition>
    </div>
</template>

<script>
export default {
  name: "burger",
  data() {
    return {
      show: false
    };
  },
  methods: {
    toogle() {
      this.show = !this.show;
    }
  }
};
</script>

<style scoped>
.menu-btn {
  font-size: 28px;
  background-color: transparent;
  color: #56e39f;
  border: none;
  outline: none;
  cursor: pointer;
}
.menu-content {
  height: 40px;
  width: 100%;
  position: absolute;
  top: 54px;
  left: 0px;
  background-color: #56e39f;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.menu-item {
  font-family: "Lato", sans-serif;
  font-weight: bold;
  font-size: 14px;
  margin: 0px 50px;
  color: #292f36;
  cursor: pointer;
}
.menu-item:hover {
  border-bottom: 0.75px solid #292f36;
}
</style>
