<template>
  <div class="frame-1440w-dark">
    <div class="container">
      <div class="logo">
        <i class="fa-solid fa-building"></i>
      </div>
      <h1 class="heading">Parma Office</h1>
      <p class="subheading">Система бронирования рабочих мест</p>

      <div class="login-background">
        <h2 class="login-title">Вход в систему</h2>
        <p class="login-description">Введите ваш логин и пароль для входа</p>

        <form class="login-form">
          <div class="form-group">
            <label for="username">Логин</label>
            <div class="input-field">
              <input type="text" id="username" placeholder="Введите логин">
            </div>
          </div>

          <div class="form-group">
            <label for="password">Пароль</label>
            <div class="input-field">
              <input type="password" id="password" placeholder="Введите пароль">
            </div>
          </div>

          <button type="submit" class="login-button">Войти</button>
        </form>

        <p class="help-text">Для получения доступа к системе обратитесь в HR отдел</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {}

document.addEventListener('DOMContentLoaded', function() {
  const loginForm = document.querySelector('.login-form');

  loginForm.addEventListener('submit', function(event) {
    event.preventDefault();

    const username = document.getElementById('username').value;
    const password = document.getElementById('password').value;

    if (!username || !password) {
      alert('Пожалуйста, введите логин и пароль');
      return;
    }

    // Здесь будет код для отправки данных на сервер
    console.log('Выполняется вход:', { username, password });

    // Имитация успешного входа
    alert('Вход выполнен успешно!');
  });
});
</script>

<style scoped>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Arial, sans-serif;
}

body {
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Основной фрейм */
.frame-1440w-dark {
  width: 100%;
  height: 100vh;
  background-color: #f3f4f6;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Контейнер */
.container {
  width: 448px;
  max-width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
}

/* Логотип */
.logo {
  margin-bottom: 18px;
}

.logo i {
  font-size: 37px;
  color: #ec1c24;
}

/* Заголовок и подзаголовок */
.heading {
  font-size: 30px;
  color: #323e49;
  margin-bottom: 12px;
  font-weight: 600;
}

.subheading {
  font-size: 20px;
  color: #323e49;
  margin-bottom: 32px;
  text-align: center;
}

/* Фон формы входа */
.login-background {
  width: 100%;
  background-color: #ffffff;
  border: 1px solid #e7e5e4;
  border-radius: 10px;
  padding: 25px;
  box-shadow: 0 1px 5px rgba(0, 0, 0, 0.05);
}

/* Заголовок и описание формы */
.login-title {
  color: #323e49;
  font-size: 24px;
  margin-bottom: 12px;
  font-weight: 600;
}

.login-description {
  color: #93999f;
  font-size: 16px;
  margin-bottom: 30px;
}

/* Форма входа */
.login-form {
  margin-top: 44px;
  margin-bottom: 44px;
}

.form-group {
  margin-bottom: 22px;
}

.form-group label {
  display: block;
  color: #323e49;
  font-size: 14px;
  margin-bottom: 12px;
  font-weight: 500;
}

.input-field {
  width: 100%;
  height: 40px;
  border: 1px solid #e7e5e4;
  border-radius: 6px;
  display: flex;
  align-items: center;
  padding: 0 13px;
  background-color: white;
}

.input-field input {
  width: 100%;
  height: 100%;
  border: none;
  outline: none;
  color: #323e49;
  font-size: 14px;
}

.input-field input::placeholder {
  color: #777f86;
}

/* Кнопка входа */
.login-button {
  width: 100%;
  height: 40px;
  background-color: #ec1c24;
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 14px;
  font-weight: 500;
  cursor: pointer;
  margin-top: 14px;
}

.login-button:hover {
  background-color: #d01920;
}

/* Текст справки */
.help-text {
  color: #93999f;
  font-size: 14px;
  text-align: center;
  margin-top: 20px;
}

/* Адаптивность для мобильных устройств */
@media (max-width: 768px) {
  .container {
    width: 90%;
    padding: 0 15px;
  }

  .login-background {
    padding: 20px 15px;
  }

  .heading {
    font-size: 24px;
  }

  .subheading {
    font-size: 16px;
  }

  .login-title {
    font-size: 20px;
  }

  .login-description {
    font-size: 14px;
  }
}

@media (max-width: 480px) {
  .container {
    width: 95%;
  }

  .login-form {
    margin-top: 30px;
    margin-bottom: 30px;
  }

  .form-group {
    margin-bottom: 16px;
  }
}

</style>