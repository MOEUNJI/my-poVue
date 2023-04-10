<template>
  <div class="home">
    <section class="main-page">
        <div class="snow-box"></div>
        <div class="container">
            <div class="move" :class="{move:true}" v-for="(tag,idx) in tagList" :key="idx">{{tag}}</div>
            <!-- <div class="move move2">#열정</div>
            <div class="move move3">#의지</div>
            <div class="move move4">#노력</div>
            <div class="move move5">#긍정</div>
            <div class="move move6">#성실</div>
            <div class="move move7">#최선</div>
            <div class="move move8">#끈기</div>
            <div class="move move9">#용기</div>
            <div class="move move10">#보람</div> -->
        </div>
        <div class='wave-box'>
            <div class='wave -one'></div>
            <div class='wave -two'></div>
            <div class='wave -three'></div>
            <div class="main-title-text">
                <h1 class="main-title">WELLCOM TO MY
                    <br>
                    <span class="portfolio">PORTFOLIO</span>
                </h1>
                <p class="main-sub-text">
                    저의 포트폴리오에 오신것을 환영합니다.
                    <br>
                    알면 알수록
                    <span class="bold-text">흥미</span>
                    롭고 코드를 작성하면
                    <br>
                    제가 원하는 결과물이 나오는 것에
                    <span class="bold-text">재미</span>
                    를 느껴
                    <br>
                    웹 퍼블리셔에
                    <span class="bold-text">도전</span>
                    하게 되었습니다.
                    <br>
                </p>
            </div>
        </div>
    </section>
  </div>
</template>

<script>

export default {
  name: 'Home',
    data() {
      return {
        tagList:['#도전','#열정','#의지','#노력','#긍정','#성실','#최선','#끈기','#용기','#보람'],
        moveNum: 'move' + 1
      }
    },
}
</script>

<style scoped>
.home {
  height: 100vh;
  color: var(--main_white);
}

.move1 {
    position: absolute;
    top: -300px;
    left: -200px;
}

.move2 {
    position: absolute;
    top: -150px;
    left: -400px;
}

.move3 {
    position: absolute;
    top: -50px;
    left: -200px;
}

.move4 {
    position: absolute;
    top: 50px;
    left: -500px;
}

.move5 {
    position: absolute;
    top: 150px;
    left: -150px;
}

.move6 {
    position: absolute;
    top: -300px;
    left: 700px;
}

.move7 {
    position: absolute;
    top: -150px;
    left: 900px;
}

.move8 {
    position: absolute;
    top:  0px;
    left: 800px;
}

.move9 {
    position: absolute;
    top:  150px;
    left: 900px;
}

.move10 {
    position: absolute;
    top: 200px;
    left: 700px;
}

.move {
    font-size: 16px;
    color: var(--font-color);
    width: 50px;
}

.main-page {
    width: 100%;
    height: 100vh;
    overflow: hidden;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    /* flex-direction: column; */
}

.snow-box {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    overflow: hidden;
}

.snow {
    width: 10px;
    height: 10px;
    background: #4D4D4D;
    border-radius: 50%;
    opacity: 0;
    animation: snow 5s linear infinite;
    position: absolute;
}

@keyframes snow {
    0% {
        opacity: 0;
        transform: translateY(0);
    }

    20% {
        opacity: 1;
        transform: translate(-15px, 20vh);
    }

    40% {
        opacity: 1;
        transform: translate(15px, 40vh);
    }

    60% {
        opacity: 1;
        transform: translate(-15px, 60vh);
    }

    80% {
        opacity: 1;
        transform: translate(0px, 80vh);
    }
    
    100% {
        opacity: 1;
        transform: translateY(100vh);
    }
}

.wave-box {
    border-radius: 5px;
    box-shadow: 0 2px 30px rgba(black, .2);
    background: lighten(#f0f4c3, 10%);
    position: relative;
    transform: translate3d(0, 0, 0);
}

.wave {
    position: absolute;
    top: 50%;
    left: 50%;
    background: #fdfdfd;
    opacity: 0.5;
    width: 600px;
    height: 600px;
    margin-left: -300px;
    margin-top: -300px;
    transform-origin: 50% 48%;
    border-radius: 43%;
    animation: drift 3000ms infinite linear;
    z-index: -1;
}

.wave.-three {
    animation: drift 5000ms infinite linear;
}

.wave.-two {
    animation: drift 7000ms infinite linear;
    opacity: 1;
    background: var(--font-color);
}

.wave-box::after {
    content: '';
    display: block;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(#e8a, 1), rgba(#def, 0) 80%, rgba(white, .5));
    z-index: 11;
    transform: translate3d(0, 0, 0);
}

@keyframes drift {
    from {
        transform: rotate(0deg);
    }

    from {
        transform: rotate(360deg);
    }
}

</style>
  
