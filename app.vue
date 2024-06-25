<template>
  <div>
    <button class="button" @click="signIn">Sign in</button>
    <button class="button" @click="signOut">Sign out</button>
    <pre>
      {{ credentials }}
    </pre>
  </div>
</template>

<script setup>
const credentials = ref()

const signIn = async () => {
  const email = "test@gmail.com"
  const password = "123456"
  credentials.value = await signInUser(email, password)
}
const signOut = async () => {
  credentials.value = await signOutUser()
}

</script>

<style scope>
@import "https://cdn.jsdelivr.net/npm/bulma@1.0.1/css/bulma.min.css";
</style>