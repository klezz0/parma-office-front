<template xmlns="http://www.w3.org/1999/html">
  <div>
    <div class="container">
      <div class="content">
        <div class="parmaOffice">
          <p class="OfficeName">
            <img :src="office" rel="preload">
            Parma Office
          </p>
        </div>
        <div class="mainMenu">
          <div class="menuName">Основное меню</div>
          <div class="map">
            <button class="btn">
              <img :src="Map" rel="preload">
              Карта офиса
            </button>
          </div>
          <div>
            <button class="btn">
              <img :src="reservation" rel="preload">
              Мои бронирования
            </button>
          </div>
          <div>
            <button class="btn">
              <img :src="calendar" rel="preload">
              Календарь
            </button>
          </div>
          <div>
            <button class="btn">
              <img :src="MyProfile" rel="preload">
              Мой профиль
            </button>
          </div>
        </div>
        <div class="Admin">
          <div class="menuNameAdmin">Администрирование</div>
          <button class="btn">
            <img :src="settings" rel="preload">
            Управление картой
          </button>
          <button class="btn">
            <img :src="statistik" rel="preload">
            Статистика
          </button>
          <button class="btn">
            <div class="sisAdminchiki">
              <img :src="sisAdminchiki" rel="preload">
              Управление <br>пользователями
            </div>
          </button>
        </div>
        <div class="profile">
          <p class="NameSurname">Имя Фамилия</p>
          <p class="JobTitle">Должность/Роль</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import calendar from '@/assets/calendar.svg'
import Map from '@/assets/Map.svg'
import MyProfile from '@/assets/MyProfile.svg'
import office from '@/assets/office.svg'
import settings from '@/assets/settings.svg'
import sisAdminchiki from '@/assets/sisAdminchiki.svg'
import reservation from '@/assets/reservation.svg'
import statistik from '@/assets/statistik.svg'

export default {
  data() {
    return {
      office,
      MyProfile,
      settings,
      sisAdminchiki,
      calendar,
      Map,
      reservation,
      statistik,
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');

* {
  margin: 0;
  padding: 0;
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  font-weight: 400;
}

.content {
  margin-left: 14px;
}

.container {
  background: #323E49;
  width: 300px;
  height: 900px;
}

.parmaOffice {
  display: flex;
  color: #FFFF;
  font-size: 36px;
  background-color: #323E49;
  border-bottom: #232D35 1px solid;
}

.OfficeName {
  background-color: #323E49;
  color: #FFFF;
  font-size: 28px;
  font-weight: bold;
  margin-top: 16px;
  margin-bottom: 20px;
}

.menuName {
  color: #93999F;
}

.menuNameAdmin {
  color: #93999F;
  font-size: 14px;
  margin-top: 59px;
  margin-bottom: 38px;
  background-color: #323E49;
}

.menuName {
  margin-top: 14px;
  margin-bottom: 15px;
  background-color: #323E49;
}

.mainMenu {
  background-color: #323E49;
}

.Admin {
  background-color: #323E49;
}

img {
  height: 22px;
  width: 22px;
  background-color: #323E49;
  margin-right: 10px;
}

p {
  color: #93999F;
  background-color: #323E49;
}

.NameSurname {
  color: #FFFF;
}

.profile {
  display: flex;
  flex-direction: column;
  border-top: #232D35 1px solid;
}

.sisAdminchiki {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 40px;
}


</style>