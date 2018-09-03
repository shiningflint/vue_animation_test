<template>
  <div>
    <ul>
      <li>
        <span>bananas</span>
        <button type="button" @click="deleteItem">delete</button>
      </li>
    </ul>
    <button type="button" @click="showPotato(true)">show potatoes</button>
    <transition>
      <p v-show="isPotatoShown">
        Here are them potatoes!
        <button type="button" @click="showPotato(false)">close</button>
      </p>
    </transition>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  data () {
    return {
      isPotatoShown: false
    }
  },
  methods: {
    deleteItem () {
      console.log('deleting the item')
    },
    showPotato (value) {
      this.isPotatoShown = value
    }
  }
}
</script>
