<template>
  <div id="app">
    <div class="references" @click="showModal">
      <h1>Hivatkozások</h1>
    </div>
    <modal v-if="showModalPls" @close="closeModal" >
      <div class="content">
        <div class="content__title">
          <h2>Működik baszki</h2>
        </div>
        <div class="content__body">
          <h3>Gyere rám Vue Master</h3>
        </div>
        <div class="content__footer">
          <h4>Dobj meg egy sörrel pls</h4>
        </div>
      </div>
    </modal>

  </div>
</template>

<script>
import PopupModal from './components/default-elements/popup-modal';

export default {
  name: 'App',
  components: {
   modal: PopupModal
  },
  data(){
    return {
      showModalPls:false
    }
  },
  methods: {
    closeModal() {
      this.showModalPls = false;
    },
    showModal() {
      this.showModalPls = !this.showModalPls;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.references{
  cursor: pointer;
}

.content{
  border: 1px solid gray;
  box-shadow: gray;
}
</style>
