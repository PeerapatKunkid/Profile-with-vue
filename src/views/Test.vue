<script>
import LightBox from "../components/Lightbox.vue";

export default {
  components: {
    LightBox,
  },
};
</script>

<template>
  <div class="content">
  <button class="btn-1">BTN 1</button>
  <button class="btn-2">BTN 2</button>
  <button class="btn-3">BTN 3</button>
  <button class="btn-4">BTN 4</button>
  <button class="btn-5">BTN 5</button>
  <button class="btn-6">
  <div class="effect">
  <span>BTN 6</span>
  </div>
  <span>BTN 6</span>
  </button>
  <button class="btn-7">BTN 7</button>
  <button class="btn-8">BTN 8</button>
  <button class="btn-9">BTN 9</button>
  
  </div>
</template>

<style scoped>


.content{
  display:grid;
  padding-left:30%;
  padding-right:30%;
  padding-top:3rem;
  padding-bottom:3rem;
  animation: fadeInUp 2s;
  grid-template-columns: 1fr 1fr 1fr;
}
button{
  padding: 20px 50px;
  font-size: 1.5rem;
  cursor:pointer;
  border:0px;
  background:transparent;
  position:relative;
  margin:20px;
  transition: all o.25s ease;
}
.btn-1{
  background:black;
  color: #fff;
  border-radius:30px;
  transition: all 0.25s ease;
   position:relative;
  }
  .btn-1:hover{
    transform: translate(-12px,-12px);
  }
  .btn-1:hover::before{
    transform: translate(12px,12px);
  }
  .btn-1:hover::after{
    transform: translate(6px,6px);
  }
  .btn-1::after, .btn-1::before{
    content:"";
    position:absolute;
    opacity:0.3;
    border-radius: inherit;
    background:#000;
    width: 100%;
    height:100%;
    left: 0;
    bottom:0;
    z-index:-1;
    transition: all 0.25s ease;
  }

/* Button 2 */
.btn-2:hover::after{
  transform: translate(-5px,-5px);
  
}
.btn-2:hover::before{
  transform: translate(5px,5px);
  
}
.btn-2::after, .btn-2::before{
  content:"";
  border: 3px solid #000;
  position:absolute;
  border-radius: inherit;
  width: calc(100% - 6px);
  height: calc(100% - 6px);

  left:0;
  bottom:0;
  z-index:-1;
  transition: all 0.25s ease;
}

/* Button 3 */
.btn-3:hover::after{
  width:100%
}
.btn-3::after{
  content: "";
  position:absolute;
  border-radius:inherit;
  width:10%;
  height:5px;
  background: #000;
  left:0;
  bottom:0;
  z-index:-1;
  transition: all 0.25s ease;
  left:50%;
  transform: translateX(-50%);
}

/* Button 4 */
.btn-4{
  color:white;
  overflow:hidden;
  border-radius: 30px;
  box-shadow: 0px -0px 0px 0px rgba(143,64,248,0.5),0px 0px 0px 0px rgba(39,200,255,0.5);
  
}
.btn-4:hover{
  transform:translate(0,-6px);
  box-shadow: 0px -10px 25px 0px rgba(143,64,248,0.5),-10px 10px 25px 0px rgba(39,200,255,0.5);
}
.btn-4:hover::after{
  transform: rotate(150deg);
  
}
.btn-4::after{
  content:"";
  width:400px;
  height:400px;
  position:absolute;
  top:-50px;
  left:-100px;
  background-color:#ff3cac;
  background-image: linear-gradient(225deg,#27d86c 0%,#26caf9 50%,#c625d0 100%);
  z-index:-1;
  transition: all 0.25s ease;
  
}

/* Button 5 */
.btn-5:hover{
  color:#fff;
}

.btn-5:hover::after{
  transform:scale(1);
  opacity:1;
}
.btn-5::after{
  content:"";
  width:100%;
  height:100%;
  border-radius:30px;
  position:absolute;
  top:0;
  left:0;
  transform:scale(.1);
  background:#000;
  z-index:-1;
  opacity:0;
  transition: all 0.25s ease;
}

/* Button 6 */
.btn-6{
  border:3px solid #000;
  transform: skew(20deg);
  overflow:hidden;
  backface-visibility:hidden;
}
.btn-6 span{
  transform: skew(-20deg);
  display:block;
  transition: all 0.25s ease;
}
.btn-6:hover > span {
  opacity: 0;
  transform: scale(.5);
}
.btn-6 .effect{
  position:absolute;
  background:#000;
  left:0;
  top:0;
  width:100%;
  height:100%;
  color:#fff;
  z-index:10;
  display: flex;
  align-items:center;
  justify-content: center;
  transform: translate(0,-100%);
  transition: all 0.25s ease;
  backface-visibility:hidden;
}
.btn-6:hover .effect{
    transform: translate(0);
}
@keyframes fadeInUp {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

</style>

