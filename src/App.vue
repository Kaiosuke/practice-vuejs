<script setup lang="ts">
const list: string = 'a,b,c,d,e,f,g'

const handleList = (v: string): string => {
  return v.split(',').join('-')
}

const attribute = 'href'
const url: string = 'https://google.com'

const number = 123 // Nếu là reactive => const number = ref(123)
</script>

<template>
  <button>
    {{ number }}
  </button>
  <div class="flex gap-4">
    <div :id="handleList(list)">11</div>
    <a :[attribute]="url">Google</a>
  </div>
</template>

