<template>
  <div class="row q-pt-md justify-center q-col-gutter-y-lg font_semi-bold">
    <div class="col-10">
      <q-btn
        outline
        rounded
        color="primary"
        class="text-purple-14 full-width"
        no-caps
        push
        type="a"
        target="_blank"
        href="https://egua.tech/egua/"
        stack
      >
      <img
        class="q-pb-sm q-pr-sm"
        alt="Trusty Icon"
        src="eguatechnoname.png"
        width="35"
      >
      <div class="q-pl-xs">Linguagem Egua</div>
      </q-btn>
    </div>
    <div class="col-10">
      <q-btn
        outline
        rounded
        color="primary"
        class="text-grey-9 full-width"
        no-caps
        push
        type="a"
        target="_blank"
        href="https://egua.tech/docs/"
        stack
      >
      <img
        class="q-pb-sm q-pr-sm"
        alt="Trusty Icon"
        src="eguatechPB.png"
        width="35"
      >
      <div class="q-pl-xs">Documentação</div>
      </q-btn>
    </div>
    <!-- <div class="col-6 text-center">
      <q-btn
        flat
        color="white"
        no-caps
        @click="register"
      >
        <span class="button-underline text-black font_semi-bold">
          Criar uma Conta
        </span>
      </q-btn>
    </div>
    <div class="col-6 text-center">
      <q-btn
        flat
        color="white"
        no-caps
        @click="email"
      >
        <span class="button-underline text-black font_semi-bold">
          Entrar com E-mail
        </span>
      </q-btn>
    </div>
    <dialog-register
      :visible="dialogRegister"
      @close="closeRegister"
    />
    <dialog-login
      :visible="dialogLogin"
      @close="closeLogin"
     /> -->
  </div>
</template>

<script>
export default {
  name: 'LoginButtons',
  components: {
  },
  data () {
    return {
      dialogRegister: false,
      dialogLogin: false
    }
  },
  methods: {
    login () {
      this.$q.loading.show()
      setTimeout(() => {
        this.$q.loading.hide()
        this.$router.push({ name: 'dashboard' })
      }, 2000)
    },
    email () {
      this.dialogLogin = true
    },
    closeLogin () {
      this.dialogLogin = false
    },
    register () {
      this.dialogRegister = true
    },
    closeRegister () {
      this.dialogRegister = false
    }
  }
}
</script>
