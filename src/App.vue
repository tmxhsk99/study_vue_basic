<!--html 영역-->
<template>
  <!-- 탬플레이트에는 하나의 엘리멘트만 있어야한다. -->
  <div>
  <!--{{ str }}-->
    <app-header></app-header>
    <app-content></app-content>
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
      str: 'hi'
    }
  },
  components:{
    //지역 컴포넌트 등록방식
    //컴포넌트 이름 : 컴포넌트 내용
    'app-header' : AppHeader,
    'app-content' : AppContent,
    'app-footer' : AppFooter
  }
}
</script>
<!-- css 영역 -->
<style>

</style>