<template>
  <div class="grid">
    <div class="grid__nps-card">
      <h1>NPS Geral</h1>
      <SuccessIcon />
      <p class="grid__nps-card__status">Excelente!</p>
      <p class="grid__nps-card__result">NPS Score 75</p>
    </div>

    <div class="grid__sales-card">
      <h1>Vendas fechadas</h1>

      <Donut percentage="70" type="primary" />

      <div class="grid__sales-card__bullets">
        <div class="grid__sales-card__bullets__result">
          <span class="grid__sales-card__bullets__dot primary" />
          <p>Esperado</p>
          <span class="grid__sales-card__bullets__result__value">100</span>
        </div>

        <div class="grid__sales-card__bullets__result">
          <span class="grid__sales-card__bullets__dot second" />
          <p>Alcançado</p>
          <span class="grid__sales-card__bullets__result__value">100</span>
        </div>
      </div>
    </div>

    <div class="grid__sales-card">
      <h1>Meta mensal</h1>

      <Donut percentage="90" type="second" />

      <div class="grid__sales-card__bullets">
        <div class="grid__sales-card__bullets__result">
          <span class="grid__sales-card__bullets__dot primary" />
          <p>Esperado</p>
          <span class="grid__sales-card__bullets__result__value">100</span>
        </div>

        <div class="grid__sales-card__bullets__result">
          <span class="grid__sales-card__bullets__dot third" />
          <p>Alcançado</p>
          <span class="grid__sales-card__bullets__result__value">100</span>
        </div>
      </div>
    </div>

    <div class="grid__week-sales-card">
      <div class="grid__week-sales-card__info">
        <h1>Vendas por dia da semana</h1>
        
        <div class="grid__week-sales-card__info__sale">
          <PolygonPlusIcon class="grid__week-sales-card__info__sale__icon" />
          <p class="grid__week-sales-card__info__sale__text">Dia com mais vendas</p>
        </div>

        <p class="grid__week-sales-card__info__label">quarta-feira</p>

        <div class="grid__week-sales-card__info__sale">
          <PolygonLessIcon class="grid__week-sales-card__info__sale__icon" />
          <p class="grid__week-sales-card__info__sale__text">Dia com menos vendas</p>
        </div>

        <p class="grid__week-sales-card__info__label">doming</p>
      </div>

      <div class="grid__week-sales-card__graph"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "./styles.scss";
* {
  font-family: Inter;
}

html,
body {
  margin: 0;
  height: 100vh;
  width: 100%;

  background: #292738;
}

h1,
p,
span {
  margin: 0;
}

#__nuxt {
  display: flex;
  align-content: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}
</style>

