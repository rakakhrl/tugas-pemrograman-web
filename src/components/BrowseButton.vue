<template>
    <a class="browse-btn">Browse Category</a>
</template>

<script>
export default {
  name: "browse-button"
};
</script>

<style scoped>
.browse-btn {
  height: 40px;
  width: 140px;
  background-color: #56e39f;
  color: white;
  font-family: "Lato", sans-serif;
  font-weight: 700;
  font-size: 14px;
  text-align: center;
  text-decoration: none;
  border: none;
  border-radius: 20px;
  outline: none;
  cursor: pointer;
  margin: 100px 0px 0px 25px;
  padding: 12px 0px;
  box-sizing: border-box;
}
.browse-btn:hover {
  background-color: #47ba83;
}
</style>
