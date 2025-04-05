<template>
  <div class="mainContainer">
    <div class="parmaOffice">
      <p class="OfficeName">
        <img
            :src="office"
            alt="Office Icon"
        >
        Parma Office
      </p>
    </div>
    <div class="mainMenu">
      <p class="menuName">Основное меню</p>
      <button
          v-for="item in mainMenu"
          :key="item.label"
          :icon="item.icon"
          :label="item.label"
          class="btn"
      />
    </div>
    <div class="Admin">
      <p class="menuNameAdmin">Администрирование</p>
      <button
          v-for="item in adminMenu"
          :key="item.label"
          :icon="item.icon"
          :label="item.label"
          :isComplex="item.isComplex"
          class="btn"
      />
    </div>
    <div class="profile">
      <p class="NameSurname">Имя Фамилия</p>
      <p class="jobTitle">Должность/Роль</p>
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
import button from "@/components/UI/Button.vue";


export default {
  components: {
    button
  },
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
      mainMenu: [
        {icon: Map, label: 'Карта офиса'},
        {icon: reservation, label: 'Мои бронирования'},
        {icon: calendar, label: 'Календарь'},
        {icon: MyProfile, label: 'Мой профиль'},
      ],
      adminMenu: [
        {icon: settings, label: 'Управление картой'},
        {icon: statistik, label: 'Статистика'},
        {icon: sisAdminchiki, label: 'Управление\nпользователями', isComplex: true},
      ]
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');

* {
  font-family: 'Inter', sans-serif;
  padding: 0;
  margin: 0;
}

.mainContainer {
  width: 300px;
  height: 900px;
  background-color: #323e49;
}

.btn {
  background-color: #323e49;
  height: 60px;
  width: 300px;
  border: none;
  outline: none;
}

</style>