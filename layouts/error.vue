<template>
  <div>
    <headers/>
    <div id="contents" class="container">
      <div class="row">
        <sidebox v-bind:data="[{id: 'error', title: '오류'}]"/>
        <div class="col s12 l11 pull-l1" style="min-height: 400px;">
          <div class="center">
            <i class="fa fa-exclamation" aria-hidden="true" style="font-size:15em;"></i>
            <div v-if="error.statusCode === 404" class="card-content">
              <p>없는 페이지입니다.</p>
            </div>
            <div v-else id="error" class="card-content">
              <p>무언가 오류가?</p>
            </div>
            <div class="row">
              <div class="col s3"></div>
              <nuxt-link to="/" class="btn btn-large orange darken-3 white-text col s6">메인으로 이동</nuxt-link>
              <div class="col s3"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footers/>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
import 'font-awesome/css/font-awesome.css'

/* import Headers from '~/components/Header.vue'
import Footers from '~/components/Footer.vue'
import Sidebox from '~/components/Sidebox.vue'

import init from '~/assets/init'
import buildmeta from '~/assets/buildmeta'

const title = 'Error :: On Demand'
const meta = buildmeta(title, 'ERROR',
  '', 'small_sunshine', null)

export default {
  components: {
    Headers,
    Footers,
    Sidebox
  },
  mounted () {
    init()
  },
  props: ['error'],
  head () {
    return {
      title,
      meta
    }
  }
} */
</script>
