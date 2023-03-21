<template>
  <!-- <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <router-link class="navbar-brand" :to="{name: 'Home'}">Meta<span class="text-primary">Kurly</span></router-link>
    <ul class="navbar-nav mr-auto">
      <li class="nav-iem active">
        <router-link class="nav-link" :to="{name: 'Orders'}">Orders</router-link>
      </li>
      <li class="nav-iem active">
        <router-link class="nav-link" :to="{name: 'OrdersList'}">OrdersList</router-link>
      </li>
    </ul>
  </nav>
  <div class="container">
    <router-view/>
  </div> -->


  <nav class="navbar navbar-expand-lg navbar-light shadow-sm">
			<div class="container">
			  <router-link class="navbar-brand" :to="{name: 'Home'}">Meta<span class="text-primary">Kurly</span></router-link>

			  <div class="navbar-collapse collapse" id="navbarContent">
					<ul class="navbar-nav ml-lg-4 pt-3 pt-lg-0">
						<li class="nav-item"><router-link class="nav-link" :to="{name: 'Home'}">홈</router-link></li>
						<!-- <li class="nav-item"><router-link class="nav-link" :to="{name: 'ProductsBestList'}">베스트</router-link></li> -->
            <li class="nav-item"><router-link class="nav-link" to="/ProductsBestList">베스트</router-link></li>
						<!-- <li class="nav-item"><router-link class="nav-link" :to="{name: 'ProductsList'}">모든상품</router-link></li> -->
            <li class="nav-item"><router-link class="nav-link" to="/products">모든상품</router-link></li>
						<!-- <li class="nav-item"><router-link class="nav-link" :to="{name: 'MemberMyPage'}">마이페이지</router-link></li> -->
            <li class="nav-item"><router-link class="nav-link" to="/myPage">마이페이지</router-link></li>
					</ul>

          <div class="ml-auto" v-if="IsNullMember">
            <router-link class="btn btn-outline rounded-pill" to="/singup">회원가입</router-link>
            <router-link class="btn btn-outline rounded-pill" to="/login">로그인</router-link>
          </div>
					<div class="ml-auto" v-else>
						<!-- <p>환영합니다! {{member.userId}} 님</p> -->
            <p>환영합니다! 000 님</p>
						<router-link class="btn btn-outline rounded-pill" to="/logout">로그아웃</router-link>
					</div>
				</div>
			</div>
  </nav>
  <div class="page-section">
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import {ref} from 'vue';
export default {
  setup(){
    const member = ref(null);

    const IsNullMember = () => {
      return member == null;
    }

    return{
      member,
      IsNullMember,
    }
  }

}
</script>

<style>

</style>
