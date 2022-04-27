<template>
  <div class="sidebar">
    <!-- プロフィール画像 -->
    <div class="sidebar-profile">
      <div class="sidebar-profile-container">
        <img class="sidebar-profile-img" src="../../assets/img2.jpeg">
        <div class="sidebar-profile-name">name-content</div>
      </div>
    </div>
    <!-- サイドバーメインコンテンツ -->
    <div class="sidebar-main-content">
      <div class="sidebar-main-item" v-for="item in sample_images" :key="item.index">
        <img class="sidebar-main-img" :src="require(`@/assets/${item.src}.png`)" alt="home">
        <div class="sidebar-main-name">{{ item.name }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sample_images: [
        {
          index: 0,
          src: 'home',
          name: 'home'
        },
        {
          index: 1,
          src: 'person',
          name: 'profile'
        },
        {
          index: 2,
          src: 'book',
          name: 'bookmark'
        },
        {
          index: 3,
          src: 'mail',
          name: 'messages'
        },
        {
          index: 4,
          src: 'search',
          name: 'search'
        }
      ]
    }
  }
}
</script>

<style scoped>
.sidebar {
  width: 15%;
  height: 100vh;
  background-color: white;
  border-right: 1px solid rgba(0,0,0,0.1);
}
/* プロフィール部分 */
.sidebar-profile {
  height: 200px;
  display: flex;
  align-items: center;
  padding-left: 15px;
}
.sidebar-profile-img {
  width: 75px;
  height: 75px;
  border-radius: 50%;
  object-fit: contain;
  cursor: pointer;
}
.sidebar-profile-name {
  padding-top: 5px;
  color: gray;
  font-size: 12px;
  font-weight: bold;
}
/* サイドバーメインコンテンツ */
.sidebar-main-item {
  
  height: 75px;
  border-bottom: 1px solid rgba(0,0,0,0.1);
  display: flex;
  align-items:flex-end;
  padding: 0 0 15px 15px;
  cursor: pointer;
}
.sidebar-main-img {
  width: 35px;
  height: 35px;
  object-fit: contain;
}
.sidebar-main-name {
  padding: 0 0 5px 35px;
  color: gray;
}
</style>