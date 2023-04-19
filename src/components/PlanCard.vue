<template>
  <div class="plancard">
    <div class="container-flag">
      <span class="flag">Mais Usado</span>
    </div>

    <h3>Hospedagem 1</h3>

    <span class="price">Grátis</span>
    <span class="subtitle1">você não paga nada para usar</span>
    <span class="subtitle2">sem taxa de setup</span>

    <hr />
    <span class="subtitle3">Ideal para quem está começando</span>
    <hr />

    <button class="primary-button">Escolher esse plano</button>

    <h4>Seu site em servidores no Estados Unidos.</h4>

    <ul>
      <li>Servidores em nossos data center americanos;</li>
      <li>Servidores em nossos data center americanos;</li>
      <li>Servidores em nossos data center americanos;</li>
      <li>Servidores em nossos data center americanos;</li>
      <li>Servidores em nossos data center americanos;</li>
      <li>Servidores em nossos data center americanos;</li>
    </ul>

    <span>Suporte 24 horas, 7 dias por semana grátis;</span>
    <span>Aplicativos disponíveis:</span>

    <ul>
      <li>Wordpress;</li>
      <li>Drupal;</li>
      <li>entre outros...</li>
    </ul>

    <span>Você ainda tem</span>

    <ul>
      <li>Webmais RoudCube;</li>
      <li>Webmais RoudCube;</li>
      <li>Webmais RoudCube;</li>
      <li>Webmais RoudCube;</li>
      <li>Webmais RoudCube;</li>
      <li>Webmais RoudCube;</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PlanCard",
  components: {},

  data() {
    return {};
  },

  computed: {},

  methods: {},
};
</script>

<style scoped>
.plancard {
  width: 348px;
  background-color: #fff;
  padding: 40px;
  border-radius: 5px;
  color: #666666;
  position: relative;
  margin-bottom: 40px;
}

h3 {
  font-size: 1.625rem;
}

span {
  display: block;
}

hr {
  border-top: 1px solid rgba(196, 196, 196, 0.5);
  margin: 18px 0
}

.price {
  font-size: 2.125rem;
  color: var(--primary-color);
  font-weight: bold;
  margin-top: 21px;
  margin-bottom: 13px;
}

.container-flag {
  position: absolute;
  top: -10px;
  left: 0;
  right: 0;
}

.flag {
  display: inline-block;
  background-color: #10c300;
  color: #fff;
  text-transform: uppercase;
  font-size: 0.875rem;
  border-radius: 10px;
  padding: 7px 16px;
}

.primary-button {
  padding: 18px 24px;
  margin-bottom: 25px;
}

.subtitle1 {
  font-size: 0.875rem;
  margin-bottom: 10px;
}

.subtitle2 {
  font-size: 0.875rem;
}

.subtitle3 {
  font-size: 1.0625rem;
}

h4 {
  text-align: left;
  font-size: 1.0625rem;
  font-weight: bold;
  margin-bottom: 10px;
}

ul {
  text-align: left;
}


</style>
