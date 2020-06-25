<script>
import Vue from 'vue'
import { mdiHome } from '@mdi/js'
import VueMdiIcon from '@/vue-mdi-icon.vue'

export default Vue.extend({
    name: 'ServeDev',
    components: {
        VueMdiIcon,
    },
    data() {
        return {
            icon: mdiHome,
        }
    },
})
</script>

<template>
    <div id="app">
        <vue-mdi-icon
            :path="icon"
            size="60"
            rotate="-12.33"
            title="Home"
            description="Home Icon"
            color="#24a39b"
        />
    </div>
</template>
