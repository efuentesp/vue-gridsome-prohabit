<template lang="pug">
layout
  h1.text-3xl.font-bold.border-b Nuevos Desarrollos Habitacionales
  ProductList(:queryList="$page.productos.edges")
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
import ProductList from "~/components/ProductList.vue";

export default {
  metaInfo: {
    title: "Inicio"
  },
  components: {
    ProductList
  }
};
</script>

<style></style>
