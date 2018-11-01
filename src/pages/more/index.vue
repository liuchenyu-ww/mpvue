<template>
  <div class="container" @click="clickHandle()">
    <div class="header">Looo-Geopen</div>
    <div class="hr_header"></div>
    <div class="footer">
      <div>
        <a href="/pages/index/main">
          <div>
            <img src="../../../static/assets/首页.png" alt="首页">
          </div>
          <div>潮流前线</div>
        </a>
      </div>
      <div>
        <a href="/pages/shoppingCart/main">
          <div>
            <img src="../../../static/assets/购物车t.png" alt="购物车">
          </div>
          <div>购物车</div>
        </a>
      </div>
      <div>
        <a href="#">
          <div>
            <img src="../../../static/assets/More1.png" alt="更多">
          </div>
          <div style="color:#FA7AD7;">更多商品</div>
        </a>
      </div>
      <div>
        <a href="/pages/counter/main">
          <div>
            <img src="../../../static/assets/我的.png" alt="我的">
          </div>
          <div>我的信息</div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      photo: '',
      phototwo: '',
      peaplenumber: '20123'
    }
  },

  components: {
    card
  },
  mounted () {
    this.query()
  },
  methods: {
    query () {
      this.$httpWX.post({
        url: '/example/Studystep',
        data: {
          // 'categoryType': 'SaleGoodsType@sim',
          // 'streamNo': 'web_bss153570682909641893',
          // 'reqSource': 'MALL_H5',
          // 'appid': 'string',
          // 'timestamp': 1535706829096,
          // 'sign': 'string'
        }
      }).then(res => {
        console.log(res)
      })
      this.$httpWX.post({
        url: '/example/Studystep/one',
        data: {
          // 'categoryType': 'SaleGoodsType@sim',
          // 'streamNo': 'web_bss153570682909641893',
          // 'reqSource': 'MALL_H5',
          // 'appid': 'string',
          // 'timestamp': 1535706829096,
          // 'sign': 'string'
        }
      }).then(res => {
        console.log(res)
        this.photo = res.data.photo
      })
      this.$httpWX.post({
        url: '/example/Studystep/two',
        data: {
          // 'categoryType': 'SaleGoodsType@sim',
          // 'streamNo': 'web_bss153570682909641893',
          // 'reqSource': 'MALL_H5',
          // 'appid': 'string',
          // 'timestamp': 1535706829096,
          // 'sign': 'string'
        }
      }).then(res => {
        console.log(res)
        this.phototwo = res.data.myphoto
      })
    },
    clickHandle () {
      this.msg = ''
    }
  },

  created () {
    // 调用应用实例的方法获取全局数据
  }
}
</script>

<style scoped>
  .header {
    width:100%;
    height:100px;
    background:#DFC0E7;
    color:#fff;
    -webkit-display:flex;
    display:flex;
    -webkit-align-items:center;
    align-items:center;
    -webkit-justify-content:center;
    justify-content:center;
    font-size:16px;
    font-weight:bold;
  }
  .hr_header {
    background:#F7F7F7;
    height:3px;
    width:100%;
    margin:10px 0;
  }
  .footer {
    height:60px;
    position:relative;
    bottom:0;
  }
  .footer>div { 
    text-align:center;
    float:left;
    width:25%;
    height:60px;
  }
  .footer div div img {
    width:22px;
    height:20px;
  }
  .footer div div {
    -webkit-display:flex;
    display:flex;
    -webkit-align-items:center;
    align-items:center;
    -webkit-justify-content:center;
    justify-content:center;
    height:30px;
    color:#888888;
    font-size:14px;
  }
</style>
