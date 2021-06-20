<template lang="html">
  <div>
    <button class="button" @click="showModal = true">Show Model</button>
    <transition name="fade" appear>
      <div
        class="modal-overlay"
        v-if="showModal"
        @click="showModal = !showModal"
      ></div>
    </transition>

    <transition name="slide" appear>
      <div class="modal" v-if="showModal">
        <h1>lorem Ipsum</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </p>
        <button class="button" @click="showModal = !showModal">
          Close Modal
        </button>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "box",
  data: () => ({
    showModal: "true",
  }),
};
</script>

<style>
.button {
  border: none;
  background: none;
  cursor: pointer;
  padding: 15px 25px;
  background-image: linear-gradient(to right, #cc2e5d, #ff5858);
  border-radius: 8px;
  color: #fff;
  font-size: 18px;
  font-weight: 700;
  cursor: pointer;
  box-shadow: 6px 6px rgba(0, 0, 0, 0.4);
}

.modal-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 98;
  background-color: rgba(0, 0, 0, 0.3);
}
.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 99;
  max-width: 400px;
  background-color: #fff;
  border-radius: 16px;
  padding: 25px;
}
h1 {
  margin-bottom: 15px;
}
.fade-enter-active,
.fade-leave-active {
  transition: 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.slide-enter-active,
.slide-leave-active {
  transition: 0.5s;
}
.slide-enter,
.slide-leave-to {
  transform: translateY(-50%) translateX(100vw);
}
</style>
