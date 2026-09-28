---
title: 天空為甚麼是藍色的？
description: 陽光是白色的，空氣是透明的，天空卻是藍色的。答案是 1871 年發現的一條四次方定律。
ref: why-is-the-sky-blue
tags: [物理, 大氣科學]
authors: [Scilophone 團隊]
cover: /assets/img/posts/why-is-the-sky-blue/cover.svg
cover_alt: 插圖：天空由頭頂的深藍漸變至日落地平線的橙色。
instagram: https://www.instagram.com/scilophone/
key_points:
  - 陽光包含所有顏色。空氣分子散射短波長的藍光，遠比散射長波長的紅光多。
  - 散射強度與 $$1/\lambda^4$$ 成正比，所以 450 nm 的藍光散射量約為紅光的 6 倍。
  - 同一原理令日落變紅；而雲的水滴大得多，對所有顏色散射程度相若，所以看起來是白色。
math: true
sample: true
---

在晴天抬頭望向天空，你看到的顏色既不是太陽的顏色（接近白色），也不是空氣的顏色（空氣本身無色）。它來自空氣在陽光射向你的途中，如何改變光的方向。

## 陽光同時包含所有顏色

白色的陽光由不同波長的光混合而成，由大約 380 納米（紫色）到大約 750 納米（紅色）。陽光穿過的空氣主要由氮分子和氧分子組成，每個分子直徑約 0.3 納米，比可見光的波長小一千倍以上。

## 小粒子偏愛短波

當光遇上比其波長小得多的粒子時，光的電場會令粒子中的電子振動，振動的電子再把光向四方八面發射出去。1871 年，瑞利勳爵（Lord Rayleigh）證明這種散射光的強度與波長有非常密切的關係：[^rayleigh]

$$
I \propto \frac{1}{\lambda^{4}}
$$

波長減半，散射便增強十六倍。比較 450 nm 的藍光與 700 nm 的紅光：

$$
\frac{I_{450}}{I_{700}} = \left(\frac{700}{450}\right)^{4} \approx 5.9
$$

{% include figure.html src="/assets/img/posts/why-is-the-sky-blue/scattering-zh.svg" alt="一條曲線在可見光譜上由左至右急劇下降。400 nm 的散射量約為紅光的 9.4 倍，450 nm 約為 5.9 倍，700 nm 為 1。" caption="可見光譜上的瑞利散射強度，以 700 nm 紅光為基準。橫軸下的彩色條顯示每個波長對應的顏色。" %}

天空中任何遠離太陽的位置，照亮它的都只是被空氣分子散射到你眼中的陽光，而這些光以短波長為主。

> **你知道嗎？** 天空的散射光同時帶有部分偏振。蜜蜂和一些沙漠螞蟻會利用這種偏振圖案來導航。
{: .callout}

## 那為甚麼天空不是紫色？

如果波長越短散射越強，紫色理應勝出。但有兩個原因阻止了它：[^smith]

1. **太陽發出的紫光較少。** 陽光中的紫光本來就比藍光少，可供散射的紫光自然也較少。
2. **眼睛看到的是混合色，而非峰值。** 天空的光並非單一波長，而是偏向短波的一大片混合光。我們的眼睛對紫光的敏感度遠低於藍光，三種視錐細胞會把整片混合光感知為一種淡淡的、略為泛白的藍色。

## 紅色的日落，白色的雲

日出和日落時，從地平線射來的陽光要穿過的空氣，差不多是正午時的 40 倍。途中大部分藍光都被散射出直射光線之外，剩下的就是橙色和紅色。

雲則遵循另一套規則。雲中的水滴直徑通常約為 10 微米，比任何可見光的波長都大。在這個尺度下，各種顏色的散射程度幾乎相同，所以雲把陽光的所有顏色一併反射回來，看起來就是白色。[^bohren]

[^rayleigh]: J. W. Strutt（Lord Rayleigh），"On the light from the sky, its polarization and colour"，*Philosophical Magazine* 41，107–120（1871）。
[^smith]: G. S. Smith，"Human color vision and the unsaturated blue color of the daytime sky"，*American Journal of Physics* 73，590–597（2005）。
[^bohren]: C. F. Bohren 與 D. R. Huffman，*Absorption and Scattering of Light by Small Particles*（Wiley，1983）。
