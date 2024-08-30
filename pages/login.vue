<script setup lang="ts">

const supabase = useSupabaseClient()
const signInWithOAuth = async () => {
  const { error } = await supabase.auth.signInWithOAuth({
    provider: 'google',
    options: {
      redirectTo: 'http://localhost:3000/confirm',
    },
  })
  if (error) console.log(error)
}

const signOut = async () => {
  const { error } = await supabase.auth.signOut()
  if (error) console.log(error)
}

definePageMeta({
  middleware: ["auth"],
})
</script>


<template>
  <div>
    <button @click="signInWithOAuth">
      Sign In with E-Mail
    </button>
  </div>
</template>