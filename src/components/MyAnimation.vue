<template>
  <ul>
    <li>
      <span>bananas</span>
      <button type="button" @click="deleteItem">delete</button>
    </li>
  </ul>
</template>

<script>
export default {
  methods: {
    deleteItem () {
      console.log('deleting the item')
    }
  }
}
</script>
