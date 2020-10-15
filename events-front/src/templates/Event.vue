<template>
    <Layout>
        <h1>{{$page.event.title}}</h1>
        <img :src="`${$page.event.imageUrl}`"/>
        <p>{{$page.event.description}}</p>
    </Layout>
</template>

<page-query>
query {
  event(id: "4") {
    id
    title
    description
    price
    date
    imageUrl
  }
}
</page-query>

<script>
export default {
    metaInfo() {
        return {
            title: this.$page.event.title
        }
    }
}
</script>