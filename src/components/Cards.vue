<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col card">
        <img src="#" class="card-img-top" alt=""/>
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <p class="card-text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto reiciendis distinctio similique cumque modi aut rem autem blanditiis cum! Veniam fuga facilis voluptates blanditiis dolor aut adipisci nesciunt enim tempore, illum labore repudiandae deleniti, totam esse laborum culpa eaque, itaque autem praesentium corporis quo? Nulla debitis ratione fugiat maxime quae?
          </p>
          <ul>
            <li>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolorum modi aliquid distinctio cum, porro molestias vero dolores ea recusandae labore. Nihil sunt molestias quas incidunt unde consequuntur libero sint porro?</li>
            <li>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolorum modi aliquid distinctio cum, porro molestias vero dolores ea recusandae labore. Nihil sunt molestias quas incidunt unde consequuntur libero sint porro?</li>
            <li>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolorum modi aliquid distinctio cum, porro molestias vero dolores ea recusandae labore. Nihil sunt molestias quas incidunt unde consequuntur libero sint porro?</li>
          </ul>
        </div>
      </div>
      <div class="col card">
        <img src="#" class="card-img-top" alt=""/>
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <p class="card-text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto reiciendis distinctio similique cumque modi aut rem autem blanditiis cum! Veniam fuga facilis voluptates blanditiis dolor aut adipisci nesciunt enim tempore, illum labore repudiandae deleniti, totam esse laborum culpa eaque, itaque autem praesentium corporis quo? Nulla debitis ratione fugiat maxime quae?
            <br><br>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum, obcaecati! Error maiores animi, nostrum dolorem earum sint adipisci laborum sed suscipit ad alias rem vitae dolor a porro ea velit.
            <br><br>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel dignissimos tempora sequi, ad, exercitationem eveniet hic placeat officiis velit voluptatibus perspiciatis atque facilis! Praesentium, maxime ut voluptates voluptas blanditiis neque.
          </p>
        </div>
      </div>
      <div class="col card">
        <img src="#" class="card-img-top" alt=""/>
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <p class="card-text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto reiciendis distinctio similique cumque modi aut rem autem blanditiis cum! Veniam fuga facilis voluptates blanditiis dolor aut adipisci nesciunt enim tempore, illum labore repudiandae deleniti, totam esse laborum culpa eaque, itaque autem praesentium corporis quo? Nulla debitis ratione fugiat maxime quae?
            <br><br>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum, obcaecati! Error maiores animi, nostrum dolorem earum sint adipisci laborum sed suscipit ad alias rem vitae dolor a porro ea velit.
            <br><br>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel dignissimos tempora sequi, ad, exercitationem eveniet hic placeat officiis velit voluptatibus perspiciatis atque facilis! Praesentium, maxime ut voluptates voluptas blanditiis neque.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.row {
  margin-top: 2rem;
}
.card {
  margin: 1rem;
  margin-bottom: 0;
}

.card-title {
  font-size: 2rem;
  font-weight: 600;
}

.card-img-top {
  height: 25rem;
  object-fit: cover;
}

</style>

<script setup lang="ts">
import { onMounted } from 'vue';
import axios from 'axios';

type Result = {
  id: string;
  url: string;
};



onMounted(async () => {
  const cards = Array.from(document.getElementsByClassName('card-img-top')) as HTMLImageElement[];
  const urls : Result[] = (await axios.get('https://api.thecatapi.com/v1/images/search?limit=3&page=100&order=DESC?category_ids=7?api_key=live_LbeQXW21MqZvQg7IUTJOvkXjCLl8bpJLPb9m3pzyV4yzEq4Pir1JqpkD2ygVcZQC')).data
  urls.forEach((url, i) => {
    cards[i].src = url.url;
  });
});

</script>

