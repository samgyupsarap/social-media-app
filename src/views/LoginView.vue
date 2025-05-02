<template>
  <div
    class="min-h-screen bg-gradient-to-br from-blue-500 to-purple-600 flex items-center justify-center p-6"
  >
    <div
      class="bg-white/20 backdrop-blur-lg rounded-2xl shadow-xl w-full max-w-4xl overflow-hidden"
    >
      <div class="grid md:grid-cols-2 gap-8 p-8">
        <!-- Brand Section -->
        <div class="flex flex-col justify-center items-center text-white">
          <div class="mb-8 transform hover:scale-105 transition-transform">
            <h1 class="text-4xl font-bold mb-4">Welcome to FeetBook</h1>
            <p class="text-lg opacity-80">Connect with friends and share your moments</p>
          </div>
          <div class="w-64 h-64 bg-white/30 rounded-full flex items-center justify-center">
            <!-- Add your logo here -->
            <span class="text-6xl">📱</span>
          </div>
        </div>

        <!-- Login Form Section -->
        <div class="bg-white/40 backdrop-blur-md rounded-xl p-8">
          <h1 class="text-3xl font-bold text-center text-gray-800 mb-8">Login</h1>
          <form class="flex flex-col gap-4" @submit.prevent="handleLogin">
            <div class="relative">
              <input
                type="text"
                placeholder="Username"
                class="w-full px-4 py-3 rounded-lg bg-white/50 border border-gray-200 focus:border-blue-500 focus:outline-none transition-colors"
                required
              />
            </div>
            <div class="relative">
              <input
                type="password"
                placeholder="Password"
                class="w-full px-4 py-3 rounded-lg bg-white/50 border border-gray-200 focus:border-blue-500 focus:outline-none transition-colors"
                required
              />
            </div>
            <button
              type="submit"
              class="bg-blue-600 hover:bg-blue-700 text-white py-3 rounded-lg font-semibold transition-colors"
            >
              Sign In
            </button>

            <div class="mt-1">
              <p class="text-center text-gray-600 mb-2">Or continue with</p>
              <div class="flex gap-4 justify-center">
                <button
                  class="w-full p-2 rounded-lg bg-black/80 hover:bg-black/60 transition-colors flex items-center justify-center gap-2"
                >
                  <Grid2x2 class="text-white w-5 h-5" />
                  <span class="text-white">Login with Microsoft</span>
                </button>
              </div>

              <div class="mt-4 text-center">
                <p class="text-gray-600">
                  Don't have an account?
                  <router-link to="/register" class="text-blue-600 hover:text-blue-700">
                    Sign Up
                  </router-link>
                </p>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Grid2x2 } from 'lucide-vue-next'
import { useRouter } from 'vue-router'

const router = useRouter()

const handleLogin = () => {
  console.log('Login attempted')

  router.push('/feetbook')
}
</script>

<style scoped>
.backdrop-blur-lg {
  backdrop-filter: blur(16px);
}
.backdrop-blur-md {
  backdrop-filter: blur(12px);
}
</style>
