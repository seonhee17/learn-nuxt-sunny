`<template>
    <div>
        <header>
        <!-- nuxt-link 사용하기 -->
        <h1>{{ $route.name }} 페이지</h1>
        <NuxtLink to="/">홈페이지</NuxtLink>
        <NuxtLink to="/main">메인 페이지</NuxtLink>
        <NuxtLink to="/product">상품페이지</NuxtLink>
        <!-- <router-link></router-link> -->
        </header>
        <Nuxt />
    </div>
</template>
<script>
export default {}
</script>