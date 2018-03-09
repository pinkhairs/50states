<template>
  <div class="wrapper">
    <div class="container">
      <div v-bind:class="['state', layout]">
        <div class="state__image">
          <img :src="this.image" :class="info.key" v-if="info.key != 'idaho' && info.key != 'missouri' && info.key != 'virginia'" />
          <a :href="url" target="_blank" v-if="this.info.key == 'idaho' || this.info.key == 'missouri' || this.info.key == 'virginia'"><img :src="sign" :alt="alt" /></a>
        </div>
        <div class="state__content">
          <span class="state__number">{{ info.number }}</span>
          <h2 class="state__name">{{ info.name }}</h2>
          <div class="author">
            <h3 class="author__name">{{ info.author }}</h3>
            <p class="author__bio">{{ info.bio }}</p>
          </div>
          <div class="state__text">
            <div class="state__story" v-html="info.text">
            </div>
          </div>
        </div>
      </div>
    </div>
    <div v-bind:class="['road-container', info.key]" v-if="info.key == 'alaska'">
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M0.3,4.7c0,0,208-21,211,83S5.1,291.4,5.1,291.4" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M0.3,4.7c0,0,208-21,211,83S5.1,291.4,5.1,291.4" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-if="info.key == 'nevada'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M0.3,4.7c0,0,208-21,211,83S5.1,291.4,5.1,291.4" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M0.3,4.7c0,0,208-21,211,83S5.1,291.4,5.1,291.4" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-if="info.key == 'oregon'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M213.7,5.3c0,0-262.4,71.6-198,139.5s198,242,198,242" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M213.7,5.3c0,0-262.4,71.6-198,139.5s198,242,198,242" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'hawaii'">
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M472.3,5.3c0,0-423-25-464,143c-39.7,162.8,212.3,25.2,183.7,209.2C346,437,473.8,308.4,472.3,315" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M472.3,5.3c0,0-423-25-464,143c-39.7,162.8,212.3,25.2,183.7,209.2C346,437,473.8,308.4,472.3,315" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'minnesota'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M472.3,5.3c0,0-423-25-464,143c-39.7,162.8,212.3,25.2,183.7,209.2C346,437,473.8,308.4,472.3,315" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M472.3,5.3c0,0-423-25-464,143c-39.7,162.8,212.3,25.2,183.7,209.2C346,437,473.8,308.4,472.3,315" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'vermont'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M472.3,5.3c0,0-423-25-464,143c-39.7,162.8,212.3,25.2,183.7,209.2C346,437,473.8,308.4,472.3,315" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M472.3,5.3c0,0-423-25-464,143c-39.7,162.8,212.3,25.2,183.7,209.2C346,437,473.8,308.4,472.3,315" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'colorado'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M4.4,5.3c0,0,262.4,71.6,198,139.5s-198,242-198,242" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M4.4,5.3c0,0,262.4,71.6,198,139.5s-198,242-198,242" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'southCarolina'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M4.4,5.3c0,0,262.4,71.6,198,139.5s-198,242-198,242" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M4.4,5.3c0,0,262.4,71.6,198,139.5s-198,242-198,242" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'kentucky'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M337.3,8.2c0,0-327.1-33-331.8,130.5s324.2,320.3,324.2,320.3" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M337.3,8.2c0,0-327.1-33-331.8,130.5s324.2,320.3,324.2,320.3" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
    <div v-bind:class="['road-container', info.key]" v-else-if="info.key == 'louisiana'">
      <!-- Generator: Adobe Illustrator 22.0.1, SVG Export Plug-In  -->
        <svg version="1.1" class="dashed"
           xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
           x="0px" y="0px" width="321px" height="441" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
           xml:space="preserve">
        <defs>
        </defs>
        <path d="M0.3,4.7c0,0,208-21,211,83S5.1,291.4,5.1,291.4" fill="none" stroke="#F6F4E5" stroke-width="9" stroke-miterlimit="10" stroke-dasharray="12,28" />
      </svg>
      <svg version="1.1" class="solid" :id="info.key"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:a="http://ns.adobe.com/AdobeSVGViewerExtensions/3.0/"
         x="0px" y="0px" width="321px" height="441px" viewBox="0 0 214.3 294.2" style="enable-background:new 0 0 214.3 294.2;"
         xml:space="preserve">
      <defs>
      </defs>
      <path class="animate" d="M0.3,4.7c0,0,208-21,211,83S5.1,291.4,5.1,291.4" fill="none" stroke="#B94B39" stroke-width="8" stroke-miterlimit="10" stroke-dasharray="28,12" />
      </svg>
    </div>
  </div>
</template>

<script>
import Rellax from 'rellax'
import Vivus from 'vivus'

export default {
  data () {
    return {
      image: '',
      url: '',
      sign: '',
      alt: '',
    }
  },
  props: ['info', 'layout'],
  mounted() {
    this.info.text = this.replaceAll(this.info.text, /\n/, '<br>')
    this.image = require(`@/assets/${this.info.key}.png`)
    if (window.outerWidth > 1024 && this.info.key != 'idaho' && this.info.key != 'missouri' && this.info.key != 'virginia') {
      this.parallax('.'+this.info.key)
    }
    let road
    if (document.getElementById(this.info.key) && this.info.key != 'idaho' && this.info.key != 'missouri' && this.info.key != 'virginia') {
      new Vivus(this.info.key, { type: 'sync' })
    }
    if (this.info.key == 'idaho') {
      this.url = 'https://pst.pcdfusion.com/pcd/Order?iKey=I**WEB'
      this.sign = require(`@/assets/subscribe-sign.png`)
      this.alt = 'Subscribe to Pacific Standard'
    } if (this.info.key == 'missouri') {
      this.url = 'https://psmag.com/page/newsletter'
      this.sign = require(`@/assets/newsletter-sign.png`)
      this.alt = 'Sign up for our newsletter'
    } if (this.info.key == 'virginia') {
      this.url = 'https://psmag.com/'
      this.sign = require(`@/assets/website-sign.png`)
      this.alt = 'Visit Pacific Standard'
    }
  },
  methods: {
    replaceAll: function(target, search, replacement) {
      return target.replace(new RegExp(search, 'g'), replacement);
    },
    parallax : function(className) {
      var rellax = new Rellax(className, {
          center: true,
          round: true,
          vertical: true,
          horizontal: false
      });
    }
  }
}
</script>

<style lang="scss">
br {
  display: block;
  margin-bottom: 8px;
  content: " ";
}
.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  position:relative;
}
.wrapper {
  position:relative;
}
.road-container {
  position:absolute;
  left:0;
  top:0;
  width:100%;
  height:200vh;
  z-index:0;
}
.dashed {
  position:absolute;
  top:0;
  left:0;
  height:100vh;
  z-index:2;
  .hawaii &, .kentucky &, .minnesota &, .oregon &, .vermont & {
    right:0;
    left:auto;
  }
}
.solid {
  position:absolute;
  top:0;
  left:0;
  height:100vh;
  z-index:1;
  .hawaii &, .kentucky &, .minnesota &, .oregon &, .vermont & {
    right:0;
    left:auto;
  }
}
.state {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 48px 0;
  &__text {
    flex: 0 0 50%;
    height: 50vh;
    overflow: auto
  }
  &__image {
    flex: 0 0 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    position:relative;
  }
  &.text-left {
    a {
      color:#b94b39;
    }
    flex-direction: row-reverse
  }
  &__name {
    padding:6px 0;
    border-top: 2px dotted #BB4B34;
    border-bottom: 2px dotted #BB4B34;
  }
  &__number {
    font-family: 'maritime-outline';
    font-size: 72px;
  }
  &__story {
    padding-bottom:80px;
    @media (max-width:768px) {
      padding-bottom:0;
    }
    a {
      text-decoration:underline;
    }
  }
  &__content {
    background:rgba(#f6f4e5,1);
    position:relative;
    box-shadow:0 50px 50px 0 rgba(#f6f4e5,1);
    z-index:2;
    &:after {
      /* Permalink - use to edit and share this gradient: http://colorzilla.com/gradient-editor/#f6f4e5+0,f6f4e5+100&0+0,1+100 */
      background: -moz-linear-gradient(top, rgba(246,244,229,0) 0%, rgba(246,244,229,1) 100%); /* FF3.6-15 */
      background: -webkit-linear-gradient(top, rgba(246,244,229,0) 0%,rgba(246,244,229,1) 100%); /* Chrome10-25,Safari5.1-6 */
      background: linear-gradient(to bottom, rgba(246,244,229,0) 0%,rgba(246,244,229,1) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
      filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00f6f4e5', endColorstr='#f6f4e5',GradientType=0 ); /* IE6-9 */
      height:80px;
      content:' ';
      display:block;
      width:100%;
      position:absolute;
      bottom:0;
      left:0;
      z-index:33;
      @media (max-width:768px) {
        display:none;
      }
    }
  }
}
.author {
  border-bottom: 4px solid #BB4B34;
  padding:12px 0;
  margin-bottom:20px;
  &__name {
    font-family: 'merriweather';
    font-weight:900;
    font-size:15px;
    font-style:italic;
  }
  &__bio {
    font-size:13px;
    text-transform: uppercase;
  }
}
.text-left {
  .state__number, .state__story {
    color:#BB4B34
  }
}
@media (max-width: 768px) {
  .container {
    display: block;
    padding:2rem;
    height: auto
  }
  .state {
    display: block !important;
    &__text, &__image {
      margin: 24px 0;
      display: block !important;
    }
    &__text {
      height: auto
    }
  }
}
/* image properties */
.state__image img {
  width: 320px;
  margin: 0 auto;
  will-change:transform;
  position:relative;
  z-index:1;
  &.arkansas, &.connecticut, &.hawaii, &.illinois, &.kentucky, &.minnesota, &.nevada, &.northCarolina, &.wyoming, &.newYork {
    width: 480px
  }
  &.idaho, &.montana, &.virginia, &.washington, &.massachusetts, &.arizona {
    width:240px
  }
}
.subscribe-sign {
  position:absolute;
  bottom:0;
  left:0;
  z-index:3;
  width:160px;
}
.website-sign {
  position:absolute;
  top:6rem;
  right:0.5rem;
  width:160px;
  z-index:3;
}
.email-sign {
  position:absolute;
  top:25%;
  width:160px;
  left:0;
  z-index:3
}
</style>
