<template>
  <div id="public">
    <div>
      <a>图文详情</a>
      <a>出版信息</a>
    </div>
    <p class="clearfix">
      <span>书名</span>
      <span>{{publicinformation.b_name}}</span>
    </p>
    <p class="clearfix">
      <span>ISBN</span>
      <span>{{publicinformation.b_isbn}}</span>
    </p>
    <p class="clearfix">
      <span>作者</span>
      <span>{{publicinformation.b_author}}</span>
    </p>
    <p class="clearfix">
      <span>出版社</span>
      <span>{{publicinformation.b_publish}}</span>
    </p>
    <p class="clearfix">
      <span>出版时间</span>
      <span>{{publicinformation.b_publishTime}}</span>
    </p>
    <p class="clearfix">
      <span>开本</span>
      <span>{{publicinformation.b_paper}}</span>
    </p>
    <p class="clearfix">
      <span>纸张</span>
      <span>{{publicinformation.b_format}}</span>
    </p>
    <p class="clearfix">
      <span>包装</span>
      <span>{{publicinformation.b_pack}}</span>
    </p>
    <p class="clearfix">
      <span>是否套装</span>
      <span>{{publicinformation.b_isSuit}}</span>
    </p>
  </div>
</template>

<script>
    export default {
        name: "Public",
      data() {
          return {
            publicinformation : {
              b_name :'追风筝的人',
              b_isbn:'9787208061644',
              b_author:'[美]卡勒德.胡赛尼（Khaled Hosseini）著，李继宏译',
              b_publish:'上海人民出版社',
              b_publishTime:'2006-05-01',
              b_paper:'32开',
              b_format:'胶版纸',
              b_pack:'平装-胶订',
              b_isSuit:'否',
            },
          }
      }
    }
</script>

<style scoped>
  #public {
    display: flex;
    flex-direction:column;
    justify-content:left;
    font-family: Arial, Verdana, Tahoma, "微软雅黑", "黑体";
    margin:0;
    padding:0;
  }
  a { text-decoration: none;
    display:block;}
  #public div {
    text-align: center;
  }
  #public div a {
    display:inline;
    font-size: 0.38rem;
    line-height:0.85rem;
  }
  #public div a:nth-child(1):after{
    content:"| ";
    margin:0 0.3rem;
  }
  #public p {
    width:80%;
    margin:0 auto;
  }
  #public p span:nth-child(1) {
    display: block;
    width:30%;
    line-height:0.82rem;
    font-size: 0.26rem;
    float:left;
    padding-left:0.2rem;
  }
  #public p  span:nth-child(2){
    display: block;
    width:70%;
    line-height:0.82rem ;
    float:left;
    font-size: 0.26rem;
  }
</style>
