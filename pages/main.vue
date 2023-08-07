<template>
    <div>
        <h1>
            메인페이지
        </h1>
    </div>
</template>


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