<template>
  <b-container class="banner">
    <b-row class="justify-content-center">
      <b-col cols="8">
        <p class="d-none d-lg-block d-xl-block
">Yıllık Hayat Sigortası ile vefat ve kaza sonrası maddi zararlara karşı kendinizi ve sevdiklerinizi koruyun.
          Yaşınıza, mesleğinizin risk grubuna, geçirdiğiniz hastalıklara göre değişen yıllık hayat sigortası fiyatları
          ve yıllık hayat sigortası poliçelerine ulaşmak için formu doldurun, yıllık hayat sigortası hesaplaması için
          sigorta şirketleri sizi arasın.
        </p>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "Banner"
}
</script>

<style scoped lang="scss">
.banner {
  width: 100%;
  height: 200px;
  background: url('https://cdnsnet.mncdn.com/static/images/shared/cover_images/branch/yillik-hayat/form.jpg') no-repeat;
  background-size: cover;
  display: inline-flex;
  place-items: center;
  position: relative;
  padding: 0;

  &:before {
    content: "";
    width: 100%;
    height: 100%;
    background: #000;
    opacity: 0.4;
    position: absolute;
  }

  p {
    color: #fff;
    position: relative;
  }
}
</style>