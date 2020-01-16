<template lang="pug">
layout
  h1.text-3xl.font-bold.border-b Nuevos Desarrollos Habitacionales
  .flex.mt-8(v-for="{node} in $page.productos.edges" :key="node.id")
    div.pr-2(class="w-1/2")
      g-image.border-8.border-solid.border-white.shadow-xl(:src="node.main_image.file.url")
    div.pl-2(class="w-1/2")
      h2.text-2xl.font-bold.text-teal-500.underline {{node.title}}
      div.text-gray-700
        h3.mt-2 {{node.address}}
        h3.font-bold.mb-3 {{node.city}}
      span.rounded.bg-teal-500.text-xl.text-white.font-bold.p-2 {{node.price}}
      .flex.mt-3
        span.border.border-green-400.rounded.px-2.py-1.text-green-600.mr-2 {{node.category}}
        span.border.border-blue-400.rounded.px-2.py-1.text-blue-500 {{node.type}}
      p.mt-3.text-justify {{node.short_description.content[0].content[0].value}}
      .flex.justify-between.items-center.mt-3
        .flex
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'home']")
            span.pl-1 {{node.m2}} m
            sup 2
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'bed']")
            span.pl-1 {{node.bedrooms}}
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'bath']")
            span.pl-2 {{node.bathrooms}}
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'car']")
            span.pl-2 {{node.garages}}
        .flex.items-center
          button.text-xl.text-blue-500.underline
            font-awesome.text-blue-500(:icon="['fas', 'info-circle']")
            span.pl-1 Más información
</template>

<page-query>
  query Productos {
    productos: allContentfulProducto {
      edges {
        node {
          id,
          title,
          date,
          main_image {
            title,
            file {
              url
            }
          },
          address,
          city,
          price,
          category,
          type,
          short_description,
          m2,
          bedrooms,
          bathrooms,
          garages
        }
      }
    }
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: "ProHabit"
  }
};
</script>

<style></style>
