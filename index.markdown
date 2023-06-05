---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home #original, with list of 'Posts'
layout: default
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
            <p>I am an aspiring security engineer, graduated with a bachelor’s in computer engineering currently improving my knowledge of AI, security, and cloud technology.</p>
            <span style="font-size:0.7em; color:#C3C3C3;">
              <p>Last updated: 05 Jun 2023.</p>
            </span>
          </span>
    </div>
  </div>
</div>

<br>
<h2>Projects</h2>
<div>
  <time datetime="2022-01-10" style="color:gray; font-size:90%;" >10 January 2022</time>
  <h3><a href="/projects/2022/01/10/sdn-ddos-entropy.html">Entropy-based Detection Method against DoS/DDoS attacks in an SDN-IoT environment</a></h3>
</div>
<div>
  <time datetime="2021-01-27" style="color:gray; font-size:90%;" >27 January 2021</time>
  <h3><a href="/projects/2021/01/27/sdg-game.html">The SDG Game - Building awareness around the SDG goals</a></h3>
</div>

<!-- testimonials -->

<br>
<h2>Contacts</h2>
<div style="text-align: center;">
  <p>Want to get in touch? Contact me through these!</p>
  <br>
  <p>
  <a href="mailto: abdul.adhim277@gmail.com">
    <img src="./images/contacts/email.png" title="Email" width="30"/>
  </a> &emsp; 
  <a target="_blank" href="https://www.linkedin.com/in/abdul-adhim">
    <img src="./images/contacts/linkedin.png" title="LinkedIn" width="30"/>
  </a>&emsp;
  <a target="_blank" href="https://t.me/abdadhim">
    <img src="./images/contacts/telegram.png" title="Telegram" width="30"/> &emsp;
  </a>
  <a target="_blank" href="https://wa.me/6281234428985">
    <img src="./images/contacts/whatsapp.png" title="WhatsApp" width="30"/>
  </a>
  </p>
</div>
<!-- max-width + centering -->
<!-- https://www.codegrepper.com/code-examples/css/max+width+and+centering -->
