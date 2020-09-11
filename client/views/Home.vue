<template>
  <div class="home">
  </div>
</template>

<script>
// import FileSaver from 'file-saver'
import ejs from 'ejs'
export default {
  name: 'Home',
  mounted () {
    // var aFileParts = ['<a id="a"><b id="b">hey!</b></a>']
    // var oMyBlob = new Blob(aFileParts, { type: 'text/plain;charset=utf-8' })
    // FileSaver.saveAs(oMyBlob, 'test.vue')
    const people = ['geddy', 'neil', 'alex']
    const html = ejs.render('<%= people.join(", "); %>', { people: people })
    console.log(html)
  }
}
</script>
