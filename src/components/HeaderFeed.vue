<script setup>
import { ref } from 'vue'

const username = ref("Spaceman")
const posts = ref(15)
const following = ref(101)
const followers = ref(102)
const bio = ref("Hey! This is my bio. This page is a simply project inspired in the UI of Pixelfed. Click on the refresh button to generate a new example account. There are many functionalities that doesn't work. Do not expect this to work the same as the real Pixelfed.")
const url = ref("https://pixelfed.es")
const registerDate = ref('10 August 2023')
</script>

<template>
  <div class="header">
    <div class="header-data">
      <img class="avatar-img" src="https://picsum.photos/150/150" alt="Imagen obtenida de manera aleatoria" />
      <div class="header-main">
        <div class="header-submain">
          <div class="header-info">
            <div class="header-info-name">
              <span class="username">{{ username }}</span>
              <span class="genderInfo">She / Her</span>
            </div>
            <span class="numberInfo">{{ posts }} posts</span>
            <span class="numberInfo">{{ following }} following</span>
            <span class="numberInfo">{{ followers }} followers</span>
          </div>
          <div class="header-options">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
              stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
              class="lucide lucide-ellipsis">
              <circle cx="12" cy="12" r="1" />
              <circle cx="19" cy="12" r="1" />
              <circle cx="5" cy="12" r="1" />
            </svg>
          </div>
        </div>
        <span class="bio">{{ bio }}</span>
        <div class="header-extra-info">
          <a href="https://pixelfed.es" class="extraInfo">{{ url }}</a>
          <span class="extraInfo">since {{ registerDate }}</span>
        </div>
      </div>
    </div>
  </div>

  <div class="mobile-header">
    <div class="mobile-header-main">
      <img class="avatar-img" src="https://picsum.photos/150/150" alt="Imagen obtenida de manera aleatoria" />
      <div class="mobile-header-submain">
        <div class="mobile-header-info-name">
          <span class="username">{{ username }}</span>
          <span class="genderInfo">She / Her</span>
        </div>
        <div class="mobile-header-data">
          <span class="mobile-numberInfo">{{ posts }} posts</span>
          <span class="mobile-numberInfo">{{ following }} following</span>
          <span class="mobile-numberInfo">{{ followers }} followers</span>
        </div>
      </div>
    </div>
    <span class="bio">{{ bio }}</span>
    <div class="mobile-header-extra-info">
      <a href="https://pixelfed.es" class="extraInfo">{{ url }}</a>
      <span class="extraInfo">since {{ registerDate }}</span>
    </div>
  </div>
</template>

<style scoped>
/* mobile */
.mobile-header {
  width: 100%;
  display: none;
  flex-direction: column;
  row-gap: 10px;
}

.mobile-header-options {
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  justify-content: center;
  align-items: center;
  margin-right: 20px;
}

.mobile-header-data {
  display: flex;
  gap: 5px;
  font-size: small;
}

.mobile-header-extra-info {
  display: flex;
  justify-content: space-between;
}

.mobile-header-main {
  display: flex;
  column-gap: 10px;
}

.mobile-header-submain {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.mobile-header-info {
  display: flex;
  flex-direction: column;
  justify-content: start;
  column-gap: 20px;
  align-items: baseline;
}

.mobile-header-info-name {
  display: flex;
  justify-content: start;
  column-gap: 5px;
  align-items: baseline;
}

.mobile-avatar-img {
  border-radius: 100px;
}

.numberInfo {
  font-size: small;
}

/* pc */
.header {
  width: 90%;
  margin-left: 10px;
  margin-right: 10px;
  display: flex;
  justify-content: space-between;
}

.header-options {
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  justify-content: center;
  align-items: center;
  margin-right: 20px;
}

.header-data {
  display: flex;
  gap: 50px;
}

.header-extra-info {
  display: flex;
  justify-content: space-between;
}

.header-main {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.header-submain {
  display: flex;
  justify-content: space-between;
}

.header-info {
  display: flex;
  justify-content: start;
  column-gap: 20px;
  align-items: baseline;
}

.header-info-name {
  display: flex;
  justify-content: start;
  column-gap: 5px;
  align-items: baseline;
}

.avatar-img {
  border-radius: 100px;
}

.bio {
  font-size: medium;
}

.username {
  font-weight: bolder;
  font-size: x-large;
}

.numberInfo {
  font-size: medium;
}

.extraInfo {
  color: rgb(121, 117, 111);
}

.genderInfo {
  color: rgb(121, 117, 111);
  font-size: small;
}

img {
  width: 200px;
  height: 200px;
}

@media (width < 1000px) {
  img {
    width: 100px;
    height: 100px;
  }

  .header {
    display: none;
  }

  .mobile-header {
    display: flex;
  }

}
</style>
