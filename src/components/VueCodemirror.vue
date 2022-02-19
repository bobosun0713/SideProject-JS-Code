<template>
  <textarea ref="codemirror"></textarea>
</template>

<script>
import _CodeMirror from 'codemirror'
import 'codemirror/lib/codemirror.css'
import 'codemirror/mode/javascript/javascript.js'
import 'codemirror/theme/darcula.css'

import { onMounted, ref } from 'vue'
export default {
  name: 'Codemirror',
  setup() {
    const codemirror = ref(null)
    const editorInit = () => {
      const editor = _CodeMirror.fromTextArea(codemirror.value, {
        mode: 'text/javascript',
        theme: 'darcula',
        lineNumbers: true,
        collapseIdentical: false,
        spellcheck: true,
      })
      editor.on('inputRead', function (cm) {
        cm.showHint()
      })
    }

    onMounted(() => {
      editorInit()
    })
    return { codemirror }
  },
}
</script>

<style lang="scss">
// Codemirror css
.CodeMirror {
  width: 100%;
  height: 300px;

  &-gutters {
    background-color: #2b2b2b !important;
  }
}
</style>
