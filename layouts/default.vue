<template>
    <div class="grid grid-cols-3">
        <div class="col-span-1 flex justify-end">
            <nav class="text-right">
                <div class="flex justify-between items-center">
                    <h1 class="font-bold uppercase p-4 border-b border-gray-100">
                      <a href="/" class="hover:text-gray-700 tracking-widest">Food Ninja</a>
                    </h1>
                    <div class="px-4 cursor-pointer md:hidden" id="burger">
                      <svg class="w-6 h-6" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24"><path d="M4 6h16M4 12h16M4 18h16"></path></svg>
                    </div>
                </div>
                <ul class="text-sm mt-6 hidden md:block" id="menu">
                  <MenuButton to="/" title="Home">
                    <svg class="w-5 ml-2" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24"><path d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
                  </MenuButton>
                  <MenuButton to="/food" title="Food">
                    <svg class="w-5 ml-2" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" ><path stroke-linecap="round" stroke-linejoin="round" d="M15.75 17.25v3.375c0 .621-.504 1.125-1.125 1.125h-9.75a1.125 1.125 0 0 1-1.125-1.125V7.875c0-.621.504-1.125 1.125-1.125H6.75a9.06 9.06 0 0 1 1.5.124m7.5 10.376h3.375c.621 0 1.125-.504 1.125-1.125V11.25c0-4.46-3.243-8.161-7.5-8.876a9.06 9.06 0 0 0-1.5-.124H9.375c-.621 0-1.125.504-1.125 1.125v3.5m7.5 10.375H9.375a1.125 1.125 0 0 1-1.125-1.125v-9.25m12 6.625v-1.875a3.375 3.375 0 0 0-3.375-3.375h-1.5a1.125 1.125 0 0 1-1.125-1.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H9.75" /></svg>
                  </MenuButton>
                  <MenuButton  to="/about" title="About">
                    <svg class="w-5 ml-2" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24"><path d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path></svg>
                  </MenuButton>
                  <MenuButton  to="/contact" title="Contact">
                    <svg class="w-5 ml-2" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24"><path d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                  </MenuButton>
                </ul>
            </nav>
        </div>
        <main class="col-span-2 p-10 bg-gray-100">
            <div class="flex justify-end">
                <NuxtLink to="/login" class="btn text-2xl border-2 border-primary text-primary hover:bg-primary hover:text-white transition ease-out duration-100">Log in</NuxtLink>
                <NuxtLink to="/signup" class="btn ml-3 text-2xl border-2 border-primary text-primary hover:bg-primary hover:text-white transition ease-out duration-100">Sign up</NuxtLink>
            </div>
            <header class="p-10">
                <h2 class="text-6xl font-bold text-gray-700 leading-none tracking-wider">{{ ($route.name==='index'?'Home':$route.name)?.toString().toUpperCase()}}</h2>
                <h3 class="text-2xl font-semibold text-gray-600 tracking-wider pt-5">For Ninjas</h3>
            </header>
            <slot />
        </main>
    </div>
</template>


<script setup lang="ts">
  
</script>

<style scoped>

</style>