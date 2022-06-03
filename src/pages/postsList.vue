<template>
  <q-page class="page_post-list flex justify-center">
    <div class="page_post-list__list">
      <div class="text-h1 q-py-lg">Blog</div>
      <div class="q-my-lg">
        <!-- lista de posts -->
        <q-list class="q-gutter-y-md">
          <div v-for="(post, index) in postList" :key="index">
            <q-card flat>
              <q-card-section horizontal>
                <div class="q-mr-md">
                  <q-img :src="post.img" style="width: 150px"/>
                </div>
                <div class="column">
                  <div class="text-bold text-h6 q-mb-sm">
                    {{ post.title }}
                  </div>
                  <div>
                    {{ post.category }}
                  </div>
                  <div>
                    {{ post.description }}
                  </div>
                </div>
              </q-card-section>
            <q-separator color="grey-5" class="q-mt-md"/>
            </q-card>
          </div>
        </q-list>
      </div>
    </div>
  </q-page>

</template>

<script>
const postList = [
  {
    title: 'Lorem, ipsum dolor.',
    img: 'https://picsum.photos/300/300?random=1',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam velit quasi, maxime nobis minus sint ut tenetur nulla exercitationem recusandae.',
    category: 'Dashboard'
  },
  {
    title: 'Lorem, ipsum lwesd.',
    img: 'https://picsum.photos/300/300?random=2',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam velit quasi, maxime nobis minus sint ut tenetur nulla exercitationem recusandae.',
    category: 'Dashboard'
  },
  {
    title: 'Lorem, ipsum casrac.',
    img: 'https://picsum.photos/300/300?random=3',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam velit quasi, maxime nobis minus sint ut tenetur nulla exercitationem recusandae.',
    category: 'Dashboard'
  },
  {
    title: 'Lorem, ipsum Asdavca.',
    img: 'https://picsum.photos/300/300?random=4',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam velit quasi, maxime nobis minus sint ut tenetur nulla exercitationem recusandae.',
    category: 'Dashboard'
  },
  {
    title: 'Lorem, ipsum Casddaer.',
    img: 'https://picsum.photos/300/300?random=5',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam velit quasi, maxime nobis minus sint ut tenetur nulla exercitationem recusandae.',
    category: 'Dashboard'
  }
]

export default {
  data () {
    return {
      postList,
      name: 'PostList'
    }
  }
}
</script>

<style lang="scss">
.page_post-list {
  &__list{
    width: 80%;
  }
}
</style>
