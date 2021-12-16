<template>
  <div id="app">
	  {{user}}
	  <hr/>登录
	  <form @submit.prevent="onSubmit">
		  <label>
			  <span>用户名</span>
		<!-- <MyInput v-model="user.username"/>两种使用方法，要么使用v-model,要么使用:value -->
		     <MyInput :value="user.username" 
			  @input="user.username =$event"/>
	     </label>
		  <label>
			  <span>密码</span>
			  <input type="password" v-model="user.password">
	     </label>
	     <button type="submit">登录</button>
     </form>
  </div>
</template>

<script>
import MyInput from "./MyInput.vue";
export default {
	components:{MyInput},
   name: 'App',
   data () {
		return {
			user:{
				username:"",
			   password:""
		 },
		 x:[]
    };
  },
  methods:{
	  onSubmit(){
		  console.log(this.user);
	  }
  },
};
</script>

