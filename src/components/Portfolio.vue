<template>
  <div id="body">
    <img v-bind:src="co.img" />
    <div id="info">
      <div id="info-container">
        <div id="co-container">
          <h1>{{co.co}}</h1>
          <div id="tri"></div>
        </div>
        <hr/>
        <p>{{co.how}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Portfolio',
  data() {
    return{
      infoShow: false
    }
  },
  props: ['co']
}
</script>

<style lang="scss" scoped>

$colors: (
  accent: rgb(255, 132, 0),
  primary: rgb(240, 240, 240)
);

@function color($color-name){
  @return map-get($colors, $color-name)
};
 
  #body {
    width: 33%;
    height: 400px;
    display: flex;
    position: relative;
    border: 2px solid color(primary);

    img {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    #info {
      visibility: hidden;
      background: rgba(0, 0, 0, 0.809);
      z-index: 1;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: center;
    }

    #info-container{
      color: white;
      width: 80%;
      position: relative;
      bottom: 20px;

      #co-container {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        cursor: pointer;

        #tri {
          width: 40px;
          height: 40px;
          clip-path: polygon(45% 5%, 50% 0, 100% 50%, 50% 100%, 45% 95%, 90% 50%);
          background: rgba(255, 166, 0, 0.612);
        }
      }
    }

    img:hover + #info {
      visibility: visible;
    }

    #info:hover {
      visibility: visible;
    }

    h1 {
      font-size: 40px;
      font-family: arial;
    }

    hr {
      background: rgb(70, 70, 70);
      height: 1px;
      width: 100%;
      border: none;
      z-index: 5;
      margin: 20px 0;
    }

    p {
      font-size: 19px;
      color: color(accent);
      font-family: arial;
    }
  }
</style>
