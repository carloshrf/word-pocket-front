<template>
  <div class="words-page">
    <top-bar />
    <div class="content">
      <go-back />
      <div class="title-group">
        <h1>words</h1>
        <add-button @click.native="showModal = !showModal"/>
      </div>
      <search-input class="search-input" />
      <ul>
        <li v-for="word in words" :key="word.id">
          <item-list 
            :phrase="word.word" 
            :translated="word.translated" 
          />
        </li>
      </ul>
    </div>
    <modal v-if="showModal" title="Add words" :handleModal="handleModalView" >
      <form v-on:submit.prevent="submit" class="add-word-form">
        <div>
          <label for="word-input">Add a phrase</label>      
          <textarea type="text" id="word-input" rows="3" placeholder="put here your word..."/>
        </div>
        <div>
          <label for="translated-input">Agora a tradução</label>
          <textarea type="text" id="translated-input" rows="3" placeholder="palavra traduzida..."/>
        </div>
        <input type="submit" value="add new word!">
      </form>
    </modal>
  </div>
</template>

<script type="module">
import data from '../bd.js';

const { words } = data; 

export default {
  name: 'Words',
  components: {
    TopBar: () => import('../components/TopBar'),
    GoBack: () => import('../components/buttons/GoBackButton'),
    AddButton: () => import('../components/buttons/AddButton'),
    Modal: () => import('../components/Modal'),
    ItemList: () => import('../components/ItemList'),
    SearchInput: () => import('../components/inputs/Search')
  },
  data() {
    return {
      showModal: false,
      words: words,
    }
  },
  methods: {
    submit() {
      console.log('enviou po')
    },
    handleModalView(e) {
      if (e) {
        e.target !== e.currentTarget 
          ? (this.showModal = !this.showModal)
          : null;
      }

      this.showModal = !this.showModal;
    }
  }
}
</script>

<style scoped>
  .words-page {
    position: relative;
  }

  .content {
    padding: 0 50px;
    padding-top: 20px;
  }

  .content .search-input {
    margin: 20px 0 50px;
  }

  .content .title-group * {
    display: inline-flex;
  }

  .content .title-group h1 {
    padding-right: 20px;
  }

  @keyframes goDown {
    0% {
      /* transform: scaleY(0); */
      transform: translate3D(0, -10px, 0);
      opacity: 0;
    }
    80% {
      /* transform: scaleY(1.1); */
    }
    100% {
      /* transform: scaleY(1); */
      transform: translate3D(0, 0px, 0);
      opacity: 1;
    }
  }

  .words-page .add-word-form {
    animation: goDown 0.2s ease-in-out forwards;
    display: flex;
    flex-direction: column;
    
  }

  .words-page .add-word-form div {
    width: 100%;
  }

  .words-page .add-word-form textarea {
    box-sizing: border-box;
    padding: 5px;
    width: 100%;
    margin-bottom: 20px;
    display: block;
    resize: none;
    border-radius: 10px;
    outline: none;
  }

  .words-page .add-word-form input[type="submit"] {
    background-color: paleturquoise;
    border: none;
    padding: 10px 20px;
    border-radius: 10px;
    font-size: 18px;
    cursor: pointer;
  }

  .content h1 {
    font-weight: 400;
    font-size: 50px;
  }

  .content ul li {
    padding-bottom: 20px;
    list-style: none;
  }

  .content ul li i {
    color: #7e7c7c;
  }
</style>