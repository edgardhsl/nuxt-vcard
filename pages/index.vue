<template>
  <Side :active="menuActive">
    <div class="h-19.5">
      <i class="absolute top-0 right-0 hidden p-4 opacity-50 cursor-pointer fas fa-times text-slate-400 xl:hidden"
        sidenav-close="" aria-hidden="true"></i>
      <a class="block px-8 py-6 m-0 text-sm whitespace-nowrap text-slate-700" href="#home">
        <img src="~/assets/images/leadership.png"
          class="inline h-full max-w-full transition-all duration-200 ease-nav-brand max-h-8" alt="main_logo">
        <span class="ml-1 font-semibold transition-all duration-200 ease-nav-brand">{{ $config.public.brandTitle }}</span>
      </a>
    </div>
    <Separator></Separator>
    <SideItem href="#page1" icon="face" v-on:hash-change="menuActive = false">Quem sou eu?</SideItem>
    <SideItem href="#page2" icon="moving" v-on:hash-change="menuActive = false">A Pedagogia Empresarial</SideItem>
    <SideItem href="#page3" icon="collections_bookmark" v-on:hash-change="menuActive = false">Portfólio</SideItem>
    <SideItem href="#page6" icon="mail" v-on:hash-change="menuActive = false">Contato</SideItem>
  </Side>
  <main class="px-6">
    <div class="top-action">
      <Icon v-if="!menuActive" v-on:click="menuActive = true">menu</Icon>
      <Icon v-if="menuActive" v-on:click="menuActive = false">clear_all</Icon>
    </div>
    <Page id="home">
      <h1>Home</h1>
    </Page>
    <Page id="page1">
      <h1>Page 1</h1>
    </Page>
    <Page id="page2">
      <h1>Page 2</h1>
    </Page>
    <Page id="page3">
      <h1>Page 3</h1>
    </Page>
    <Page id="page4">
      <h1>Page 4</h1>
    </Page>
    <Page id="page5">
      <h1>Page 5</h1>
    </Page>
    <Page id="page6">
      <h1>Page 6</h1>
    </Page>
  </main>
</template>
<style lang="scss">
main {
  @apply ease-soft-in-out xl:ml-72 relative h-full max-h-screen rounded-xl transition-all duration-200;
  scroll-behavior: smooth;

  .top-action {
    @apply fixed p-5 w-[calc(100%_-_2rem)] flex justify-end;
  }
}
</style>
<script lang="ts">
export default {
  mounted() {
  },
  data() {
    return {
      menuActive: false,
    }
  },
  methods: {
    notify() {
      alert('dasdsad');
    }
  }
}
</script>