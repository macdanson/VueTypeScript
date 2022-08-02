<template>
  <div class="container mt-4">
    <div class="row d-flex justify-content-between">
    <div class="col">
      <h3>Most Recent Posts</h3>
    </div>
    </div>
    <PostList :posts="posts"/>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue';
import Post from './data-types/Posts'
import PostList from './components/Posts.vue'

export default defineComponent({
  name: 'App',
  components: {PostList},
  // ======== This is the OPTIONS method ==========
  // data(){
  //   return{
  //     name: 'Link',
  //     age: 30,
  //     location: 'Kampala, Uganda'
  //   }
  // },

  // ========= This the COMPOSITION API method ===============
  setup(){
    // ++++++++++Composition API by Reactive++++++++++++++++++
    // const state = reactive({
      // age: 30 as number | string,
    //   name: 'Link',
    //   location: 'Kampala, Uganda'
    // })

    // // To chage the defauld value of any thing in the SETUP above
    // state.age = 80
    // state.location = 'Biguli, Kamwenge'
    // state.name = 'Geremaya Kamurare'

    // return { ...toRefs(state)}

    // ++++++++++Composition API by Refs ++++++++++++++++++
    // const name = ref('Link Name')
    // const age = ref<number | string>(67)
    // const location = ref('Rwamwanja Kamwenge')

    // return { name, age, location}

    const posts = ref<Post[]>([
      {
      "id": 500,
      "title": "Voluptas enim nesciunt consequatur ut.",
      "body": "Sed dolorum rerum quisquam est assumenda ratione magnam consequatur. Ut est omnis suscipit velit dolores eius enim blanditiis. Voluptatem ex id repellendus similique eveniet illo. Qui et et excepturi laudantium omnis.",
      "type": "text",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "tempore",
      "author": "Tremaine Orn"
    },
    {
      "id": 499,
      "title": "Voluptas repellat et voluptas ullam iste.",
      "body": "Ad sit doloremque occaecati aliquid eos quo. Nesciunt eveniet reiciendis minima ab ea nisi. Quod autem alias nobis velit omnis porro. Officiis enim voluptatem exercitationem nulla magnam.",
      "type": "text",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "quasi",
      "author": "Lilla Johns"
    },
    {
      "id": 498,
      "title": "Et vero ea quo eius placeat ducimus.",
      "body": "Quod dolore hic ratione omnis ut quaerat inventore tenetur. Et delectus optio iste architecto nesciunt sint. Ab reprehenderit quia quibusdam autem. Aliquid laboriosam nihil provident repellat harum sapiente laboriosam.",
      "type": "text",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "omnis",
      "author": "James Ganner",
    },
    {
      "id": 497,
      "title": "Velit adipisci consectetur quibusdam quisquam.",
      "body": "Cum voluptas provident qui occaecati. Ex incidunt et laboriosam et sit voluptate. Omnis aut debitis ut dicta velit modi sint.",
      "type": "text",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "quasi",
      "author": "Zola Fahey"
    },
    {
      "id": 496,
      "title": "Error ut optio mollitia.",
      "body": "Culpa voluptatum quos nam laborum dolores corrupti quis. Quis excepturi laborum doloremque vitae quidem. Aspernatur quis blanditiis magni et iure.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "incidunt",
      "author": "Ivah Howe"
    },
    {
      "id": 495,
      "title": "Similique quidem doloribus placeat corporis.",
      "body": "Quo similique repudiandae aliquam voluptatem impedit iste vel. Assumenda ad facilis quasi vel delectus quia reprehenderit quam. Facilis omnis et voluptatum quasi. Vero molestiae totam neque laudantium.",
      "type": "text",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "velit",
      "author": "null"
    },
    {
      "id": 494,
      "title": "Animi fugiat totam et eligendi modi sunt voluptas odit.",
      "body": "Corporis earum vel voluptatem itaque earum et similique. Fugiat quod cupiditate eos eaque atque asperiores officiis. Eaque accusamus ipsum veniam nesciunt commodi iusto. Dolores corrupti non quia rem.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "iste",
      "author": "Muhammad Lebsack"
    },
    {
      "id": 493,
      "title": "Repellendus porro dolorum quae quis suscipit eum.",
      "body": "Voluptas nam a soluta voluptatem dolore unde hic. Libero officiis est libero ea. Vitae dignissimos aut ratione sit sapiente laboriosam. Nobis quia vero architecto deleniti aut repellat minima pariatur.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "iste",
      "author": "Quincy Wisoky V"
    },
    {
      "id": 492,
      "title": "At itaque atque consequatur.",
      "body": "Eos aut vel illum non officia. Minus ut dolorem voluptatem voluptatum ea magnam odio. Eos sed laboriosam tempora ratione perferendis quibusdam ea. Deserunt quos expedita atque tempore.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "category",
      "author": "null"
    },
    {
      "id": 491,
      "title": "Nisi optio est delectus.",
      "body": "Voluptate sunt earum tenetur ut ipsa. Sequi alias eum in aperiam occaecati dolorum libero. Suscipit maiores perspiciatis accusamus assumenda ea hic.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "placeat",
      "author": "null"
    },
    {
      "id": 490,
      "title": "Aut voluptas praesentium quasi error quam.",
      "body": "Quo dolorum esse quod et. Commodi et consequuntur rerum optio qui voluptatem. Mollitia quo possimus dicta assumenda qui cumque sit.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "placeat",
      "author": "placeat"
    },
    {
      "id": 489,
      "title": "Eaque consequatur optio qui sed sunt aliquid aut.",
      "body": "Quo voluptas rerum architecto odit. Praesentium molestiae et ea et dolores. Delectus neque iure sed ducimus. Veritatis consequatur provident velit voluptatem facere a.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "placeat",
      "author": "Tyra Schaden IV"
    },
    {
      "id": 488,
      "title": "Officia vel cupiditate aspernatur quaerat.",
      "body": "Ea ut id fugit. Nemo blanditiis tenetur commodi at ex. Id cum consequatur culpa facere deserunt. Est voluptas dolor non debitis rem et nulla.",
      "type": "text",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "tempore",
      "author": "Elissa Daniel"
    },
    {
      "id": 487,
      "title": "Est omnis optio atque.",
      "body": "Quas sed sint velit accusantium. Vitae rem est exercitationem modi. Rerum natus magni dolorum dignissimos.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "quod",
      "author": "Chauncey O'Reilly"
    },
    {
      "id": 486,
      "title": "Quasi voluptates aut optio libero.",
      "body": "Voluptatum tempore ut omnis aut laudantium velit et. Nobis earum vel vero velit quis excepturi. Et repellendus expedita quisquam ut. Eaque labore et nulla rerum ipsum.",
      "type": "video",
      "updated_at": "19/07/2022 | 09:07:44",
      "category": "placeat",
      "author": "Prof. Rick Boyle Sr."
    },
    ])

    return {posts}
  },

  
});
</script>

<style>
</style>
