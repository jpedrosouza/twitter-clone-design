<template>
  <div class="make-login">
    <span class="make-login-title">Novo no Twitter?</span>
    <span class="make-login-subtitle"
      >Inscreva-se para ter sua própia timeline personalizada!</span
    >
    <div class="buttons-container">
      <button class="login-option-button">
        <img
          class="login-option-button-image"
          src="../assets/icons/google_icon.png"
          alt=""
        />
        <span>Inscrever-se no Google</span>
      </button>
      <button class="login-option-button">
        <img
          class="login-option-button-image"
          src="../assets/icons/apple_icon.svg"
          alt=""
        />
        <span>Inscrever-se com Apple</span>
      </button>
      <button class="login-option-button">
        <span>Inscrever-se com número de celular</span>
      </button>
    </div>
    <div class="terms-container">
      Ao se inscrever você concorda com os <span>Termos de Serviço</span> e a
      <span>Política de Privacidade</span>, incluindo o
      <span>Uso de Cookies.</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "MakeLogin",
};
</script>

<style scoped>
.make-login {
  width: 30vw;
  height: 35vh;
  margin-left: 30px;
  display: flex;
  flex-direction: column;
  border-radius: 30px;
  border: rgba(255, 255, 255, 0.527);
  border-style: solid;
  border-width: thin;
}

.make-login-title {
  margin-top: 20px;
  margin-left: 20px;
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 800;
  color: white;
}

.make-login-subtitle {
  margin-left: 20px;
  font-size: 13px;
  color: rgb(148, 148, 148);
}

.buttons-container {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.login-option-button {
  width: 90%;
  height: 40px;
  margin-bottom: 20px;
  border-radius: 30px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  color: black;
  background-color: white;
  cursor: pointer;
}

.login-option-button:hover {
  background-color: rgba(255, 255, 255, 0.877);
}

.login-option-button-image {
  padding-right: 10px;
}

.terms-container {
  margin-left: 20px;
  font-size: 13px;
  color: rgb(148, 148, 148);
}

.terms-container span {
  color: rgb(29, 155, 240);;
  cursor: pointer;
}
</style>