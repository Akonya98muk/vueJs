<template>
  <div>
    <Post-form/>
    <TheHeader posts="posts"></TheHeader>
  </div>

</template>

<script>

import PostForm from '@/components/PostForm'
import TheHeader from '@/components/TheHeader'

export default {
  components: {
    PostForm,
    TheHeader
  },
  data: function () {
    return {
      posts: [
        {
          id: 1,
          title: 'JavaScript',
          body: 'Описание поста'
        },
        {
          id: 2,
          title: 'JavaScript 2',
          body: 'Описание поста'
        },
        {
          id: 3,
          title: 'JavaScript 3',
          body: 'Описание поста'
        }
      ],
      title: '  ',
      body: ' '
    }
  },
  methods: {
    createPost () {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body
      }
      this.posts.push(newPost)
      this.body = ' '
      this.title = ' '
    }

  }
}

</script>
