<template>
  <div class="post" v-for="post in posts" :key="post" >
    <div><strong>НАзвание:</strong> {{ post.title }}</div>
    <div><strong>OPisanie:</strong> {{ post.body }}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>
