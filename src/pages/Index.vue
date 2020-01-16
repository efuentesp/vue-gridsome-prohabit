<template lang="pug">
layout
  h1.text-3xl.font-bold.border-b Nuevos Desarrollos Habitacionales
  .flex.mt-6
    div
      img(src="http://prohabit.netlify.com/images/residencial-del-bosque/conjunto.652x480.jpg")
    div
      h2.text-2xl.font-bold.text-teal-500 Residencial del Bosque
      h3.font-bold.mt-2 Carretera al Moral No 111, Col. El Moral
      h3.font-bold.mb-3 San Martín Texmelucan, Puebla
      span.rounded.bg-teal-500.text-xl.text-white.font-bold.p-2 Desde $384,000 hasta $414,000
      p.mt-3.text-justify Residencial Del Bosque está ubicado a 10 minutos del zócalo de San Martin Texmelucan, a solo unos metros del libramiento (Carretera Federal - Carretera al Verde). Residencial del Bosque cuenta con 60 departamentos distribuidos en 10 edificios de 3 niveles. Las plantas bajas cuentan con jardín y las plantas altas con espacio de azotea. Los departamentos cuentan con sala-comedor, cocina, baño y 2 recamaras. Residencial del Bosque cuenta área de estacionamiento común.
      .flex.justify-between.items-center.mt-3
        .flex
          span.tag-property-features.mr-2
            span 55 m
            sup 2
          span.tag-property-features.mr-2 2
          span.tag-property-features.mr-2 2
          span.tag-property-features.mr-2 1
        .flex
          button.bg-orange-400.rounded.text-white.p-2 Más información
      .flex
        span.bg-green-400.rounded.p-1.text-white.mr-2 Venta
        span.bg-blue-300.rounded.p-1.text-white Departamentos Nuevos
</template>

<script>
export default {
  metaInfo: {
    title: "ProHabit"
  }
};
</script>

<style>

</style>
