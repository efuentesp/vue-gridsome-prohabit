<template lang="pug">
layout
  h1.text-3xl.font-bold.border-b Nuevos Desarrollos Habitacionales
  .flex.mt-6
    div.pr-2(class="w-1/2")
      img.border-8.border-solid.border-white.shadow-xl(src="http://prohabit.netlify.com/images/residencial-del-bosque/conjunto.652x480.jpg")
    div.pl-2(class="w-1/2")
      h2.text-2xl.font-bold.text-teal-500.underline Residencial del Bosque
      div.text-gray-700
        h3.mt-2 Carretera al Moral No 111, Col. El Moral
        h3.font-bold.mb-3 San Martín Texmelucan, Puebla
      span.rounded.bg-teal-500.text-xl.text-white.font-bold.p-2 Desde $384,000 hasta $414,000
      .flex.mt-3
        span.border.border-green-400.rounded.px-2.py-1.text-green-600.mr-2 Venta
        span.border.border-blue-400.rounded.px-2.py-1.text-blue-500 Departamentos Nuevos
      p.mt-3.text-justify Residencial Del Bosque está ubicado a 10 minutos del zócalo de San Martin Texmelucan, a solo unos metros del libramiento (Carretera Federal - Carretera al Verde). Residencial del Bosque cuenta con 60 departamentos distribuidos en 10 edificios de 3 niveles. Las plantas bajas cuentan con jardín y las plantas altas con espacio de azotea. Los departamentos cuentan con sala-comedor, cocina, baño y 2 recamaras. Residencial del Bosque cuenta área de estacionamiento común.
      .flex.justify-between.items-center.mt-3
        .flex
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'home']")
            span.pl-1 55 m
            sup 2
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'bed']")
            span.pl-1 2
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'bath']")
            span.pl-2 2
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'car']")
            span.pl-2 1
        .flex.items-center
          button.text-xl.text-blue-500.underline
            font-awesome.text-blue-500(:icon="['fas', 'info-circle']")
            span.pl-1 Más información
</template>

<script>
export default {
  metaInfo: {
    title: "ProHabit"
  }
};
</script>

<style></style>
