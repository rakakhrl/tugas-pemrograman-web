<template>
    <div class="container" >
        <img class="image" :src="imgSrc"/>
        <div class="content">
          <p class="title" >{{title}}</p>
          <p class="desc" >{{count}} articles</p>
        </div>
    </div>
</template>

<script>
export default {
  name: "thumbnail",
  props: ["imgSrc", "title", "count"]
};
</script>

<style scoped>
.container {
  height: 240px;
  width: 180px;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  cursor: pointer;
}

.container:hover {
  padding-bottom: 10px;
}

.image {
  max-height: 200px;
  max-width: 150px;
  border-radius: 8px;
  margin: auto;
}

.content {
  width: 150px;
  margin: auto;
}

.title {
  font-family: "Lato", sans-serif;
  font-size: 16px;
  font-weight: bold;
  color: #292f36;
  margin: 0px;
}

.desc {
  font-family: "Lato", sans-serif;
  font-size: 12px;
  color: #292f36;
  margin: 0px;
}
</style>
