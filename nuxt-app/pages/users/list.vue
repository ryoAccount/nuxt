<template>
  <div>
    <h1>User List</h1>
    <ul>
      <li v-for="user in users" :key="user.id">
        {{ user.id }} : <a :href="user.id">{{ user.name }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'Adam' },
        { id: 2, name: 'Baba' },
        { id: 3, name: 'Camel' },
      ],
    }
  },
}
</script>
