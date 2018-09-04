<template>
  <div>
    <ul>
      <li>
        <span>bananas</span>
        <button type="button" @click="deleteItem">delete</button>
      </li>
    </ul>
    <button type="button" @click="showPotato(true)">show potatoes</button>
    <transition name="banana">
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

<style>
.banana-enter {
  opacity: 0;
  transform: translateY(-10px);
}
.banana-enter-active {
  transition: opacity 0.4s cubic-bezier(0.0, 0.0, 0.2, 1), transform 0.4s cubic-bezier(0.0, 0.0, 0.2, 1);
}
.banana-leave-active {
  transition: opacity 0.4s cubic-bezier(0.4, 0.0, 1, 1), transform 0.4s cubic-bezier(0.4, 0.0, 1, 1);
  opacity: 0;
  transform: translateY(-10px);
}
</style>
