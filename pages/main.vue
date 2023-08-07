<template>
    <div>
      <!-- <h1>메인페이지</h1> -->
      <p>메인페이지</p>
      <div>
        <ul>
          <!-- key 사용 이유
            Vue에서 개별 DOM 노드들을 추적하고 기존 엘리먼트를 재사용, 
             재정렬하기 위해서 v-for의 각 항목들에 고유한 key 속성을 제공해야 합니다.
          -->
          <li v-for="product in products" :key="product.id">
            {{ product }}
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  import axios from 'axios';


  export default {
   
    async asyncData(){
      const response = await axios.get('http://localhost:3000/products');
      console.log(response)
      const products = response.data
      return { products }
    },
    // data(){
    //   return {
    //     products: [],
    //   }
    // },
    // async created() {},

    // created 를 사용 시 빈배열이 먼저 화면에 그려지는 것을 확인할 수 있다.
    // 이러한 단점을 보완하기위해 
    // nuxt에서 제공하는것을 알아보자.
    
    // 1.asyncData 사용
    // 컴포넌트가 생성되기 전에 이전에 호출 
    // asyncData 의 속성 주의 사항
    // pages 폴더 안에서만 유효한 인스턴스 속성이라는 것을 기억!!

  }
  </script>
  
  <style></style>

<!-- <template>
    <div>
        <NuxtLogo />
        <h1>메인페이지</h1>
    </div>
</template>

<script>
import NuxtLogo  from '@/components/NuxtLogo.vue';

export default{
    components: {
        NuxtLogo,
    },
}
</script> -->

<!-- 
       .nuxt/layouts/default.vue 해당 경로 파일내용
       <templete>
            <Nuxt/>
       </templete>
    
       <Nuxt/> 태그는 아래의 태그들과 같은의미 이다.
       <Nuxt></Nuxt> 
       <router-view></router-view>
       
       /main url은 /.nuxt/router.js에서 경로를 확인 (router설정파일)
       /main URL 이동 시 아래 처럼 DOM이 그려진다.
       <Root>
        <NuxtLoading>
        <NuxtBuildingIndicator>
        <Transition>
        <.nuxtLayoutsDefault.vue>  ->/layouts/default.vue 의미 
        <Nuxt>
          <PagesMain.vue> ->pages/main.vue

       
  -->