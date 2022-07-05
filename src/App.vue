<!--html 영역-->
<template>
  <!-- 탬플레이트에는 하나의 엘리멘트만 있어야한다. -->
  <div>
<!--<app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header>-->
    <app-header v-bind:propsdata="message"
                v-on:renew="rewnewStr"></app-header>
    <app-content v-bind:propsnum="num"></app-content>
    <app-footer></app-footer>
  </div>
</template>
<!--자바스크립트 영역-->
<script>
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  data: function () {
    return {
      message : 'appHeader',
      num : 10
    }
  },
  components:{
    //지역 컴포넌트 등록방식
    //컴포넌트 이름 : 컴포넌트 내용
    'app-header' : AppHeader,
    'app-content' : AppContent,
    'app-footer' : AppFooter
  },
  methods:{
    rewnewStr:function (){
      this.message = 'hi'
    }
  }
}
</script>
<!-- css 영역 -->
<style>

</style>