<template>
<div class="mdc-grid-list">
  <ul class="mdc-grid-list__tiles">
    <li class="mdc-grid-tile">

    <a :href="'https://www.youtube.com/watch?v=' + video.id.videoId" target="_blank">
      <img class="card-img-top" :src="video.snippet.thumbnails.medium.url" alt="YouTube thumbnail">
    </a>

      <div class="mdc-grid-tile__primary">
        <div class="mdc-grid-tile__primary-content my-tile-image"></div>
          <div class="card-body">
           <h5 class="card-title">{{ video.snippet.title }}</h5>
          <h6
        class="card-subtitle mb-2 text-muted"
      >{{ video.snippet.channelTitle }} | {{ video.snippet.publishedAt | formatDate }}</h6>
      <p class="card-text">{{ video.snippet.description }}</p>
    </div>
  </div>
      </div>
      <span class="mdc-grid-tile__secondary">
        <span class="mdc-grid-tile__title">Title</span>
      </span>
    </li>
  </ul>
</div>


    
    
</template>

<script>
export default {
  name: 'VideoGridItem',
  props: ['video']
};
</script>