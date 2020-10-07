<!--  -->
<template>
<div class='details'>
<header class="dp-header">
      <span class="dp-header-toRoot">
        <router-link to="/">
          <i class="el-icon-arrow-left" > 返回 </i>
        </router-link>
      </span>
      <h3>商品详情</h3>
    </header>

    <main class="dp-main">
      <div class="goods-img-wrap">
       <img src="" alt="">
      </div> 
      <div class="goods-card">
        <h3>这是水果一</h3>
        <p>这是水果介绍</p>
        <div>
          <span>￥
            <span class="goods-price">18</span>
          </span>
        </div>
      </div>
      <div class="goods-intruction">
        <p>
          这是水果一 的商品详细介绍
        </p>
      </div>
    </main>
    <footer class="dp-footer">
        <span>
          <router-link to="/Cart">
            <el-button icon="el-icon-goods">
              <span class="cart-counter" v-show="true">{{ cartCounter }}</span>
            </el-button>
          </router-link>
        </span>
        <el-button @click="addGoodsToCart" type="danger">加入购物车</el-button>
      </footer>
</div>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';

export default {
    name: 'detail',
//import引入的组件需要注入到对象中才能使用
components: {},
data() {
//这里存放数据
return {

};
},
//监听属性 类似于data概念
computed: {
  
},
//监控data中的数据变化
watch: {},
//方法集合
methods: {
 
    
},
//生命周期 - 创建完成（可以访问当前this实例）
created() {

},
//生命周期 - 挂载完成（可以访问DOM元素）
mounted() {
 
},
beforeCreate() {}, //生命周期 - 创建之前
beforeMount() {}, //生命周期 - 挂载之前
beforeUpdate() {}, //生命周期 - 更新之前
updated() {}, //生命周期 - 更新之后
beforeDestroy() {}, //生命周期 - 销毁之前
destroyed() {}, //生命周期 - 销毁完成
activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
}
</script>
<style lang="scss" scoped>
.details{
  width:100%;
  height: 100%;
  position: absolute;
  z-index: 1001;
  background-color: #fff;
}
.dp-header{
  position: relative;
  text-align: center;
  height: 40px;
  border-bottom: 1px solid #eee;
  line-height: 40px;
  .dp-header-toRoot{
    display: block;
    position: absolute;
    top: 0;
    left: 5px;
    .el-icon-arrow-left{
      font-size: 20px;
      font-weight: 800;
    }
  }
}
.dp-main{
  text-align: center;
  background-color: #fff;
  padding-bottom:40px;
  .goods-card{
    border: 1px solid #eee;
    margin: 0 10px;
    line-height: 40px;
    .goods-price{
      color: red;
    }
  }
  .goods-intruction{
    margin-top: 10px;
    border: 1px solid #eee;
    padding: 10px;
    line-height: 20px;
  }
}
.dp-footer{
  text-align: center;
  width: 100%;
  height: 50px;
  position: fixed;
  bottom: 0;
  left: 0;
  border-top: 1px solid #eee;
  background-color: #fff;
  font-size: 18px;
  .el-button--default,
  .el-button--danger{
    
    border: none;
    border-radius: 0;
    height: 50px;
    font-size: 25px;
    
  }
  .el-button--default{
    position: relative;
    width: 20%;
  }
  .el-button--danger{
    width: 80%;
    
    background-color: rebeccapurple;
  }
  .cart-counter{
    position: absolute;
    z-index: 10;
    width: 25px;
    height: 20px;
    top: 5px;
    left: 35px;
    line-height: 20px;
    border-radius: 40%;
    background-color: #ff65af;
    color: #fff;
    font-size: 10px;
  }
}
</style>