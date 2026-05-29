<script setup lang="ts">
import { ref } from 'vue'

const embedCode = `<a href="https://above.gay/" target="_blank"><img src="https://above.gay/88x31.gif" alt="above.gay" /></a>`
const copied = ref(false)

function copyCode() {
  navigator.clipboard.writeText(embedCode)
  copied.value = true
  setTimeout(() => { copied.value = false }, 1000)
}
</script>

<template>
  <div class="container">
    <div class="box">
      <p class="box-title">my button.</p>
      <div class="box-content">
        <p class="subtitle">Feel completely free to put this on your site. Hotlinking is allowed.</p>
        <div class="button-row">
        <img src="/88x31.gif" alt="above.gay" class="web-badge button-preview" />
        <div class="btn-code">
          <code class="mono"><span class="hl-tag">&lt;a</span> <span class="hl-attr">href</span>=<span class="hl-str">"https://above.gay/"</span> <span class="hl-attr">target</span>=<span class="hl-str">"_blank"</span><span class="hl-tag">&gt;</span><span class="hl-tag">&lt;img</span> <span class="hl-attr">src</span>=<span class="hl-str">"https://above.gay/88x31.gif"</span> <span class="hl-attr">alt</span>=<span class="hl-str">"above.gay"</span> <span class="hl-tag">/&gt;</span><span class="hl-tag">&lt;/a&gt;</span></code>
          <button class="copy" @click="copyCode">
            <icon-lucide-check v-if="copied" />
            <icon-lucide-copy v-else />
          </button>
        </div>
        </div>
      </div>
    </div>

    <div class="box">
      <p class="box-title">cool people.</p>
      <div class="box-content">
        <p class="subtitle"><a href="https://github.com/Abovescore/abovegay" style="color: rgb(150 114 255);">Make a PR</a> with your own button and I'll merge it.</p>
        <div class="badge-grid">
          <a href="https://silly.city" target="_blank">
            <img src="/gif/buttons/sillycity.gif" alt="Silly City Webring" class="web-badge" loading="lazy" />
          </a>
          <a href="https://jaymbermations.org" target="_blank">
            <img src="/gif/buttons/jaymber.webp" alt="Jaymbermations" class="web-badge" loading="lazy" />
          </a>
          <a href="https://lyra.horse" target="_blank">
            <img src="/gif/buttons/lyra.horse.png" alt="Rebane2001" class="web-badge" loading="lazy" />
          </a>
          <a href="https://trafficlunar.net" target="_blank">
            <img src="/gif/buttons/trafficlunar.gif" alt="trafficlunar" class="web-badge" loading="lazy" />
          </a>
          <a href="https://centiskor.ch/" target="_blank">
            <img src="/gif/buttons/centiskorch-badge.png" alt="centiskor.ch" class="web-badge" loading="lazy" />
          </a>
        </div>
      </div>
    </div>

    <div class="box">
      <p class="box-title">other.</p>
      <div class="box-content">
        <div class="badge-grid">
          <img src="/gif/buttons/men.png" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/transrights.gif" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/js-warning.gif" class="web-badge" loading="lazy" />
          <iframe src="//incr.easrng.net/badge?key=abovedotgay" class="web-badge" style="background: url(//incr.easrng.net/bg.gif)" title="increment badge" width="88" height="31" frameborder="0"></iframe>
          <a href="https://www.repair.org/stand-up" target="_blank" rel="noopener noreferrer">
            <img src="/gif/buttons/right-to-repair.webp" class="web-badge" loading="lazy" />
          </a>
          <a href="https://www.qbittorrent.org/" target="_blank" rel="noopener noreferrer">
            <img src="/gif/buttons/sharing.gif" class="web-badge" loading="lazy" />
          </a>
          <a href="https://ublockorigin.com/" target="_blank" rel="noopener noreferrer">
            <img src="/gif/buttons/ublock.png" class="web-badge" loading="lazy" />
          </a>
          <a href="https://uscpr.org/" target="_blank" rel="noopener noreferrer">
            <img src="/gif/buttons/standwith.webp" class="web-badge" loading="lazy" />
          </a>
          <img src="/gif/buttons/tomscott.webp" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/queen.gif" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/anythingbut.gif" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/archlinux.png" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/kde-now.gif" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/nomobilebanner.jpg" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/pbsource.png" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/steam.gif" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/tested-on-firefox.webp" class="web-badge" loading="lazy" />
          <img src="/gif/buttons/blockads.gif" class="web-badge" loading="lazy" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 32px;
  padding: 40px 0;
  color: #e0daf0;
}

.box {
  border: 1px solid rgb(150 114 255 / 0.15);
  border-radius: 5px;
  overflow: hidden;
}

.box-title {
  margin: 0;
  padding: 10px;
  font-size: 14px;
  font-weight: 600;
  color: rgb(150 114 255 / 0.7);
  border-bottom: 1px solid rgb(150 114 255 / 0.1);
}

.box-content {
  padding: 15px;
}

.subtitle {
  margin: 0 0 12px;
  font-size: 14px;
  color: rgb(200 190 220 / 0.7);
}

.button-row {
  display: flex;
  align-items: center;
  gap: 12px;
}

.button-preview {
  flex-shrink: 0;
}

.btn-code {
  flex: 1;
  min-width: 0;
  position: relative;
  padding: 10px 40px 10px 14px;
  border: 1px solid rgb(150 114 255 / 0.15);
  border-radius: 6px;
  background: rgb(150 114 255 / 0.04);
  overflow: hidden;
}

.btn-code code {
  font-size: 13px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  display: block;
}

.hl-tag {
  color: #e06c75;
}

.hl-attr {
  color: #d19a66;
}

.hl-str {
  color: #98c379;
}

.copy {
  position: absolute;
  top: 50%;
  right: 8px;
  transform: translateY(-50%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 6px;
  border: none;
  outline: none;
  border-radius: 5px;
  background: transparent;
  color: #9b6dff;
  cursor: pointer;
  transition: background 0.2s;
}

.copy:hover {
  background: rgb(150 114 255 / 0.15);
}

.badge-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  justify-content: center;
}

.web-badge {
  display: block;
  width: 88px;
  height: 31px;
  image-rendering: pixelated;
}

.badge-grid a {
  display: block;
  transition: opacity 0.2s;
}

.badge-grid a:hover {
  opacity: 0.8;
}
</style>
