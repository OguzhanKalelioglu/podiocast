<template>
  <div class="container">

    <CThemeProvider>
      <CColorModeProvider>
        <CBox font-family="body" as="main">
            <Navbar />
          <CReset />
          <Nuxt />
        </CBox>
      </CColorModeProvider>
    </CThemeProvider>
  </div>
</template>
<script>
import {
  CThemeProvider,
  CColorModeProvider,
  CReset,
  CBox
} from '@chakra-ui/vue'

import Navbar from '../components/Navbar'

export default {
  name: 'App',
  components: {
    CThemeProvider,
    CColorModeProvider,
    CReset,
    CBox,
  },
  components : {
    Navbar
  }
}

</script>
