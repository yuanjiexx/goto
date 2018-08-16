<template>
  <div class="container">
    <!--<ul class="wrap">-->
    <!--<li><img src="../../assets/img/banner3.jpg"></li>-->
    <!--<li><img src="../../assets/img/banner2.jpg"></li>-->
    <!--<li><img src="../../assets/img/banner1.jpg"></li>-->
    <!--<li><img src="../../assets/img/banner3.jpg"></li>-->
    <!--</ul>-->
    <mt-swipe :auto="2000">
      <mt-swipe-item v-for="item in kiterunnerO" :key="item.id">
        <a :href="item.href" rel="external nofollow" >
          <img :src="item.url" class="img"/>
          <span class="desc"></span>
        </a>
      </mt-swipe-item>
    </mt-swipe>
  </div>
</template>

<script>
  import {Swipe, SwipeItem} from 'mint-ui'
  import 'mint-ui/lib/style.css'

  export default {
    components: {
      'mt-swipe': Swipe,
      'mt-swipe-item': SwipeItem
    },
    data () {
      return {
        kiterunnerO : [
          {url: require('@/assets/img/p-d-1.jpg')},
          {url: require('@/assets/img/p-d-2.jpg')},
          {url: require('@/assets/img/p-d-3.jpg')},
          {url: require('@/assets/img/p-d-4.jpg')},
        ],
      }
    }
  }
</script>

<style scoped>
  img {
    width: 3.6rem;
    height:4.6rem;
    margin:0 auto;
  }
  .mint-swipe {
    height: 4.6rem;
  }
  .desc {
    /*font-weight: 600;*/
    opacity: 0.9;
    font-size: 0.18rem;
    text-align: center;
    padding: 5px;
    height: 0.1rem;
    /*line-height: 0.4rem;*/
    width: 100%;
    color: #fff;
    background-color: rgba(0,0,0,0.2);
    position: absolute;
    bottom: 0;
  }
</style>
