<template lang="pug">
  div
    h2 Examples
    p.-text(slot="example-description") To render a file input, apply the class <code>chi-file-input</code>
      | to an <code>input type="file"</code> and add a label next to it.

    <Base />
    <Disabled />
    <SizesPortal v-if="$store.state.themes.theme === 'portal'" />
    <SizesLumenCenturyLink v-else/>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Base from './_base.vue';
import Disabled from './_disabled.vue';
import SizesLumenCenturyLink from './_sizes-lumen-centurylink.vue';
import SizesPortal from './_portal/_sizes.vue'

@Component({
  components: {
    Base,
    Disabled,
    SizesLumenCenturyLink,
    SizesPortal
  }
})
export default class Examples extends Vue {}
</script>
