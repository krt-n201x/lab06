<template>
  <div v-if="Store.event">
    <h1>{{ Store.event.title }}</h1>
    <div id="nav">
      <router-link :to="{ name: 'EventDetails' }">Details</router-link>
      |
      <router-link :to="{ name: 'EventRegister' }">Register</router-link>
      |
      <router-link :to="{ name: 'EventEdit' }">Edit</router-link>
    </div>
    <router-view :event="Store.event" />
  </div>
</template>
<script>
export default {
  inject: ['Store']
}
</script>
