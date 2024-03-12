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

March 11, 2024

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub" title="Open in GitHub"
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

---

# JavaScript Numbers and IEEE 754

- Unexpected behaviors

  - 0.1 + 0.2: type and result
  - Number.MAX_SAFE_INTEGER + 1: +1 and +2
  - NaN: typeof ===
  - Python / Java

- To find the answer

  - mdn
  - wikipedia
  - implemented by xxx languages

- Visualization of IEEE 754

  - general ideals of 3 parts and their bits: 1, 11, 52 (1 hidden)
  - sign: negative and positive
  - exponent: the position of point, floating point, offset binary notation
  - significand: the most important part, integer and fraction
    - try: 1, 2, 3, 4
    - try: 1.5, 1.25, 1.75
    - 1.1 (the problem of 0.1 + 0.2 solved) (2 factors)
    - Number.MAX_SAFE_INTEGER 9007199254740991 (1-bit gap, 2-bit gap)
    - Definitions for `0`, `Infinity` and `NaN`
      - 0, -0, equality, detected by `Object.is`
      - Infinity
      - NaN, `typeof` is number defined by 64 bits like any other number, any bit change leads to NaN so NaN === NaN

- Summary
  - 2024.3
  - 1.5
  - can never present some fractions accurately, eg. 1.1
  - can only present part of numbers larger than Number.MAX_SAFE_INTEGER
  - Special definitions for some special numbers in JavaScript
    - 0
    - Infinity
    - NaN
