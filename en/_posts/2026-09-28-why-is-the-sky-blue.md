---
title: Why is the sky blue?
description: Sunlight is white and air is transparent, yet the sky is blue. The answer is a fourth-power law worked out in 1871.
ref: why-is-the-sky-blue
tags: [Physics, Atmosphere]
authors: [Scilophone Team]
cover: /assets/img/posts/why-is-the-sky-blue/cover.svg
cover_alt: Illustration of a sky fading from deep blue overhead to orange at a sunset horizon.
instagram: https://www.instagram.com/scilophone/
key_points:
  - Sunlight contains every colour. Air molecules scatter short, blue wavelengths far more than long, red ones.
  - Scattering strength rises as $$1/\lambda^4$$, so blue light at 450 nm scatters about 6 times more than red.
  - The same effect makes sunsets red, while much larger cloud droplets scatter all colours equally and look white.
math: true
sample: true
---

Look straight up on a clear day and the colour you see is not the colour of the Sun, which is close to white, and not the colour of air, which has none. It comes from how the air redirects sunlight on its way to you.

## Sunlight is every colour at once

White sunlight is a mixture of wavelengths, from about 380 nanometres (violet) to about 750 nanometres (red). The air it passes through is mostly nitrogen and oxygen molecules. Each one is about 0.3 nanometres across, more than a thousand times smaller than the wavelength of visible light.

## Small particles prefer short waves

When light meets a particle much smaller than its wavelength, the light's electric field makes the particle's electrons oscillate. The oscillating electrons send light back out in all directions. In 1871, Lord Rayleigh showed that the intensity of this scattered light depends very steeply on wavelength:[^rayleigh]

$$
I \propto \frac{1}{\lambda^{4}}
$$

Halve the wavelength and the scattering becomes sixteen times stronger. Comparing blue light at 450 nm with red light at 700 nm:

$$
\frac{I_{450}}{I_{700}} = \left(\frac{700}{450}\right)^{4} \approx 5.9
$$

{% include figure.html src="/assets/img/posts/why-is-the-sky-blue/scattering-en.svg" alt="A curve falling steeply from left to right across the visible spectrum. Scattering is about 9.4 times the red value at 400 nm, 5.9 times at 450 nm, and 1 at 700 nm." caption="Rayleigh scattering across the visible spectrum, relative to red light at 700 nm. The coloured strip under the axis shows each wavelength's colour." %}

Any patch of sky away from the Sun is lit only by sunlight that air molecules have scattered toward you, and that light is dominated by the short wavelengths.

> **Did you know?** Scattered skylight is also partly polarised. Bees and some desert ants use the pattern of that polarisation to navigate.
{: .callout}

## So why isn't the sky violet?

If shorter always means stronger, violet should win. Two things stop it.[^smith]

1. **The Sun sends less violet.** Sunlight contains less violet than blue to begin with, so there is less violet available to scatter.
2. **Our eyes see the mix, not the peak.** Skylight is not one wavelength but a broad blend weighted toward the short end. Our eyes are much less sensitive to violet than to blue, and our three types of cone cell register the whole blend as a pale, slightly washed-out blue.

## Red sunsets, white clouds

At sunrise and sunset, sunlight reaching you from the horizon travels through almost 40 times as much air as it does at noon. Along the way, most of the blue is scattered out of the direct beam, and the oranges and reds are what remain.

Clouds follow different rules. Their water droplets are typically around 10 micrometres across, larger than any visible wavelength. At that size scattering is nearly the same for every colour, so clouds send back all of sunlight's colours together and look white.[^bohren]

[^rayleigh]: J. W. Strutt (Lord Rayleigh), "On the light from the sky, its polarization and colour", *Philosophical Magazine* 41, 107–120 (1871).
[^smith]: G. S. Smith, "Human color vision and the unsaturated blue color of the daytime sky", *American Journal of Physics* 73, 590–597 (2005).
[^bohren]: C. F. Bohren and D. R. Huffman, *Absorption and Scattering of Light by Small Particles* (Wiley, 1983).
