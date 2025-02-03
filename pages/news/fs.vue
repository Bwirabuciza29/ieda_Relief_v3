<template>
  <div>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi dicta animi
    accusamus illo placeat deserunt molestias tenetur hic, perspiciatis, dolore
    velit cum, nihil obcaecati? Aut recusandae suscipit praesentium quo animi!
  </div>
</template>
<script>
// first Slider
const totalPages = computed(() =>
  Math.ceil(articlesFiltres.value.length / articlesParPage)
);

const currentArticles = computed(() => {
  const start = (currentPage.value - 1) * articlesParPage;
  return articles.value.slice(start, start + articlesParPage);
});

const nextPage = () => {
  if (pageActuelle.value < nombreTotalPages.value) pageActuelle.value++;
};

const prevPage = () => {
  if (pageActuelle.value > 1) pageActuelle.value--;
};
</script>