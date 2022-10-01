<template>
  <div>
    <form @submit.prevent>
      <input
        @input="title=$event.target.value"
        :value="title"
        type="text"
        placeholder="Nazvanie">

      <input
        @input="body=$event.target.value"
        :value="body"
        type="text"
        placeholder="Opisanie">

      <button @click="createPost">Dobavit</button>
    </form>
  </div>

</template>

<script>

</script>
