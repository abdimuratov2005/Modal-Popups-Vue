<template>
  <main class="modal">
    <div class="modal__container">
      <div class="alert">
        <h1>Alert</h1>
        <button type="button" @click="alertOne = !alertOne" class="btn">Alert #1</button>
        <button type="button" @click="alertTwo = !alertTwo" class="btn">Alert #2</button>
        <button type="button" @click="alertThree = !alertThree" class="btn">Alert #3</button>
        <button type="button" @click="alertFour = !alertFour" class="btn">Alert #4</button>
        <button type="button" @click="alertFive = !alertFive" class="btn">Alert #5</button>
        <button type="button" @click="alertSix = !alertSix" class="btn">Alert #6</button>

        <Transition>
          <div v-if="alertOne" class="alert-one">
            <div class="alert-one__container">
              <div @click="alertOne = !alertOne" class="close">
                <img :src="close">
              </div>
              <div class="alert-one__icon">
                <img :src="icon">
              </div>
              <div class="text">
                <h1 class="title">Successfully applied!</h1>
                <p class="content">Malesuada tellus tincidunt fringilla enim, id mauris. Id etiam nibh suscipit
                  aliquam dolor. Nunc sit nunc aliquet justo, facilisi leo. Nulla a eget tincidunt integer orci.</p>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="alertTwo" class="alert-two">
            <div class="alert-two__container">
              <div @click="alertTwo = !alertTwo" class="close">
                <img :src="close">
              </div>
              <h1 class="title">Project Successfully created!</h1>
              <p class="content">Malesuada tellus tincidunt fringilla enim, id mauris. Id etiam nibh suscipit
                aliquamdolor.</p>
              <a href="#" class="title link">
                Learn More
              </a>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="alertThree" class="alert-one">
            <div class="alert-one__container">
              <div @click="alertThree = !alertThree" class="close">
                <img :src="close">
              </div>
              <div class="alert-one__icon">
                <img :src="icon">
              </div>
              <div class="alert__text">
                <h1 class="title">Successfully applied!</h1>
                <p class="content">Malesuada tellus tincidunt fringilla enim, id mauris. Id etiam nibh suscipit
                  aliquam dolor.</p>
                <a href="#" class="title link">
                  Learn More
                </a>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="alertFour" class="alert-two">
            <div class="alert-two__container">
              <div @click="alertFour = !alertFour" class="close">
                <img :src="close">
              </div>
              <p class="content">Malesuada tellus tincidunt fringilla enim, id mauris. Id etiam nibh suscipit
                aliquamdolor.</p>
              <a href="#" class="title link">
                Learn More
              </a>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="alertFive" class="alert-one">
            <div class="alert-one__container">
              <div @click="alertFive = !alertFive" class="close">
                <img :src="close">
              </div>
              <div class="alert-one__icon">
                <img :src="icon">
              </div>
              <div class="alert__text">
                <p class="content">Malesuada tellus tincidunt fringilla enim, id mauris. Id etiam nibh suscipit
                  aliquam dolor.</p>
                <a href="#" class="title link">
                  Learn More
                </a>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="alertSix" class="alert-two">
            <div class="alert-one__container" style="align-items: center;">
              <div @click="alertSix = !alertSix" class="close">
                <img :src="close">
              </div>
              <div class="alert-one__icon">
                <img :src="icon">
              </div>
              <div class="alert__text">
                <p class="content">Malesuada tellus tincidunt fringilla enim, id mauris. Id etiam nibh suscipit
                  aliquam dolor.</p>
              </div>
            </div>
          </div>
        </Transition>
      </div>
      <div class="popups">
        <h1>Popups</h1>
        <button type="button" @click="popupOne = !popupOne" class="btn">Popup #1</button>
        <button type="button" @click="popupTwo = !popupTwo" class="btn">Popup #2</button>
        <button type="button" @click="popupThree = !popupThree" class="btn">Popup #3</button>

        <Transition>
          <div v-if="popupOne" class="popup">
            <div class="popup__container">
              <div @click="popupOne = !popupOne" class="close">
                <img :src="close">
              </div>
              <div class="text">
                <h1 class="title">Sure you want to accept?!</h1>
                <p class="content">Egestas arcu egestas parturient dui vitae. Ornare risus id ullamcorper in ut.
                  Vestibulum neque ullamcorper non orci vel, consectetur mi, pulvinar. Eu lectus quis leo viverra lacus
                  non fames est ut.</p>
              </div>
              <div class="popup__btn">
                <button @click="popupOne = !popupOne" class="popup-btn btn-no" type="button">No, cancel</button>
                <button @click="popupOne = !popupOne" class="popup-btn btn-confirm" type="button">Yes, confirm</button>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="popupTwo" class="popup">
            <div class="popup__container">
              <div @click="popupTwo = !popupTwo" class="close">
                <img :src="close">
              </div>
              <div class="text">
                <h1 class="title">Sure you want to accept?!</h1>
                <p class="content">Write your name</p>
                <input class="form" type="text" placeholder="Your Name">
              </div>
              <div class="popup__btn">
                <button @click="popupTwo = !popupTwo" class="popup-btn btn-no" type="button">No, cancel</button>
                <button @click="popupTwo = !popupTwo" class="popup-btn btn-confirm" type="button">Yes, confirm</button>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="popupThree" class="popup">
            <div class="popup__container">
              <div @click="popupThree = !popupThree" class="close">
                <img :src="close">
              </div>
              <div class="text">
                <h1 class="title">Terms and agreements</h1>
                <p class="content">Commodo eget a et dignissim dignissim morbi
                  vitae, mi. Mi aliquam sit ultrices enim cursus. Leo sapien, pretium duis est eu volutpat interdum eu
                  non. Odio eget nullam elit laoreet. Libero at felis nam at orci venenatis rutrum nunc. Etiam mattis
                  ornare pellentesque iaculis enim.<br><br>
                  Felis eu non in aliquam egestas placerat. Eget maecenas ornare venenatis lacus nunc, sit arcu. Nam
                  pharetra faucibus eget facilisis pulvinar eu sapien turpis at. Nec aliquam aliquam blandit eu ipsum.</p>
              </div>
              <div class="popup__btn">
                <button @click="popupThree = !popupThree" class="popup-btn btn-no" type="button">Nuuuu 😏</button>
                <button @click="popupThree = !popupThree" class="popup-btn btn-confirm" type="button">I agree</button>
              </div>
            </div>
          </div>
        </Transition>
      </div>
      <div class="modals">
        <h1>Modal</h1>
        <button type="button" @click="modalOne = !modalOne" class="btn">Modal #1</button>
        <button type="button" @click="modalTwo = !modalTwo" class="btn">Modal #2</button>
        <button type="button" @click="modalThree = !modalThree" class="btn">Modal #3</button>
        <button type="button" @click="modalFour = !modalFour" class="btn">Modal #4</button>
        <Transition>
          <div v-if="modalOne" class="alert-one">
            <div class="alert-one__container">
              <div @click="modalOne = !modalOne" class="close">
                <img :src="close">
              </div>
              <div class="alert-one__icon">
                <img :src="icon">
              </div>
              <div class="alert__text">
                <h1 class="title">Sure you want to accept?</h1>
                <p class="content">Are you sure you want to accept this?</p>
                <div class="popup__btn">
                  <button @click="modalOne = !modalOne" class="popup-btn btn-no" type="button">No, cancel</button>
                  <button @click="modalOne = !modalOne" class="popup-btn btn-confirm" type="button">Yes, confirm</button>
                </div>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="modalTwo" class="alert-one">
            <div class="alert-one__container">
              <div @click="modalTwo = !modalTwo" class="close">
                <img :src="close">
              </div>
              <div class="alert-one__icon">
                <img :src="icon">
              </div>
              <div class="alert__text">
                <h1 class="title">Sure you want to accept?</h1>
                <p class="content">Are you sure you want to accept this?</p>
                <div class="popup__btn">
                  <button @click="modalTwo = !modalTwo" class="popup-btn w-100 btn-confirm" type="button">Yes,
                    confirm</button>
                </div>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="modalThree" class="alert-one">
            <div class="alert-one__container center">
              <div @click="modalThree = !modalThree" class="close">
                <img :src="close">
              </div>
              <div class="alert__text">
                <h1 class="title">Sure you want to accept?</h1>
                <p class="content">Are you sure you want to accept this?</p>
                <div class="popup__btn">
                  <button @click="modalThree = !modalThree" class="popup-btn btn-no" type="button">No, cancel</button>
                  <button @click="modalThree = !modalThree" class="popup-btn btn-confirm" type="button">Yes, confirm</button>
                </div>
              </div>
            </div>
          </div>
        </Transition>
        <Transition>
          <div v-if="modalFour" class="smallPopup">
            <div class="alert-one__container">
              <div @click="modalFour = !modalFour" class="close">
                <img :src="close">
              </div>
              <div class="alert__text">
                <h1 class="title">Sure you want to accept?</h1>
                <p class="content">Are you sure you want to accept this?</p>
                <br>
                <div class="content"><input type="checkbox"> Don’t show this again</div>
                <div class="popup__btn">
                  <button @click="modalFour = !modalFour" class="popup-btn btn-no" type="button">No, cancel</button>
                  <button @click="modalFour = !modalFour" class="popup-btn btn-confirm" type="button">Yes, confirm</button>
                </div>
              </div>
            </div>
          </div>
        </Transition>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data: () => ({
    icon: '../public/icon.svg',
    close: '../public/close.svg',
    alertOne: false,
    alertTwo: false,
    alertThree: false,
    alertFour: false,
    alertFive: false,
    alertSix: false,
    popupOne: false,
    popupTwo: false,
    popupThree: false,
    modalOne: false,
    modalTwo: false,
    modalThree: false,
    modalFour: false,
  }),
}
</script>