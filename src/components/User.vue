<template>
    <router-link :to="{name: 'Profile', params: {id: creator.id}}">
      <img class="rounded-circle" :src="creator.picture" :alt="creator.name" :title="creator.name">
    </router-link>

</template>


<script>
import { Account } from '../models/Account.js';

export default {
  props: {
    creator: {
      type: Account,
      required: true
    }
  },
  setup(props) {
    return {}
  }
}
</script>


<style lang="scss" scoped>
img {
  height: 64px;
  width: 64px;
  object-fit: cover;
  object-position: center;
  border-radius: 2px;
}
</style>
