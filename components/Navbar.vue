<template>
     <c-box
    bg="gray.100"
    as="nav"
    h="60px"
    px="4"
    d="flex"
    align-items="center"
    shadow="sm"
  >
    <c-link
      as="nuxt-link"
      to="/"
      color="brand.700"
      font-weight="bold"
      :_hover="{ color: 'brand.900' }"
    >
      Podiocast
    </c-link>

    <c-box
      as="ul"
      color="gray.500"
      d="flex"
      align-items="center"
      list-style-type="none"
      ml="auto"
    >
      <c-box as="li" mr="8">
        <c-link
          color="gray.500"
          :_hover="{ color: 'brand.400' }"
          is-external
          href="https://vue.chakra-ui.com"
        >
          Documentation
        </c-link>
      </c-box>
      <c-box as="li" mr="8">
        <c-link
          color="gray.500"
          :_hover="{ color: 'brand.400' }"
          is-external
          href="https://github.com/chakra-ui/chakra-ui-vue"
        >
          Repo
        </c-link>
      </c-box>
     <c-box as="li">
        <c-icon-button
                variant="ghost"
                variant-color="gray[900]"
                :aria-label="`Switch to ${colorMode == 'light' ? 'dark' : 'light'} mode`"
                :icon="colorMode == 'light' ? 'moon' : 'sun'"
                @click="$toggleColorMode"
            />
        </c-box>
    </c-box>
  </c-box>
</template>

<script>
import { Cflex,CText,CButton,CBox, CLink, CIconButton } from '@chakra-ui/vue';

export default {
    components : {
        Cflex,
        CText,
        CButton,
        CBox,
        CLink,
        CIconButton
    },
    inject: ['$chakraColorMode', '$toggleColorMode'],
    computed: {
    colorMode () {
      return this.$chakraColorMode()
    }
  }
}
</script>
