<template>
  <div class="container">
    <!--<ul class="wrap">-->
      <!--<li><img src="../../assets/img/banner3.jpg"></li>-->
      <!--<li><img src="../../assets/img/banner2.jpg"></li>-->
      <!--<li><img src="../../assets/img/banner1.jpg"></li>-->
      <!--<li><img src="../../assets/img/banner3.jpg"></li>-->
    <!--</ul>-->
    <mt-swipe :auto="2000">
      <mt-swipe-item v-for="item in items" :key="item.id">
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
        items: [{
          title: '你的名字', url: require('@/assets/img/banner1.jpg')
        }, {
          title: '图书大促销', url: require('@/assets/img/banner2.jpg')
        }, {
          title: '品牌打折扣', url: require('@/assets/img/banner3.jpg')
         }
       ]
      }
    }
  }
</script>

<style scoped>
  img {
    width: 100%;
  }
  .mint-swipe {
    height: 2rem;
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
