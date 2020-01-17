<template lang="pug">
layout
  article.product-teaser.mt-8
    div.pr-2(class="w-1/2")
      g-image.border-8.border-solid.border-white.shadow-xl(:src="$page.producto.main_image.file.url")
    div.pl-2(class="w-1/2")
      h2.text-2xl.font-bold.text-teal-500.underline {{$page.producto.title}}
      div.text-gray-700
        h3.mt-2 {{$page.producto.address}}
        h3.font-bold.mb-3 {{$page.producto.city}}
      span.rounded.bg-teal-500.text-xl.text-white.font-bold.p-2 {{$page.producto.price}}
      .flex.mt-3
        span.border.border-green-400.rounded.px-2.py-1.text-green-600.mr-2 {{$page.producto.category}}
        span.border.border-blue-400.rounded.px-2.py-1.text-blue-500 {{$page.producto.type}}
      p.mt-3.text-justify {{$page.producto.short_description.content[0].content[0].value}}
      .flex.justify-between.items-center.mt-3
        .flex
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'home']")
            span.pl-1 {{$page.producto.m2}} m
            sup 2
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'bed']")
            span.pl-1 {{$page.producto.bedrooms}}
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'bath']")
            span.pl-2 {{$page.producto.bathrooms}}
          span.tag-property-features.mr-2
            font-awesome(:icon="['fas', 'car']")
            span.pl-2 {{$page.producto.garages}}
</template>

<page-query>
query Producto($id: ID) {
  producto: contentfulProducto(id: $id) {
    id
    title
    date
    createdAt
    updatedAt
    locale
    name
    category
    short_description
    status
    price
    address
    city
    type
    bedrooms
    bathrooms
    m2
    garages
    main_image {
      title
      file {
        url
      }
    }
    map_image {
      title
      file {
        url
      }
    }
    photos {
      title
      file {
        url
      }
    }
    long_description
    belongsTo {
      edges {
        node {
          id
        }
      }
    }
  }
}
# Write your query or mutation here
</page-query>

<script>
export default {
  metaInfo: {
    title: "Propiedad"
  }
};
</script>

<style></style>
