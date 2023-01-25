# Vue MDI Icon
Provides icon component for Vue that uses the https://materialdesignicons.com/ icons through @mdi/js

[![NPM Package](https://github.com/EarlPomeroy/vue-mdi-icon/actions/workflows/npm-publish.yml/badge.svg?branch=main)](https://github.com/EarlPomeroy/vue-mdi-icon/actions/workflows/npm-publish.yml)

### Install
    $ npm i vue-mdi-icon

### Basic Usage
```javascript
<template>
    <vue-mdi-icon :path="mdiHome" />
</template>

<script>
import Vue from 'vue'
import { mdiHome } from '@mdi/js'
import VueMdiIcon from '@/vue-mdi-icon.vue'
export default Vue.extend({
    components: {
        VueMdiIcon,
    },
    data() {
        return {
            mdiHome,
        }
    },
})
</script>
```
## License
[The 3-Clause BSD License](https://opensource.org/licenses/BSD-3-Clause)
