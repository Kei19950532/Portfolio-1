<template>
  <div>
    <h2>モーダルウィンドウ</h2>
    <button class="btn01" v-on:click='showModal=!showModal'>モーダルひらく</button>
    <transition name="modal">
      <div class="modal" v-if='showModal'>
        <div class="modal_inner">
          <p>モーダルサンプルです。</p>
          <a class="close" href="#" v-on:click='click01'>×</a>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
    data(){
      return {
        showModal: false
      }
    },methods: {
      click01: function (ev) {
        this.showModal = false
        ev.preventDefault()
      }
    }
}
</script>

<style>
.modal-enter-active, .modal-leave-active {
  transition:opacity 0.5s;
}
.modal-enter, .modal-leave-to {
  opacity: 0;
}
</style>