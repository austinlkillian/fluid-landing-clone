<template>
  <div id="app">

    <div id="frame">
      <div id="top">
        <div id="top-top"></div>
        <div id="logo" @click='navShow=!navShow'>
          <div id="stamp">
            <p>+</p>
          </div>
        </div>
      </div>
      <div id="bottom"></div>
      <div id="left"></div>
      <div id="right"></div>
    </div>

    <div id="port-container">
      <header v-if='navShow'>
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
            <img src='./assets/searchOrange.png'/>
            <img src='./assets/emailOrange.png'/>
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

    <div id="contact">
      <h1>FLUID</h1>
      <h3>1065 South 500 West Bountiful, UT 84010 | (801) 295-9820 | Fluid Advertising</h3>
      <div id="social">
        <img src='./assets/facebookOrange.png'/>
        <img src='./assets/twitterOrange.png'/>
        <img src='./assets/emailOrange.png'/>
        <img src='./assets/linkedInOrange.png'/>
        <img src='./assets/blogOrange.png'/>
      </div>
      <p>Privacy Policy</p>
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
      navShow: true,
      portList: [
        {img:'http://getfluid.com/site/uploads/2016/01/fluid_sign_662x492_acf_cropped.jpg', co: 'FLUID', how: 'DESIGN | WEB DEV'},
        {img:'https://www.gmc.com/content/dam/gmc/na/us/english/index/shared-assets/jellybeans/2018/sierra-ld/sierra-denali/2018-sierra-1500-denali-onyx-black.jpg?imwidth=162', co: 'GMC', how: 'DESIGN | WEB DEV'},
        {img:'https://cdn.nextgov.com/media/img/upload/2018/05/16/051618microsoftNG/860x394.jpg', co: 'MICROSOFT', how: 'DESIGN | WEB DEV'},
        {img:'https://fortunedotcom.files.wordpress.com/2015/08/gettyimages-140706886-1.jpg', co: 'IBM', how: 'DESIGN | WEB DEV'},
        {img:'https://media.wired.com/photos/59c166e1fdf0d5611a915af7/2:1/w_2500,c_limit/AppleProductLaunch-HP-GettyImages-846153794.jpg', co: 'APPLE', how: 'DESIGN | WEB DEV'},
        {img:'https://cdn0.tnwcdn.com/wp-content/blogs.dir/1/files/2015/05/mcdonalds-e1430922835284-1200x639.jpg', co: 'MCDONALDS', how: 'DESIGN | WEB DEV'},
        {img:'https://brain-images-ssl.cdn.dixons.com/7/3/10170337/l_10170337_001.jpg', co: 'BEATS', how: 'DESIGN | WEB DEV'},
        {img:'https://static.makeuseof.com/wp-content/uploads/2018/08/most-watched-youtube-670x335.jpg', co: 'YOUTUBE', how: 'DESIGN | WEB DEV'},
        {img:'https://timedotcom.files.wordpress.com/2015/06/facebook.jpg', co: 'FACEBOOK', how: 'DESIGN | WEB DEV'},
        {img:'https://cdn-images-1.medium.com/max/1600/1*yZ1LPIcXnnW6Ubmp2M-0rQ.png', co: 'AIRBNB', how: 'DESIGN | WEB DEV'},
        {img:'https://www.geek.com/wp-content/uploads/2018/07/amazon-625x352.jpg', co: 'AMAZON', how: 'DESIGN | WEB DEV'},
        {img:'https://amp.businessinsider.com/images/56b9fd532e526575008b5efb-750-562.jpg', co: 'WENDYS', how: 'DESIGN | WEB DEV'},
        {img:'https://cdn0.tnwcdn.com/wp-content/blogs.dir/1/files/2016/12/twitch-e1491600114230-796x398.jpg', co: 'TWITCH', how: 'DESIGN | WEB DEV'},
        {img:'https://brand.campaign.adidas.com/Images/adidas-skateboarding_SS18-CityCup-FranchiseTeaser-CLO_640x640_tcm66-268245.jpg?locale=en_US&device=desktop&version=2', co: 'ADIDAS', how: 'DESIGN | WEB DEV'},
        {img:'http://www.sobhacitymall.com/wp-content/uploads/2017/10/Levis-1.png', co: 'LEVIS', how: 'DESIGN | WEB DEV'},
        {img:'https://cdn.vox-cdn.com/thumbor/f3vZQsUgEUzG8J_SrwucezgvQQo=/0x0:1000x800/1200x800/filters:focal(420x320:580x480)/cdn.vox-cdn.com/uploads/chorus_image/image/58194493/IGN_logo_2.0.jpg', co: 'IGN', how: 'DESIGN | WEB DEV'},
        {img:'https://slickdeals.net/blog/wp-content/uploads/2018/08/best_buy_anniversary_sale_52_hero_.jpg', co: 'BEST BUY', how: 'DESIGN | WEB DEV'},
        {img:'https://assets.entrepreneur.com/content/3x2/2000/20171228231121-ent18-janfeb-greatclips.jpeg?width=700&crop=2:1', co: 'GREAT CLIPS', how: 'DESIGN | WEB DEV'},
        {img:'https://cdn.gobankingrates.com/wp-content/uploads/2015/11/Home_depot_deals_best-848x477.jpg', co: 'HOME DEPOT', how: 'DESIGN | WEB DEV'},
        {img:'https://amp.businessinsider.com/images/55a95c612acae7a6098b7998-750-563.jpg', co: 'BANK OF AMERICA', how: 'DESIGN | WEB DEV'},
        {img:'https://static1.squarespace.com/static/51b3dc8ee4b051b96ceb10de/t/5b2a4a95562fa7f5948b8c5a/1529498266965/amc-now-offering-its-own-subscription-service-social.jpg?format=2500w', co: 'AMC', how: 'DESIGN | WEB DEV'}
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
  primary: white,
  secondary: rgb(187, 187, 187)
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

    #top:hover + header {
      visibility: visible;
  }

    #top-top {
    width: 100%;
    height: $frame;
    background: color(primary);
    position: absolute;
    top: 0;
  }

    #logo{
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background: color(primary);
      z-index: 3;
      display: flex;
      justify-content: center;
      align-items: center;

      #stamp{
        width: 50px;
        height: 50px;
        border-radius: 50%;
        border: 3px solid color(secondary);
        display: flex;
        justify-content: center;
        align-items: center;

        p {
          font-size: 60px;
          font-weight: bold;
          color: color(secondary)
        }
      }
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
    width: calc(100% - 60px);
    background: color(primary);
    position: relative;
    top: 35px;
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;

    header:hover {
      visibility: visible;
    }

    header:hover {
      visibility: visible;
    }

    header {
      // visibility: hidden;
      width: 100%;
      height: 150px;
      background: rgba(37, 37, 37, 0.776);
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
        position: relative;
        top: 25px;
      }

      #title {
        width: 25%;
        color: white;
        font-size: 30px;
        font-weight: bold;
      }

      #nav {
        width: 50%;

        ul {
          display: flex;
          justify-content: space-between;
          align-items: center;
          font-size: 20px;
          font-weight: bold;
          color: color(accent)
        }
      }

      #icons {
        width: 25%;
        display: flex;
        justify-content: flex-end;

        img {
          width: 30px;
          height: 30px;
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

  #contact {
    width: 80%;
    height: 300px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    margin-bottom: 100px;

    h1 {
      font-family: Arial;
      font-weight: bold;
      font-size: 35px;
      color: rgb(59, 59, 59);
    }

    h3 {
      font-family: arial;
      font-weight: bold;
      font-size: 25px;
      color: grey;
    }

    #social {
      width: 300px;
      display: flex;
      justify-content: space-between;
      align-items: center;

      img {
        width: 30px;
      }
    }

    p {
      font-weight: bold;
      color: grey;
    }
  }

}
</style>
