<template>
  <ul class="history">
    <div class="header1">
      <router-link class="st1" to="/person">&#xe602;</router-link>
      <h2>浏览历史</h2>
      <button type="button" class="ci">清除</button>
    </div>
    <li class="part1 clearfix" v-for="(u,index) in jpgList">
      <div class="left">
        <!--<span>{{index+1}}</span>-->
        <img :src="u.url" width="100" height="100"/>
      </div>
      <div class="right">
        <p>{{u.title}}</p>
      </div>
      <div class="lo">
        <h5>{{u.priceNew}}</h5>
        <h6>{{u.priceOld}}</h6>
      </div>
      <div class="ko">
        <div class="po">总计钱数{{u.allprice}}</div>

      </div>
    </li>
  </ul>
</template>

<script>
  export default {
    name: "history",
    data(){
      return{
        jpgList:[
          {url:require('../../assets/img/1.jpg'),
            title:'中国历史',
            author:'匿名',
            priceNew:'￥40.80',
            priceOld:'￥45.00',
            allprice:'￥26.60',
          },
          {url:require('../../assets/img/2.jpg'),
            title:'解忧杂货铺',
            author:'东野圭吾',
            priceNew:'￥30.90',
            priceOld:'￥34.00',
            allprice:'￥26.60',
          },
          {url:require('../../assets/img/3.jpg'),
            title:'我不',
            author:'大冰',
            priceNew:'￥26.60',
            priceOld:'￥28.00',
            allprice:'￥26.60',

          }
        ]
      }
    }
  }
</script>

<style scoped>
  .ko{
    width:100%;
    height: 0.6rem;
  }

  .part1{
    display: block;
    background-color: white;
    border-top:0.1rem #eaeaea solid;
    border-bottom: 0.1rem #ccc solid;
    position: relative;
    float: left;
  }
  .left>span:nth-child(1){
    background-color: forestgreen;
    color: white;
    padding:0 0.1rem;
    position: absolute;
    left: 0;
    top: 0;
    width: 0.2rem;
  }
  .ci{
    width:1.5rem;
    height: 0.7rem;
    background-color: #fff;
    border:1px #009a61 solid;
    padding-bottom:1px;
  }
  .left{
    float: left;
    position: relative;
    height: 2.5rem;
    margin-right: 1.5rem;
  }
  .right{
    float: left;
    position: relative;
    line-height: 0.2rem;
    padding-top:0.1rem;
    padding-bottom: 0.1rem;
  }
  .part1 img{
    margin-top: 0.2rem;
    margin-left: 0.2rem;
    border: 0.1rem solid #f5f5f5;
    /*padding: 20px;*/
  }
  .star span,.span1{
    font-family: 'iconfont';
    font-size: 0.1rem;
  }


  .right{
    display: flex;
    flex-grow: 2;

    margin:1rem auto;
  }
  .lo{
    margin-top: 1rem;
    float: right;
    display: flex;
    flex-direction: column;
    margin-right: 0.5rem;
  }h5{
     font-size: 0.4rem;
     margin-bottom: 0.3rem;
   }
  h6{
    text-decoration: line-through;
    color:#ccc;
    font-size: 0.4rem;
  }

  .po , .ko{

    float: right;

    font-size: 0.3rem;

  }

  .header1{

    width:100%;
    height:1.5rem;
    background-color: white;
    border-bottom: 0.1rem #f2f2f2 solid;
    display: flex;
    justify-content: flex-start;
    padding:0.5rem;
  }
  .st1{
    font-family:iconfont;
    font-size:0.6rem;
    position: absolute;
    left:0.3rem;

  }
  h2{
    margin: 0 auto;
  }

</style>
