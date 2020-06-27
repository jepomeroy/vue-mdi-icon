<template>
    <div id="app">
        <h4 class="title">{{ `Showing ${state ? 'Home' : 'Airplane'} Icon` }}</h4>
        <div class="icon">
            <template v-if="this.state">
                <vue-mdi-icon
                    :path="mdiHome"
                    size="60"
                    rotate="-12.33"
                    title="Home"
                    description="Home Icon"
                    color="#24a39b"
                />
            </template>
            <template v-else>
                <vue-mdi-icon
                    :path="mdiAirplane"
                    size="60"
                    rotate="90"
                    title="Aiplane"
                    description="Aiplane Icon"
                    color="#ffa39b"
                />
            </template>
        </div>
        <div class="input">
            <input type="button" @click="switchIcons" value="Switch Icons" />
        </div>
    </div>
</template>

<script>
import Vue from 'vue'
import { mdiHome, mdiAirplane } from '@mdi/js'
import VueMdiIcon from '@/vue-mdi-icon.vue'

export default Vue.extend({
    name: 'ServeDev',
    components: {
        VueMdiIcon,
    },
    data() {
        return {
            mdiHome,
            mdiAirplane,
            state: false,
        }
    },
    methods: {
        switchIcons() {
            this.state = !this.state
        },
    },
})
</script>
