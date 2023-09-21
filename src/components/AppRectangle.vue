<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <div class="subscribe d-flex justify-content-around">
    <div class="subscribe-image">
      <img src="../../public/img/news.png" alt="" />
    </div>
    <div class="subscribe-content">
      <h4>Subscribe to our newsletter</h4>
      <div class="input-group mb-3">
        <input
          type="text"
          class="form-control"
          placeholder="Username"
          aria-label="Username"
          aria-describedby="basic-addon1"
        />
        <span class="input-group-text" id="basic-addon1">@</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.subscribe {
  max-width: 800px;
  min-height: 250px;
  background-color: #cc7c2b;
  margin: 0 auto;
  position: relative;

  img {
    height: 315px;
    position: absolute;
    top: -65px;
    left: 2%;
  }
}

.subscribe-content {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 400px;
}
</style>
