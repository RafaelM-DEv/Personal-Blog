<template>
  <q-page class="row justify-center page-posts">
    <!-- pagina de post -->
    <div class="page-posts__list">
      <!-- titulo da página -->
      <h1>Blog</h1>
      <!-- lista de posts -->
      <div class="q-gutter-y-lg">
        <q-list v-for="(post, index) in posts" :key="index">
         <q-card>
          <q-card-section horizontal>
            <q-img  class="col-5"  :src="post.img" />
            <q-card-section>
              <div>
                <h6>{{ post.title }}</h6>
              </div>
              <div>
                {{ post.date }} | {{ post.category}}
              </div>
              <div>
                {{ post.description}}
              </div>
            </q-card-section>
           </q-card-section>
          </q-card>
        </q-list>
      </div>
    </div>
  </q-page>
</template>

<script>
const posts = [
  {
    title: 'Desiging Dashboards',
    date: '2022',
    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi nulla iste hic voluptate harum blanditiis architecto consectetur dolore reprehenderit eiu',
    category: 'Dahsboard',
    img: 'https://picsum.photos/200/150?random=1'
  },
  {
    title: 'Desiging Dashboards',
    date: '2022',
    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi nulla iste hic voluptate harum blanditiis architecto consectetur dolore reprehenderit eiu',
    category: 'Dahsboard',
    img: 'https://picsum.photos/200/150?random=2'
  },
  {
    title: 'Desiging Dashboards',
    date: '2022',
    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi nulla iste hic voluptate harum blanditiis architecto consectetur dolore reprehenderit eiu',
    category: 'Dahsboard',
    img: 'https://picsum.photos/200/150?random=3'
  },
  {
    title: 'Desiging Dashboards',
    date: '2022',
    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi nulla iste hic voluptate harum blanditiis architecto consectetur dolore reprehenderit eiu',
    category: 'Dahsboard',
    img: 'https://picsum.photos/200/150?random=4'
  }
]

export default {
  data () {
    return {
      name: 'postlist',
      posts
    }
  }
}
</script>

<style lang="scss">
.page-posts {
  &__list {
    width: 80%;
  }
}
</style>
