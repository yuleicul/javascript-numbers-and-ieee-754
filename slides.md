---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
# some information about your slides, markdown enabled
title: 0.1 + 0.2 ≠ 0.3 ?
info: |
  ## 0.1 + 0.2 ≠ 0.3 ?
  JavaScript numbers and IEEE 754
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
---

# 0.1 + 0.2 ≠ 0.3 ?

JavaScript numbers and IEEE 754

<br />
<br />

Yulei Chen

March 2024

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/yuleicul/javascript-numbers-and-ieee-754" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---
class: bg-black text-red
---

# Disclaimer

<br />

I am NOT the creator of this content. I'm just a messenger.

This content was originally presented by Bartek Szopka at JSConf EU 2013. You can watch the recording of the original speech on Youtube: [Bartek Szopka: Everything you never wanted to know about JavaScript numbers - JSConf EU 2013](https://www.youtube.com/watch?v=MqHDDtVYJRI).

If there's anything mind-blowing in my presentation, that's all thanks to the creator.
If there's anything wrong in my presentation, that's all on me.
