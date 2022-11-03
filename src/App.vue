<script setup>
// import wrapper from './templates/wrapper.vue'
import { ref, onMounted } from 'vue'

// reactive state
const reg = ref(false)

// functions that mutate state and trigger updates
// function toggle() {
  //   if (reg.value) {
    //     reg.value = false
    //   } else {
      //     reg.value = true
      //   }
      // }
      function setReg() {
        reg.value = true
      }
      function unsetReg() {
        reg.value = false
      }
      
      // lifecycle hooks
      onMounted(() => {
        console.log(`The initial reg is ${reg.value}.`)
      })
</script>

<template>
  <div class="wrapper">
      <div class="wrapper__inner">
          <main class="content">
              <div class="form">
                  <img class="form__logo" src="./assets/images/logo.png" alt="" srcset="">
                  <div class="form__title">Форма входа пользователя киберспортивного клуба</div>
                  <form action="" class="form__body" v-if="reg">
                    <div>
                        <input type="text" placeholder="Логин">
                        <input type="text" placeholder="ФИО">
                    </div>
                    <div>
                        <input type="text" placeholder="Пароль">
                        <input type="text" placeholder="Подтверждение пароля">
                    </div>
                    <div>
                        <input type="text" placeholder="8 (777) 777 - 77 - 77">
                        <input type="text" placeholder="Email">
                    </div>
                  </form>
                  <form action="" class="form__body" v-else>
                    <div>
                        <input type="text" placeholder="Логин">
                        <input type="text" placeholder="Пароль">
                    </div>
                  </form>
                  <div class="form__checkboxes">
                      <div>
                          <input type="checkbox" name="fch" id="">
                          <label for="fch">Согласен(а) с правилами посещения комплекса клуба</label>
                      </div>
                      <div>
                          <input type="checkbox" name="sch" id="">
                          <label for="sch">Согласен(а) с политикой обработки персональных данных</label>
                      </div>
                  </div>
                  <div class="form__buttons">
                      <button @click="unsetReg" >Вход</button>
                      <button @click="setReg" >Регистрация</button>
                  </div>
                  <div class="form__ad">
                      <div class="f_ad__text">Скачайте приложение и получите бонус</div>
                      <div class="f_ad__body">
                          <div class="f_ad__app">
                              <img class="f_ad__qr" src="./assets/images/qr.png" alt="">
                              <img class="f_ad__img" src="./assets/images/apple_app.png" alt="">
                          </div>
                          <div class="f_ad__app">
                              <img class="f_ad__img" src="./assets/images/play_app.png" alt="">
                              <img class="f_ad__qr" src="./assets/images/qr.png" alt="">
                          </div>
                      </div>
                  </div>
              </div>
              <div class="number">
                  <span>88</span>
              </div>
          </main>
          <footer class="footer">
              <div class="footer__block">
                  <div class="f_block__title">Раскладка клавиатуры</div>
                  <div class="f_block__buttons">
                      <button><img src="./assets/images/russia.png" alt=""></button>
                      <button><img src="./assets/images/us.png" alt=""></button>
                  </div>
                  <div class="f_block__subtitle">
                      <div class="subtitle__text">
                          <span>*Для смены раскладки ввода</span><br>
                          <span>языка нажмите комбинацию клавиш</span>
                      </div>
                      <div class="subtitle__buttons">
                          <button>Alt</button>
                          <span>+</span>
                          <button>Shift</button>
                      </div>
                  </div>
              </div>
              <div class="footer__block">
                  <div class="footer__item">вы находитесь в зоне</div>
                  <div class="footer__item">standart</div>
              </div>
          </footer>
      </div>
  </div>
</template>
