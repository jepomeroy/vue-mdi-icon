<template>
    <div id="app">
        <h4 class="title">
            {{ `Showing ${state ? 'Home' : 'Airplane'} Icon` }}
        </h4>
        <div class="icon">
            <template v-if="this.state">
                <vue-mdi-icon
                    class="home"
                    :path="mdiHomeOutline"
                    size="60"
                    rotate="-12.33"
                    title="Home"
                    description="Home Icon"
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
import { mdiHomeOutline, mdiAirplane } from '@mdi/js'
import VueMdiIcon from '@/vue-mdi-icon.vue'

export default Vue.extend({
    name: 'ServeDev',
    components: {
        VueMdiIcon,
    },
    data() {
        return {
            mdiHomeOutline,
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
<style scoped>
.home {
    fill: hsl(320, 77%, 34%);
}
.home:hover {
    fill: hsl(320, 77%, 44%);
}
</style>
