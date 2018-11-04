<template>
  <div id="app">

    <div id="frame">
      <div id="top">
        <div id="top-top"></div>
        <div id="logo"></div>
      </div>
      <div id="bottom"></div>
      <div id="left"></div>
      <div id="right"></div>
    </div>

    <div id="port-container">
      <header>
        <div id="header-container">
          <div id="title">
            <p>FLUID</p>
          </div>
          <div id="nav">
            <ul>
              <li>PORTFOLIO</li>
              <li>SERVICES</li>
              <li>AGENCY</li>
              <li>BLOG</li>
            </ul>
          </div>
          <div id="icons">
            <img />
            <img />
          </div>
        </div>
      </header>
      <portfolio v-for='(co, i) in portList'
                    :key='i'
                    :co='co'/>

      <div id="footer">
        <ul>
          <li>ALL</li>
          <li>DESIGN</li>
          <li>LEAD GEN</li>
          <li>SOCIAL</li>
          <li>STRATEGY</li>
          <li>TRADITIONAL</li>
          <li>WEB DEV</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Portfolio from "./components/Portfolio.vue";
import "./reset.css";

export default {
  name: "app",
  data() {
    return {
      portList: [
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'https://www.gmc.com/content/dam/gmc/na/us/english/index/shared-assets/jellybeans/2018/sierra-ld/sierra-denali/2018-sierra-1500-denali-onyx-black.jpg?imwidth=162', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
      ]
    }
  },
  components: {
    Portfolio
  }
};
</script>

<style lang="scss">

$frame: 35px;

$colors: (
  accent: rgb(255, 132, 0),
  primary: white
);

@function color($color-name){
  @return map-get($colors, $color-name)
};

#app {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  #frame {
    z-index: 5;
  }

  #top {
    width: 100%;
    height: 70px;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1;

    #top-top {
    width: 100%;
    height: $frame;
    background: color(primary);
    position: absolute;
    top: 0;
  }

    #logo{
      width: 90px;
      height: 90px;
      border-radius: 50%;
      background: color(primary);
      z-index: 3;
    }
  }

  #bottom {
    width: 100%;
    height: $frame;
    background: color(primary);
    position: fixed;
    bottom: 0;
    left: 0;
    z-index: 1;
  }

  #left {
    width: $frame;
    height: 100%;
    background: color(primary);
    position: fixed;
    left: 0;
    z-index: 1;
  }

  #right {
    width: $frame;
    height: 100%;
    background: color(primary);
    position: fixed;
    right: 0;
    z-index: 1;
  }

  #port-container {
    width: calc(100% - 65px);
    background: color(primary);
    position: relative;
    top: 35px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

    header {
      width: 100%;
      height: 150px;
      background: red;
      position: fixed;
      z-index: 2;
      display: flex;
      justify-content: center;
      align-items: center;

      #header-container {
        width: 90%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
      }

      #title {
        width: 33%;
      }

      #nav {
        width: 33%;

        ul {
          display: flex;
          justify-content: space-between;
          align-items: center;
        }
      }

      #icons {
        width: 33%;
        display: flex;
        justify-content: flex-end;

        img {
          width: 30px;
          height: 30px;
          border-radius: 50%;
          background: blue;
          margin: 15px;
        }
      }

    }

    #footer {
      position: fixed;
      width: calc(100% - 68px);
      background: rgba(46, 46, 61, 0.801);
      bottom: 35px;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px 0;
      z-index: 2;

      ul {
        width: 90%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        align-items: center;
        font-size: 17px;
        color: white;
        letter-spacing: 4px;

        li{
          margin: 10px;
        }
      }
    }
  }

}
</style>
