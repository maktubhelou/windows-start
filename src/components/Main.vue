<template>
  <div>
    <div class="header">
      <div class="start">
        Start
      </div>
      <div class="user">
        Mark Evans
        <img src="@/assets/avatar.jpg" />
      </div>
    </div>
    <div class="grid-container">
      <div class="grid">
        <div
          v-for="tile in tiles"
          class="tile"
          :key="tile.title"
          :style="{
            background: `var(--${tile.bgColor}`,
            gridColumn: `span ${tile.width}`,
            gridRow: `span ${tile.height}`,
            backgroundImage: `url('${tile.image}')`,
            left: `${tile.sidebar === true && 'calc(90vw / 30)'}`,
            order: `${tile.index}`,
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat'
            }">
          <div class="icon">
          <i class="material-icons" :style="{fontSize: `${tile.height *24}px`}" >
            {{ tile.icon }}
          </i>
          </div>
          <div class="title">
          {{ tile.title }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
  data () {
    return {
      tiles: [
        {
          title: 'Desktop',
          height: 4,
          width: 4,
          bgColor: 'lightgreen',
          image: require('@/assets/cover.jpg'),
          icon: 'none'
        },
        {
          title: 'SkyDrive',
          width: 2,
          height: 2,
          bgColor: 'skydrive',
          image: '',
          icon: 'cloud'
        },
        {
          title: 'Maps',
          width: 2,
          height: 2,
          bgColor: 'maps',
          image: '',
          icon: 'map'
        },
        {
          title: 'Photos',
          width: 2,
          height: 2,
          bgColor: 'photos',
          image: '',
          icon: 'photo'
        },
        {
          title: '',
          width: 1,
          height: 1,
          bgColor: 'picture',
          image: '',
          icon: 'photo_camera'
        },
        {
          title: '',
          width: 1,
          height: 1,
          bgColor: 'music',
          image: '',
          icon: 'play_circle_filled'
        },
        {
          title: 'News',
          width: 4,
          height: 2,
          bgColor: 'news',
          image: '',
          icon: 'live_tv',
          sidebar: true
        },
        {
          title: '',
          width: 1,
          height: 1,
          bgColor: 'games',
          image: '',
          icon: 'gamepad'
        },
        {
          title: '',
          width: 1,
          height: 1,
          bgColor: 'camera',
          image: '',
          icon: 'camera'
        },
        {
          title: 'Calendar',
          width: 4,
          height: 2,
          bgColor: 'calendar',
          image: '',
          icon: 'calendar_today'
        },
        {
          title: 'Internet Explorer',
          width: 2,
          height: 2,
          bgColor: 'internetexplorer',
          image: '',
          icon: 'web'
        },
        {
          title: 'Help & Tips',
          width: 2,
          height: 2,
          bgColor: 'help-and-tips',
          image: '',
          icon: 'help'
        },
        {
          title: 'Food & Drink',
          width: 4,
          height: 2,
          bgColor: 'food-and-drink',
          image: '',
          icon: 'fastfood',
          sidebar: true
        },
        {
          title: 'Mail',
          width: 4,
          height: 2,
          bgColor: 'mail',
          image: '',
          icon: 'mail'
        },
        {
          title: 'Finance',
          width: 4,
          height: 2,
          bgColor: 'finance',
          image: '',
          icon: 'show_chart'
        },
        {
          title: 'Sports',
          width: 4,
          height: 2,
          bgColor: 'sports',
          image: '',
          icon: 'directions_run'
        },
        {
          title: 'Travel',
          width: 4,
          height: 2,
          bgColor: 'travel',
          image: '',
          icon: 'card_travel',
          sidebar: true
        },
        {
          title: 'People',
          width: 4,
          height: 2,
          bgColor: 'people',
          image: '',
          icon: 'people'
        },
        {
          title: 'Weather',
          width: 4,
          height: 2,
          bgColor: 'weather',
          image: '',
          icon: 'wb_sunny'
        },
        {
          title: 'Store',
          width: 4,
          height: 2,
          bgColor: 'store',
          image: '',
          icon: 'store'
        },
        {
          title: 'Reading List',
          width: 2,
          height: 2,
          bgColor: 'reading-list',
          image: '',
          icon: 'view_list',
          sidebar: true
        },
        {
          title: 'Health & Fitness',
          width: 2,
          height: 2,
          bgColor: 'health-and-fitness',
          image: '',
          icon: 'fitness_center',
          sidebar: true
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
