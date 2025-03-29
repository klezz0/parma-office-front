<template>
  <div>
    <div class="container">
      <div class="parmaOffice">
        <img :src="office" rel="preload">
        <h4>Parma Office</h4>
      </div>
      <div class="mainMenu">
        <div class="menuName">Основное меню</div>
        <div class="map">
          <button class="btn">Карта офиса</button>
        </div>
        <div>
          <button class="btn">Мои бронирования</button>
        </div>
        <div>
          <button class="btn">Календарь</button>
        </div>
        <div>
          <button class="btn">Мой профиль</button>
        </div>
      </div>
      <div class="Admin">
        <div class="menuNameAdmin">Администрирование</div>
        <button class="btn">Управление картой</button>
        <button class="btn">Статистика</button>
        <button class="btn">Управление пользователями</button>
      </div>
    </div>
  </div>
</template>

<script>
import calendar from '@/assets/calendar.svg'
import dragsHere from '@/assets/dragsHere.svg'
import MyProfile from '@assets//MyProfile.svg'
import office from '@/assets/office.svg'
import settings from '@/assets/settings.svg'
import sisAdminchiki from '@assets//sisAdminchiki.svg'
import zakladochka from '@/assets/zakladochka.svg'

export default {
  data() {
    return {
      office,
      MyProfile,
      settings,
      sisAdminchiki,
      calendar,
      dragsHere,
      zakladochka,
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');

* {
  margin: 0;
  padding: 0;
  background-color: black;
}
.parmaOffice {
  display: flex;
}
.container {
  background: #323E49;
  width: 300px;
  height: 900px;
}

.parmaOffice {
  color: #FFFF;
  font-size: 36px;
}

.menuName {
  font-size: 14px;
  color: #93999F;
}

.menuNameAdmin {
  color: #93999F;
  font-size: 14px;
  margin-top: 40px;
  margin-bottom: 40px;
}

.btn {
  display: flex;
  justify-content: center;
  color: #FFFF;
  background-color: #323E49;
  height: 60px;
  width: 300px;
  text-align: left;
  border: none;
  outline: none;
}

</style>