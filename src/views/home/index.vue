<template>
  <div class="app-init home-index">
    <header class="public-header">
      <form class="search-box clear">
        <div class="input-box" @click="$router.openPage('/search')">
          <span class="iconfont icon-sousuo-copy absolute"></span>
          <input
            type="text"
            class="input-controller"
            placeholder="搜索商品名称"
            readonly
          />
        </div>
        <div class="myself-center fr" @click="$router.openPage('/mine')">
          <span class="iconfont icon-smile"></span>
        </div>
      </form>

      <nav class="menu-box scroll-box-x noscroll">
        <ul class="wrap-box clear">
          <li
            class="item"
            :class="{ active: index == navListActiveIndex }"
            v-for="(value, index) in navList"
            @click="navChange(index)"
            :key="index"
          >
            <span>{{ value.name }}</span>
          </li>
        </ul>
      </nav>
    </header>

    <div
      ref="view01"
      class="app-init scroll-box tab-box mi-tj footer-hack"
      v-show="navListActiveIndex == 0"
    >
      <div class="shop-item">
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view02"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 1"
    >
      <div class="shop-item">
        <img alt="" />
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist01"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view03"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 2"
    >
      <div class="shop-item">
        <img alt="" />
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist02"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view04"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 3"
    >
      <div class="shop-item">
        <img alt="" />
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist03"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view05"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 4"
    >
      <div class="shop-item">
        <img alt="" />
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist04"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view06"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 5"
    >
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317010732422.png'
        "
        @click="$router.openPage('/detail/1003')"
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/48ca6cfb19c45e7cbecbd8c34c757445.jpg'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317012799998.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317013522274.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317005752430.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317011947232.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317014434073.png'
        "
        alt=""
      />
    </div>

    <div
      ref="view07"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 6"
    >
      <div class="shop-item">
        <img
          src="http://qiniu.verydog.cn//show.liluo.cc/2018011316464243450.png"
          alt=""
        />
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist06"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view08"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 7"
    >
      <div class="shop-item">
        <img
          src="http://qiniu.verydog.cn//show.liluo.cc/2018011316464243450.png"
          alt=""
        />
        <div class="shop-box clear">
          <div
            class="shop-box-item"
            v-for="(target, index) in shoplist07"
            :key="index"
            @click="$router.openPage(target.href)"
          >
            <img v-lazy="target.src" alt="" />
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      ref="view09"
      class="app-init scroll-box tab-box footer-hack"
      v-show="navListActiveIndex == 8"
    >
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317154829739.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317155627636.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317160444789.png'
        "
        alt=""
      />
      <img
        v-lazy="
          'http://qiniu.verydog.cn//show.liluo.cc/2018011317161351928.png'
        "
        alt=""
      />
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import VueDB from "../../util/vue-db/vue-db";

let DB = new VueDB();

export default {
  data() {
    return {
      shoplist: [
        {
          src: "https://s3.ax1x.com/2020/12/15/rKQESP.jpg",
          title: "呀土豆蜂蜜黄油味",
          con: "蜂蜜黄油味",
          money: 7,
          href: "/detail/1010",
        },
      ],
      navList: [
        {
          name: "推荐",
        },
        {
          name: "酒水饮料",
        },
        {
          name: "方便速食",
        },
        {
          name: "零食小食",
        },
        {
          name: "生活日用",
        },
      ],
      navListActiveIndex: 0,

      bannerList01: [
        {
          href: "/detail/1007",
        },
        {
          href: "/detail/1009",
        },
      ],
      shoplist01: [
        {
          src: "https://s3.ax1x.com/2020/12/09/rCKV9x.png",
          title: "康师傅冰红茶",
          con: "康师傅 / 冰红茶",
          money: 2.5,
          href: "/detail/1001",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKAkuR.jpg",
          title: "可口可乐",
          con: "可口可乐 / 原味",
          money: 3,
          href: "/detail/1003",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKZIqs.jpg",
          title: "百事可乐",
          con: "百事可乐/原味",
          money: 3,
          href: "/detail/1004",
        },
      ],

      bannerList02: [
        {
          href: "/detail/1011",
        },
      ],
      shoplist02: [
        {
          src: "https://s3.ax1x.com/2020/12/09/rCKcvT.jpg",
          title: "康师傅红烧牛肉面",
          con: "大桶更尽兴",
          money: 4.5,
          href: "/detail/1002",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKmc38.jpg",
          title: "老坛酸菜牛肉面",
          con: "统一老坛 就是这个味",
          money: 4,
          href: "/detail/1005",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKn1Kg.jpg",
          title: "康师傅酸菜牛肉面",
          con: "酸菜牛肉面",
          money: 4,
          href: "/detail/1007",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKK69x.jpg",
          title: "统一藤椒牛肉面",
          con: "藤椒",
          money: 4,
          href: "/detail/1008",
        },
      ],

      bannerList03: [
        {
          href: "/detail/1013",
        },
      ],
      shoplist03: [
        {
          src: "https://s3.ax1x.com/2020/12/15/rKQESP.jpg",
          title: "呀土豆",
          con: "蜂蜜黄油味",
          money: 7,
          href: "/detail/1009",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKQlYn.jpg",
          title: "乐事薯片",
          con: "经典原味",
          money: 7,
          href: "/detail/1010",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rKQRTH.jpg",
          title: "米多奇小馍丁",
          con: "经典小食",
          money: 2,
          href: "/detail/1011",
        },
      ],

      bannerList04: [
        {
          href: "/detail/1014",
        },
      ],
      shoplist04: [
        {
          src: "https://s3.ax1x.com/2020/12/15/rKlc3q.jpg",
          title: "得力胶棒",
          con: "得力",
          money: 3,
          href: "/detail/1012",
        },
        {
          src: "https://s3.ax1x.com/2020/12/15/rK13rT.jpg",
          title: "每洁面巾纸",
          con: "每洁",
          money: 1,
          href: "/detail/1013",
        },
      ],

      bannerList06: [
        {
          href: "/detail/1015",
        },
      ],
      shoplist06: [],

      bannerList07: [
        {
          href: "/detail/1017",
        },
      ],
      shoplist07: [],
    };
  },
  components: {},
  mounted() {
    // 笨方法，设置N个盒子的scroll top

    this.navListActiveIndex =
      DB.getItemOnce("home-index-nowIndex").toNumber() || 0;

    setTimeout(() => {
      this.$refs.view01.scrollTop =
        DB.getItemOnce("home-index-view01").toNumber() || 0;
      this.$refs.view02.scrollTop =
        DB.getItemOnce("home-index-view02").toNumber() || 0;
      this.$refs.view03.scrollTop =
        DB.getItemOnce("home-index-view03").toNumber() || 0;
      this.$refs.view04.scrollTop =
        DB.getItemOnce("home-index-view04").toNumber() || 0;
      this.$refs.view05.scrollTop =
        DB.getItemOnce("home-index-view05").toNumber() || 0;
      this.$refs.view06.scrollTop =
        DB.getItemOnce("home-index-view06").toNumber() || 0;
      this.$refs.view07.scrollTop =
        DB.getItemOnce("home-index-view07").toNumber() || 0;
    }, 10);
  },
  methods: {
    navChange(index) {
      // 导航栏切换
      this.navListActiveIndex = index;
    },
  },
  beforeRouteLeave(to, from, next) {
    DB.setItem("home-index-view01", this.$refs.view01.scrollTop);
    DB.setItem("home-index-view02", this.$refs.view02.scrollTop);
    DB.setItem("home-index-view03", this.$refs.view03.scrollTop);
    DB.setItem("home-index-view04", this.$refs.view04.scrollTop);
    DB.setItem("home-index-view05", this.$refs.view05.scrollTop);
    DB.setItem("home-index-view06", this.$refs.view06.scrollTop);
    DB.setItem("home-index-view07", this.$refs.view07.scrollTop);

    DB.setItem("home-index-nowIndex", this.navListActiveIndex);
    next();
  },
};
</script>

<style type="text/sass" lang="sass">
.home-index .tab-box
  top: 2.5rem
  .home-swiper
    height: 5rem

  .home-index  .nav-mi-tj a
    display: block
    width: 25%
  .home-index .shop-box
    background-color: #fff
</style>
