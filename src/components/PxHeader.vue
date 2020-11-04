<template>
  <header class="shadow w-screen">
    <nav>
      <nav class="flex items-center justify-between flex-wrap bg-green-400 p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <router-link :to="{name: 'home'}" style="display: inherit">
            <px-icon/>
            <span class="font-semibold text-xl tracking-tight ml-2" style="align-self: center;">
              PlatziExchange
            </span>
          </router-link>
        </div>
        <div class="flex w-auto flex-grow items-center">
          <div class="text-sm lg:flex-grow">
            <router-link v-for="l in links" :key="l.title" :to="l.to" class="inline-block text-teal-200 hover:text-white mr-4">
              {{ l.title }}
            </router-link>
          </div>
        </div>
      </nav>
    </nav>
  </header>
</template>

<script>
  import PxIcon from "@/components/PxIcon";
  export default {
    components: {
      PxIcon
    },
    props: {
      links: {
        type: Array,
        default: () => []
      }
    }
  }
</script>

<style>

</style>