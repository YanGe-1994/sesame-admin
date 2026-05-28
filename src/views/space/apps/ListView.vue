<script>
import { post } from '@/utils/fetch.ts'
export default {
  methods: {
    fetchChat: async () => {
      const res = await post('/apps/debug/fa4e492d-191c-4e65-86fe-160d1c8e2a23', {
        body: {
          query: '你好，你是谁',
        },
      })
      console.log(res)
    },
  },
}
</script>
<template>
  <a-button @click="fetchChat">发起请求</a-button>
</template>

<style scoped></style>
