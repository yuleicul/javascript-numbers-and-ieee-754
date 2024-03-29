# 0.1 + 0.2 ≠ 0.3

This is a knowledge sharing about JavaScript Numbers and IEEE 754.

Recording: [Talk Clone: Everything You Never Wanted to Know About JavaScript Numbers by Bartek Szopka @jsconf\_ - YouTube](https://www.youtube.com/watch?v=1rfE8P5T6Yo&t=1480s)

Slides: [0.1 + 0.2 ≠ 0.3 ? - Slidev](https://javascript-numbers-and-ieee-754.vercel.app/1)

## References

[IEEE-754 Floating Point representation explained](https://bartaz.github.io/ieee754-visualization/)

[Bartek Szopka: Everything you never wanted to know about JavaScript numbers -- JSConf EU 2013 - YouTube](https://www.youtube.com/watch?v=MqHDDtVYJRI)

<details>

<summary>Outline draft</summary>

## Outline

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

</details>
