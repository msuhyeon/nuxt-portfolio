<template>
  <div class="main">
    <section class="main__content">
      <h1 class="main__content--title">Frontend<br />개발자</h1>
      <p class="main__content--sub">
        훌륭한 사용자 경험을 제공하고 확장 가능한 Products를 만드는 것을
        좋아합니다.
      </p>
    </section>
  </div>
</template>
<script>
definePageMeta({
  layout: 'default',
});
</script>
<style lang="scss" scoped>
.main {
  .main__content {
    margin-top: calc(11.12em + 2em);
    padding: 0 15rem;

    .main__content--title {
      font-size: 5rem;
      color: #00008b;
    }
    .main__content--sub {
      margin-top: 20px;
      font-size: 1.5rem;
      color: #fff;
    }
  }
}
</style>
