<template>
  <div>
    <div>
      <input type="text">
      <button @click="chat">发送</button>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    socket.on("lmq", data => {
      console.log(data);
    });
  },
  methods: {
    chat() {
      socket.emit("lmq", "你好啊");
    }
  }
};
</script>

<style scoped>
</style>