---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<!-- <span style="font-size:1.7em;"> -->
<!-- <img style="float: right;" src="./images/memoji.png"> -->
<!-- ![image alt <](./images/memoji.png) -->

<!-- NOTE: text align to left, when screen is smaller depends on Jekyll config I think. -->

<style>
  .columns {
    Width: 100%;
  }

  .column {
    width: 100%;
    /* word-wrap: break-word;
    max-width: 500px; */
  }

  @media (min-width: 48em) {
    .column {
      width: 50%;
      float: left;
    }

    .columns {
      content: "";
      display: table;
      clear: both;
    }

    .img-container {
      text-align: center;
    }

    .noBorder {
        border:none !important;
    }
</style>

<div class="columns">
  <div class="column img-container" style="text-align: center;">
    <img src="./images/memoji.png" alt="drawing" width="200" />
    <br>
    <br>
  </div>
  <div class="column">
    <div style="max-width: 450px; margin: 0 auto !important; float: none !important;">
          <span style="font-size:1.5em;">
            <p>Hi, I am Abdul Adhim!</p>
          </span>
          <span style="font-size:1.2em;">
            <p>I am a computer engineering student based in Tokyo, Japan. Learning about fields like network system,
              system
              engineering, and programming.</p>
            <span style="font-size:0.6em; color:#C3C3C3;">
              <p>Latest featured work : <a href="/projects/2022/01/10/sdn-ddos-entropy.html" title=""
                  style="color:#C3C3C3;">Entropy-based Detection Method against DoS/DDoS attacks in an SDN-IoT
                  environment</a></p>
            </span>
          </span>
    </div>
  </div>
</div>

<br>

<!-- max-width + centering -->
<!-- https://www.codegrepper.com/code-examples/css/max+width+and+centering -->
