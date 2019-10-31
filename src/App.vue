<template>
  <div id="app"></div>
</template>

<script>
  export deafult{
    name: 'app',
    componentes:{},
    data(){
     return{
     videos:[],
     reformattedSearchString: '';
     api{
     baseUrl: 'https://www.googleapis.com/youtube/v3/search?',
     part: 'snippet',
     type: 'video',
     order: 'viewCount',
     maxResults: 12,
     q: '',
     key: 'AIzaSyDiM2IecFkkxiQABc81-AIHmXDi1o2Ei8o'
     prePageToken: '',
     nextPageToken: ''
      }
     };
   },

   methods:{}
    };
</script>