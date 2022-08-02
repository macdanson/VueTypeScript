<template>
    <div class="posts">
    <div class="card mb-2" v-for="(post, index) in posts" :key="index">
  <div class="card-body">
    <h5 class="card-title">{{ index+1 }}. {{ post.title}} </h5>
    <p class="card-text">{{ post.body}}</p>
  </div>
  <div class="card-footer">
    <div class="row d-flex justify-content-center">
    <div class="col">
      <small class="text-muted">Posted by: <strong>{{ post.author }}</strong></small>
    </div>
    <div class="col">
      <small class="text-muted">Posted at: <strong>{{ post.updated_at}}</strong></small>
    </div>
    <div class="col">
      <small class="text-muted">Category: <strong>{{ post.category }}</strong></small>
    </div>
    <div class="col">
      <small class="text-muted">Post Type: <strong>{{ post.type }}</strong></small>
    </div>
  </div>
</div>
</div>
    </div>
</template>
<script lang="ts">
import Post from '@/data-types/Posts'
import { defineComponent, PropType } from 'vue'

export default defineComponent({
    name: 'PostList',
    props:{
        posts:{
            require: true,
            type: Array as PropType<Post[]>
        },
    }
})
</script>
