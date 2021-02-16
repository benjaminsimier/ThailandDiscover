<template>
  <div>
      <header>
            <div class="container">
                <div class="menuHeader">
                    <div class="left">
                        <div class="logo">
                            <img src="@/assets/images/logo.svg" alt="">
                        </div>
                    </div>
                    <div class="right">
                        <div class="lineTop">
                        </div>
                        <div class="songPlayer">
                            <div class="player">
                                <span @click.prevent="playSound('/sound/bg.mp3')">
                                    <span>
                                        Listen the place music
                                    </span>
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
      </header>


      <div class="gradientBottom">
      </div>

  </div>
</template>

<script>
export default {
    data() {
        return {
           play: false,
        }
    },

    methods: {
    playSound (sound) {
        if(sound) {
            var audio = new Audio(sound);
            if(this.play == false) {
                audio.play();
                this.play = true;
            } else {
                 this.play = false;
            }
        }
    }
    }
}
</script>

<style>

</style>