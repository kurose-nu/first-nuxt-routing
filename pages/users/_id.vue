<template>
  <section>
    <h1>{{ message }}</h1>
    <p>id: {{ this.$route.params.id }}</p>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      message: "/users/_id.vueを表示中"
    }
  },
  validate({ params }) {
    // 数値でない場合にエラーとする（正規表現で数値のみとしている）
    return /^\d+$/.test(params.id)
  }
}
</script>
