<template>
  <div>
    <a :href="'https://www.youtube.com/watch?v=' + video.id.videoId" target="_blank">
      <img class="card-img-top" :src="video.snippet.thumbnails.medium.url" alt="YouTube thumbnail">
    </a>
    <div class="card-body">
      <h5 class="card-title">{{ video.snippet.title }}</h5>
      <h6
        class="card-subtitle mb-2 text-muted"
      >{{ video.snippet.channelTitle }} | {{ video.snippet.publishedAt | formatDate }}</h6>
      <p class="card-text">{{ video.snippet.description }}</p>
    </div>
  </div>
</template>

<GridList cellHeight={180} className={gridlist}>
  <GridListTitle key="Subheader" cols={2} style={{height: 'auto'}}>
   <ListSubheader component="div"></ListSubheader>
</GridListTile>

{tileData.map(tile => (
 <GridListTile key={tile.img}>
 <img src={tile.img} alt={tile.title}/>

))}

<script>
export default {
  name: 'VideoGridItem',
  props: ['video']
};
</script>