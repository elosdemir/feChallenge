<template>
  <b-breadcrumb class="breadcrumb" :items="items"></b-breadcrumb>
</template>
<style lang="scss">
.breadcrumb {
  border-radius: 0;
  background-color: #f2f2f2;
  border-bottom: 1px solid #ccc;
  padding: 15px !important;
  font-size: 16px;
  .breadcrumb-item {
    &.active {
      font-weight: bold;
      color: #000;
    }
  }
}
</style>
<script>
export default {
  data() {
    return {
      items: [
        {
          text: 'Sigortam.Net',
          href: '#'
        },
        {
          text: 'Yıllık Hayat Sigortası',
          href: '#'
        },
        {
          text: 'Yıllık Hayat Sigortası Başvuru Formu',
          active: true
        }
      ]
    }
  }
}
</script>