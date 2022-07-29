<template>
  <div>
    <section class="profile">
      <div class="profile_title">
        <div>
          <a :href='userLink' target="_blank" rel="noopener noreferrer">
            <img :src='user.profile_image' :alt='user.name' draggable="false">
          </a>
          <p>Joined at {{ user.joined_at }}</p>
        </div>
        <div>
          <h1>{{ user.name }}</h1>
          <h2>{{ user.summary }}</h2>
        </div>
      </div>
    </section>
    <div class="grid">
      <a v-for='post in posts' :key='post' class="card" :href='post.url'>
        <img :src="post.social_image" :alt='post.title' class="card__image" draggable="false">
        <div class="card__content">
          <h3 class="card__title">{{ post.title }}</h3>
          <p class="card__desc">{{ post.description }}</p>
          <p class="card__date">{{ formatDate(post.published_timestamp) }}</p>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
const USERID_DEVTO = '18254'
const USERNAME_DEVTO = 'thomasbnt'

export default {
  name: 'devto',
  data() {
    return {
      posts: {
        data: []
      },
      user: {
        user: {}
      },
      userLink: `https://dev.to/${USERNAME_DEVTO}`
    }
  },
  mounted() {
    fetch(`https://dev.to/api/articles?username=${USERNAME_DEVTO}&per_page=100`)
        .then(res => res.json())
        .then(data => {
          this.posts = data
        })
        .catch(error => console.log(error))
    fetch(`https://dev.to/api/users/${USERID_DEVTO}`)
        .then(res => res.json())
        .then(data => {
          document.title = `${data.username} on dev.to`
          document.querySelector('link[rel="icon"]').href = data.profile_image
          this.user = data
        })
        .catch(error => console.log(error))
  },
  methods: {
    formatDate(date) {
      const options = {year: 'numeric', month: 'long', day: 'numeric'}
      return new Date(date).toLocaleDateString('en', options)
    }
  }
}
</script>
<style scoped>
h1 {
  font-size: 2rem;
  text-transform: uppercase;
  margin: unset;
}
h2 {
  font-size: 1.3rem;
  line-height: 1.8rem;
}
.profile_title {
  display: flex;
  align-items: center;
  margin: 1rem auto;
  background-color: #f7f7f7;
  border-radius: 5px;
}
@media screen and (max-width: 768px) {
  .profile_title {
    flex-direction: column;
    margin: 0 auto;
  }
  .profile_title > div:last-of-type {
    text-align: center;
  }
}
.profile_title > div {
  margin: 1rem;
}
.profile_title > div:first-of-type {
  margin-right: 1rem;
  text-align: center;
}

.profile_title h1, .profile_title h2, .profile_title p {
  font-weight: 100;
}

.profile_title img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-right: 1rem;
  transition: .3s;
}
.profile_title img:hover {
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 2rem;
  margin: 1rem auto;
  padding-bottom: 3rem;
}

.card {
  display: flex;
  flex-direction: column;
  color: #262626;
  text-decoration: none;
  border-radius: 5px;
}
.card__image {
  border-radius: 5px 5px 0 0;
}
.card,
.card:hover .card__image {
  transition: .3s;
}

.card:hover {
  background-color: #f7f7f7;
  box-shadow: 2px 2px 4px #26262636;
}

.card:hover .card__image {
  filter: brightness(0.8);
}

.card__image {
  width: 100%;
}

.card__content {
  display: flex;
  flex-direction: column;
  padding: 1rem;
  flex-grow: 1;
}

.card__title {
  font-size: 1.5rem;
  font-weight: bold;
}

.card__desc {
  flex-grow: 1;
  font-size: 1.2rem;
  line-height: 1.8rem;
}

.card__date {
  font-size: 0.8rem;
}

</style>
