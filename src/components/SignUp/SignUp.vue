<script setup>
import '../../assets/css/SignUp/signUp.css'
import LogoTitle from '@/components/LogoTitle.vue'
import { useRouter } from 'vue-router';

// TODO implement form validation
const router = useRouter();
const signUp = () => {
  router.push('/dashboard')
};
</script>

<template>
  <div class="signup-wrapper">
    <div class="signup-container">
      <form class="signup-form" @submit.prevent="signUp">
        <LogoTitle color="#ffffff"></LogoTitle>
        <input class="username-input" type="text" placeholder="Username">
        <input class="password-input" type="password" placeholder="Password">
        <input class="password-input" type="password" placeholder="Repeat password">
        <div class="signup-button-container">
          <button class="signup-button" type="submit">Sign up</button>
          <div class="login-paragraph-container">
            <p>Already created an account?
              <RouterLink to="/login" style="color: white">Login</RouterLink>
            </p>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<style scoped>

</style>