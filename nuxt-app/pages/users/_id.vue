<template>
  <div>
    <h1>ユーザID: {{ $route.params.id }}</h1>
    <a href="/users/list">back</a>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: this.$route.params.id,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'User Id :' + this.$route.params.id,
        },
      ],
    }
  },
}
</script>
