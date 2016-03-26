# html5-audio-player

## 1. introduce
html5 audio player(with playlist) using flexbox, svg, css animations and  js api.

forked from @k-ivan at http://codepen.io/k-ivan/pen/pJMLmJ

demo: [html5-audio-player](http://blog.tianqi.at/html5-audio-player/ 'html5-audio-player demo')

<iframe src='http://blog.tianqi.at/html5-audio-player/' height='260px' width='100%'>

## 2. how to use

first insert follow html code to your html file

```html
<!-- Audio player div begin-->
<div class="ap" id="ap">
<div class="ap-inner">
<div class="ap-panel">
  <div class="ap-item ap--playback">
    <button class="ap-controls ap-prev-btn">
      <svg xmlns="http://www.w3.org/2000/svg" fill="#ffffff" height="24" viewBox="0 0 24 24" width="24">
          <path d="M6 6h2v12H6zm3.5 6l8.5 6V6z"/>
          <path d="M0 0h24v24H0z" fill="none"/>
      </svg>
    </button>
    <button class="ap-controls ap-toggle-btn">
      <svg xmlns="http://www.w3.org/2000/svg" fill="#fff"  height="30" viewBox="0 0 24 24" width="30" class="ap--play">
        <path d="M8 5v14l11-7z"/>
        <path d="M0 0h24v24H0z" fill="none"/>
      </svg>
      <svg xmlns="http://www.w3.org/2000/svg" fill="#ffffff" height="30" viewBox="0 0 24 24" width="30" class="ap--pause">
          <path d="M6 19h4V5H6v14zm8-14v14h4V5h-4z"/>
          <path d="M0 0h24v24H0z" fill="none"/>
      </svg>
    </button>
    <button class="ap-controls ap-next-btn">
      <svg xmlns="http://www.w3.org/2000/svg" fill="#ffffff" height="24" viewBox="0 0 24 24" width="24">
          <path d="M6 18l8.5-6L6 6v12zM16 6v12h2V6h-2z"/>
          <path d="M0 0h24v24H0z" fill="none"/>
      </svg>
    </button>
  </div>
  <div class="ap-item ap--track">
    <div class="ap-info">
      <div class="ap-title">Unknown</div>
      <div class="ap-time">
        <span class="ap-time--current">--</span>
        <span> / </span>
        <span class="ap-time--duration">--</span>
      </div>

      <div class="ap-progress-container">
        <div class="ap-progress">
          <div class="ap-bar"></div>
          <div class="ap-preload-bar"></div>
        </div>
      </div>

    </div>
  </div>
  <div class="ap-item ap--settings">
    <div class="ap-controls ap-volume-container">
      <button class="ap-volume-btn">
        <svg fill="#ffffff" height="48" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg" class="ap--volume-on">
            <path d="M3 9v6h4l5 5V4L7 9H3zm13.5 3c0-1.77-1.02-3.29-2.5-4.03v8.05c1.48-.73 2.5-2.25 2.5-4.02zM14 3.23v2.06c2.89.86 5 3.54 5 6.71s-2.11 5.85-5 6.71v2.06c4.01-.91 7-4.49 7-8.77s-2.99-7.86-7-8.77z"/>
            <path d="M0 0h24v24H0z" fill="none"/>
        </svg>
        <svg xmlns="http://www.w3.org/2000/svg" fill="#ffffff" height="48" viewBox="0 0 24 24" width="24" class="ap--volume-off">
            <path d="M7 9v6h4l5 5V4l-5 5H7z"/>
            <path d="M0 0h24v24H0z" fill="none"/>
        </svg>
      </button>
      <div class="ap-volume">
        <div class="ap-volume-progress"><div class="ap-volume-bar"></div></div>
      </div>
    </div>
    <button class="ap-controls ap-repeat-btn">
      <svg fill="#ffffff"  height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 0h24v24H0z" fill="none"/>
          <path d="M7 7h10v3l4-4-4-4v3H5v6h2V7zm10 10H7v-3l-4 4 4 4v-3h12v-6h-2v4z"/>
      </svg>
    </button>
    <button class="ap-controls ap-playlist-btn">
      <svg fill="#ffffff" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 0h24v24H0z" fill="none"/>
          <path d="M15 6H3v2h12V6zm0 4H3v2h12v-2zM3 16h8v-2H3v2zM17 6v8.18c-.31-.11-.65-.18-1-.18-1.66 0-3 1.34-3 3s1.34 3 3 3 3-1.34 3-3V8h3V6h-5z"/>
      </svg>
    </button>
  </div>
</div>
</div>
</div>
<!-- Audio player div end-->
```
then insert follow javascript code to your html file

```javascript
<!-- Audio player js begin-->
<script src="js/AudioPlayer.js"></script>

<script>
    // test image for web notifications
    var iconImage = null;

    AP.init({
        volume   : 0.7,
        notification: false,
        playList: [
            {'icon': iconImage, 'title': 'Try Everything', 'file': 'mp3/try-everything.mp3'},
            {'icon': iconImage, 'title': 'Let It Go', 'file': 'http://blog.tianqi.at/html5-audio-player/mp3/let-it-go.mp3'}
      ]
    });
</script>
<!-- Audio player js end-->

```
it will work!
