<template>
  <nav class="md:mx-auto flex flex-wrap items-center justify-center divide-x divide-emerald-100">
    <RouterLink class="px-4 py-2 text-emerald-500 transition hover:bg-emerald-100"
                :active-class="'text-slate-700 hover:bg-transparent'"
                to="/">Home
    </RouterLink>
    <RouterLink class="px-4 py-2 text-emerald-500 transition hover:bg-emerald-100"
                :active-class="'text-slate-700 hover:bg-transparent'"
                to="/about">About
    </RouterLink>
  </nav>
  <RouterView/>
</template>

