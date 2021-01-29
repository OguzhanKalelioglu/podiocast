<template>
    <div>
        <div v-for="item in post" :key="item.id" class="container">
           <c-flex align="center" justify="center">
                 <c-box w="sm">
                    <c-image src="https://bit.ly/chakra-jonathan-bakebwa" alt="Jonathan Bakebwa" />
                 </c-box>
           </c-flex>
        </div>
    </div>
</template>

<script>
import { CImage } from "@chakra-ui/vue";


export default {
      async asyncData({ params, $http }) {
      const post = await $http.$get(`https://aralikmag.herokuapp.com/sayilars?slug=${params.index}`)
      return { post }
    }
}
</script>