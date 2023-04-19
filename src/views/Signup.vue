<template>
  <div class="signup">
    <img alt="Vue logo" class="logo" src="../assets/logo-locaweb.svg" />

    <div class="container">
      <h3>
        Você está muito próximo de mudar a forma de <br /><span
          >hospedar seu site</span
        >
      </h3>

      <span class="choose-plan">Escolha o seu plano</span>

      <div class="container-plancard">
        <PlanCard />
        <PlanCard />
        <PlanCard />
      </div>
    </div>
  </div>
</template>

<script>
import PlanCard from "../components/PlanCard.vue";

export default {
  name: "Signup",
  components: { PlanCard },

  data() {
    return {};
  },

  computed: {},

  methods: {},
};
</script>

<style scoped>
.signup {
  display: flex;
  flex-direction: column;
  text-align: center;
  margin: 30px 16px;
}

h3 {
  margin-top: 44px;
  margin-bottom: 22px;
}

h3 span {
  color: var(--primary-color-hover);
  text-decoration: underline;
}

.container-plancard {
  display: flex;
  justify-content: center;
  gap: 0 20px;
}

.choose-plan {
  margin-top: 20px;
  margin-bottom: 35px;
}
</style>
