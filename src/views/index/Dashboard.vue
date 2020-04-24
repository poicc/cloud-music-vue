<template>
  <div>
    <b-carousel :indicator-inside="false">
      <b-carousel-item v-for="(item, i) in 6" :key="i">
        <span class="image">
          <img :src="getImgUrl(i)" />
        </span>
      </b-carousel-item>
      <template slot="indicators" slot-scope="props">
        <span class="al image">
          <img :src="getImgUrl(props.i)" :title="props.i" />
        </span>
      </template>
    </b-carousel>

    <div class="columns">
      <div class="column" style="margin-top:20px;">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              Component
            </p>
            <a href="#" class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </a>
          </header>
          <div class="card-content">
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit .
              <br />
              <time datetime="2016-1-1">02:09 PM - 22 Jan 2020</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">Save</a>
            <a href="#" class="card-footer-item">Edit</a>
            <a href="#" class="card-footer-item">Delete</a>
          </footer>
        </div>
      </div>
      <div class="column" style="margin-top:20px;">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              Component
            </p>
            <a href="#" class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </a>
          </header>
          <div class="card-content">
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              <br />
              <time datetime="2016-1-1">07:09 PM - 1 Jan 2020</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">Save</a>
            <a href="#" class="card-footer-item">Edit</a>
            <a href="#" class="card-footer-item">Delete</a>
          </footer>
        </div>
      </div>
      <div class="column" style="margin-top:20px;">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              Component
            </p>
            <a href="#" class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </a>
          </header>
          <div class="card-content">
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              <br />
              <time datetime="2016-1-1">12:09 PM - 1 Jan 2020</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">Save</a>
            <a href="#" class="card-footer-item">Edit</a>
            <a href="#" class="card-footer-item">Delete</a>
          </footer>
        </div>
      </div>
      <div class="column" style="margin-top:20px;">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              Component
            </p>
            <a href="#" class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </a>
          </header>
          <div class="card-content">
            <div class="content">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              <br />
              <time datetime="2016-1-1">21:39 PM - 1 Jan 2020</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">Save</a>
            <a href="#" class="card-footer-item">Edit</a>
            <a href="#" class="card-footer-item">Delete</a>
          </footer>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  data: () => ({
    show: false,
    items: [
      {
        color: '#1F7087',
        src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
        title: 'Supermodel',
        artist: 'Foster the People'
      },
      {
        color: '#952175',
        src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
        title: 'Halcyon Days',
        artist: 'Ellie Goulding'
      }
    ]
  }),
  methods: {
    getImgUrl(value) {
      return `https://picsum.photos/id/43${value}/1230/500`
    }
  }
}
</script>

<style>
.is-active .al img {
  filter: grayscale(0%);
}
.al img {
  filter: grayscale(100%);
}
</style>
