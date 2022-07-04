<template>
  <div class="card">
    <img class="card-image" :src="info.previewPictureSrc" />
    <div class="card-body">
      <div class="title">{{ info.title }}</div>
      <div
        class="content lg:max-h-[75px] max-h-[50px] overflow-hidden relative before:content-[''] before:absolute before:w-full before:h-8 lg:before:h-12 before:bg-gradient-to-t before:from-white before:to-transparent before:bottom-0 before:left-0"
      >
        {{ info.previewContext }}
      </div>
      <a :href="info.url" target="_blank" class="button">立即前往 &#x276F;</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    info: Object,
  },
};
</script>
<style scoped>
.card {
  width: 323px;
}
.card-image {
  width: 100%;
  height: 170px;
}
.card-body {
  padding: 18px 5px;
  text-align: center;
}
.title {
  font-size: 20px;
}
.content {
  font-size: 16px;
}

.button {
  font-size: 14px;
  height: 40px;
  width: 108px;
  color: #fff;
  background: #504e4d;
  margin: 18px auto;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
