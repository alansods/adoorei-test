<template>
  <div class="home">
    <img alt="Vue logo" class="logo" src="../assets/logo-locaweb.svg" />

    <div class="container">
      <h3>Entre na sua conta</h3>
      <span class="subtitle"
        >Para acessar sua conta informe seu e-mail e senha</span
      >

      <form action="submit" @click="handleLogin" class="form">
        <div>
          <label for="">E-mail</label>
          <input v-model="user.email" type="text" placeholder="Seu e-mail" />
        </div>

        <div>
          <label for="">Senha</label>
          <input
            v-model="user.password"
            type="password"
            placeholder="Sua senha"
          />
        </div>

        <span class="forgot-password">Esqueci minha senha</span>

        <button class="primary-button" :disabled="!checkForm">
          Fazer Login
        </button>
      </form>
    </div>

    <div class="sign-up">Ainda não tem conta? <span>Cadastre-se</span></div>
  </div>
</template>

<script>

export default {
  name: "Login",
  components: {},

  data() {
    return {
      user: {
        email: "",
        password: "",
      },
    };
  },

  computed: {
    checkForm() {
      return this.user.email.length && this.user.password.length ? true : false;
    },
  },

  methods: {
    handleLogin(e) {
      e.preventDefault();

      const newUser = {
        email: this.user.email,
        username: "alansods",
        password: this.user.password,
        name: {
          firstname: "Alan",
          lastname: "Santos",
        },
        address: {
          city: "kilcoole",
          street: "7835 new road",
          number: 3,
          zipcode: "12926-3874",
          geolocation: {
            lat: "-37.3159",
            long: "81.1496",
          },
        },
        phone: "1-570-236-7033",
      };

      console.log(newUser);

      fetch("https://fakestoreapi.com/users", {
        method: "POST",
        body: JSON.stringify(newUser),
      })
        .then((res) => res.json())
        .then((json) => console.log(`json: ${JSON.stringify(json)}`));
    },
  },
};
</script>

<style scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100vh;
}

.logo {
  margin-bottom: 48px;
}

.container {
  background-color: #fff;
  border: solid 1px #e6eaf2;
  border-radius: 5px;
  padding: 30px;
  width: 617px;
}

@media only screen and (max-width: 600px) {
  .container {
    background-color: #fff;
    border: solid 1px #e6eaf2;
    border-radius: 5px;
    padding: 30px 20px;
    max-width: 350px;
    margin: 0 auto;
  }
}

.container .form {
  margin-top: 19px;
}

.form div {
  margin-bottom: 15px;
}

.sign-up {
  font-size: 1.125rem;
  margin-top: 32px;
}

.sign-up span {
  display: inline-block;
  color: var(--primary-color);
  text-decoration: underline;
  cursor: pointer;
}

.sign-up span:hover {
  color: var(--primary-color-hover);
}

.forgot-password {
  display: block;
  text-align: right;
  margin-left: auto;
  margin-bottom: 25px;
  color: #515d74;
  font-size: 1rem;
  cursor: pointer;
}

.forgot-password:hover {
  text-decoration: underline;
}

.subtitle {
  font-size: 1.125rem;
}
</style>
