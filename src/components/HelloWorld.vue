<template>
  <div class="flex justify-center mt-5">
    <div class="max-w-sm rounded overflow-hidden shadow-lg w-96">
      <form>
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">Masuk</div>
          <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="username">
              Username
            </label>
            <input v-model="user.username" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username">
          </div>
          <div class="mb-6">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
              Password
            </label>
            <input v-model="user.password" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="Password">
          </div>
          <div class="flex items-center justify-between">
            <button @click.prevent="onSubmit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="submit">
              Sign In
            </button>
            <a class="inline-block align-baseline font-bold text-sm text-blue-500 hover:text-blue-800" href="#">
              Forgot Password?
            </a>
          </div>
        </div>

      </form>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      user:{
        username: '',
        password: ''
      }
    }
  },
  methods:{
    onSubmit(){
      console.log(this.user)
      this.user.username = ''
      this.user.password = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
