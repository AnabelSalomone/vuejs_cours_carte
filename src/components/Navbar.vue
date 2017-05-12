<template>
  <div>
    Message: {{ msg }} Nb: {{ nimporte.counter }}
    <a @click="nimporte.counter += 5">Up!!!!</a>
    <coucou></coucou>
  </div>
</template>

<script>
import {Bus} from '@/Bus.js'
import {Store} from '@/Store.js'
import Coucou from '@/components/Coucou'

export default {
  name: 'navbar',
  components: {coucou: Coucou},

  created() {
    Bus.$on('faim', () =>
        this.msg = "J'ai faim!"
    );

    Bus.$on('soif', () =>
      alert(' A Malibu')
    );
  },
  data(){
    return {
      msg: '',
      nimporte: Store.datas
    }
  },
}
</script>