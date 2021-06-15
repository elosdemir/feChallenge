<template>
  <b-container>
    <b-row>
      <b-col cols="12">
        <h3>Başvuru Formu</h3>
        <p>Yıllık hayat sigortasından yalnız 18 yaşın üzerinde olanlar yararlanabilir.
        </p>
        <p> Vermiş olduğunuz bilgiler sizin adınıza sigorta şirketleri tarafına iletilecek ve ilgili şirketler
          tarafından
          size geri dönüş yapılacaktır.</p>
      </b-col>
    </b-row>
    <b-form inline>
      <b-row>
        <b-col lg="6" sm="12" md="12">
          <label class="sr-only" for="name">Adınız</label>

          <b-form-input v-model="userName" :state="validationName" id="feedback-user"></b-form-input>
          <b-form-invalid-feedback :state="validationName">
            isim boş bırakalamaz
          </b-form-invalid-feedback>
        </b-col>
        <b-col lg="6" sm="12" md="12">
          <label class="sr-only" for="surname">Soyadınız</label>

          <b-form-input v-model="userSurname" :state="validationSurname" id="feedback-user"></b-form-input>
          <b-form-invalid-feedback :state="validationSurname">
            soyisim boş bırakalamaz
          </b-form-invalid-feedback>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="4" sm="12" md="12">
          <label class="sr-only" for="telno">Cep Telefon Numaranız</label>
          <b-form-select v-model="selected" :options="options" size="sm" class="mt-3 form-control"></b-form-select>
          <b-form-input v-model="userTel" :state="validationTel" id="feedback-user"></b-form-input>
          <b-form-invalid-feedback :state="validationTel">
            tel boş bırakalamaz
          </b-form-invalid-feedback>
        </b-col>
      </b-row>
      <b-row class="mt-3">


      </b-row>
      <b-row class="mt-3">
        <b-col cols="6">
          <label class="sr-only mt-3" for="mail">E-posta adresiniz</label>
          <b-form-input v-model="userMail" :state="validationMail" id="feedback-user"></b-form-input>
          <b-form-invalid-feedback :state="validationMail">
            mail boş bırakalamaz
          </b-form-invalid-feedback>
        </b-col>

      </b-row>
      <b-row class="mt-3">
        <p>Yaşadığın şehir</p>
        <b-col>
          <b-form-select v-model="selected" :options="optionsIl" class="mt-1  form-control"></b-form-select>
        </b-col>
        <b-col>
          <b-form-select v-model="selected" :options="optionsIlce" class="mt-1  form-control"></b-form-select>
        </b-col>
      </b-row>
      <b-button variant="primary mt-3 mb-3" v-on:click="validation">Kayıt</b-button>
    </b-form>
  </b-container>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      userName: '',
      userSurname: '',
      userTel: '',
      userMail: '',
      selected: null,
      options: [
        {text: 'Seçiniz'},
        {text: 'VODAFONE'},
        {text: 'TURKCELL'},
      ],
      optionsIl: [
        {text: 'İl'},
        {text: 'İstanbul'},
        {text: 'Ankara'},
      ],
      optionsIlce: [
        {text: 'İlçe '},
        {text: 'Maslak '},
        {text: 'Karanfil'},
      ]
    }
  },
  computed: {
    validationName() {
      return this.userName.length > 0
    },
    validationSurname() {
      return this.userSurname.length > 0
    },
    validationMail() {
      return this.userMail.length > 0
    },
    validationTel() {
      return this.userTel.length > 0
    }
  }
}
</script>

<style scoped lang="scss">
 input,select {
   background: #f2f2f2;
 }
 select {
   appearance: auto !important;
 }
</style>