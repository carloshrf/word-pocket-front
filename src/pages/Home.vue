<template>
  <section id="home-page">
    <div class="top-bar-container" />
    <div class="container">
      <div class="content">
        <h1>Collections</h1>
        <div class="cards">
          <HomeCard 
            title="Words"
            value=77
          />
          <HomeCard 
            title="phrases"
            value=115
          />
        </div>
        <div class="op-buttons">
          <Button>
                        <router-link to='/words'>add words</router-link>
          </Button>
          <Button>
            <router-link to='/phrases'>add phrases</router-link>
          </Button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home',
  components: {
    HomeCard: () => import('../components/HomeCard'),
    Button: () => import('../components/buttons/Button')
  },
  data() {
    return {
      phrases: [
        'aaaeeeee só do massa ó',
        'Bixo réi supimpa',
        'vem pro x1 safado',
        'cai dento que to doido pra te descer na paulada',
        'I have a burguesa in my hands'
      ]
    }
  }
}
</script>
<style scoped>
  .home-page {
    position: relative;
  }

  .top-bar-container {
    width: 100%;
    height: 200px;
    border-radius: 0 0 60px 60px;
    background-color: wheat;
  }

  .container .content {
    position: relative;
  }

  .container .content h1 {
    position: absolute;
    top: -110px;
    width: 100%;

    text-align: center;
    font-size: 36px;
  }

  .container .content .cards {
    position: absolute;
    top: -40px;
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .container .content .cards div:first-child {
    margin-right: 50px;
  }

  .container .content .op-buttons {
    padding-top: 300px;
    display: flex;
    justify-content: center;
  }

  .container .content .op-buttons button:first-child {
    margin-right: 50px;
  }
</style>