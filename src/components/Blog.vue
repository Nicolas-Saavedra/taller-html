<template>
  <main>
    <div class="posts container-fluid">
      <div class="post row justify-content-center" v-for="post in posts" :key="post.title">
          <div class="col-md-6">
          <h2 class="title" v-html="post.title"></h2>
          <h3 class="date" v-html="post.date"></h3>
          <p class="content" v-html="post.content"></p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>

.posts {
  margin-bottom: 2rem;
  padding: 2rem 0;
}

/* post class centered on screen with 80vw width, some top margin space, and padding */
.post {
  margin-top: 1.5rem;
  padding: 2rem;
}

/* title class with some bottom margin space */
.title {
  font-size: 3rem;
  margin-bottom: 0.5rem;
}

/* date class with some bottom margin space */
.date {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

/* content class with some top margin space */
.content {
  font-size: 1.5rem;
  margin-top: 0.5rem;
}

</style>

<script setup lang="ts">

const posts = [
  {
    title: 'My first post',
    date: '2021-08-01',
    content: `
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <a href="http://www.script-o-rama.com/movie_scripts/a1/bee-movie-script-transcript-seinfeld.html">Read more</a>`
  },
  {
    title: 'My second post',
    date: '2021-08-02',
    content: `
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <a href="http://www.script-o-rama.com/movie_scripts/a1/bee-movie-script-transcript-seinfeld.html">Read more</a>`
  },
  {
    title: 'My third post',
    date: '2021-08-03',
    content: `
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl ut
        aliquam tincidunt, nunc nisl aliquam mauris, eget aliquam nunc nunc vel
        mauris. Sed euismod, nisl ut aliquam tincidunt, nunc nisl aliquam mauris,
        eget aliquam nunc nunc vel mauris.
      </p><a href="http://www.script-o-rama.com/movie_scripts/a1/bee-movie-script-transcript-seinfeld.html">Read more</a>`
  }
];
</script>
