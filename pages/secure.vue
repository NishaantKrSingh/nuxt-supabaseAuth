<script setup>
const supabase = useSupabaseClient()
const signOut = async () => {
  const { error } = await supabase.auth.signOut()
  if (error) console.log(error)
  navigateTo('/login')
}
</script>


<template>
    <div>secure page</div>
    <div>
        <button @click="signOut">Log Out</button>
    </div>
</template>