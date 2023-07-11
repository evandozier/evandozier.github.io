---
layout: post
title: Rebuilding and Testing a Marantz 2385
tags: hifi
---

I got this 2385 in a trade. It was in rough shape and not functional. The specific-to-this-model volume knob and shaft was missing as were many of the screws holding it together

Here are a couple of pics after cleaning it up before restoration:
![]({{ site.baseurl }}/images/hifi/original/amp-2385-1.jpg)
![]({{ site.baseurl }}/images/hifi/original/amp-2385-2.jpg)
![]({{ site.baseurl }}/images/hifi/original/amp-2385-3.jpg)
![]({{ site.baseurl }}/images/hifi/original/amp-2385-4.jpg)

## Restoration

I started with replacing all of the burned out lamps with LEDs. The function panel was already LEDs and working, so I left that alone

I then restored the following boards:
- P400 - Phono & Selector
- P700 - Main Amp
- P850 - Power Supply
- PE00 - Pre, Tone Amp
- PN00 - Audio Muting Circuit
- PQ00 - Soft Start Circuit
- PS00 - Switches Board
- PT00 - Filter Amp Circuit

This restoration consisted of replacing all electrolytic caps with modern Nichicon, Panasonic, or Kemet equivalents, replacing all known problem transistors with modern equivalents, and replacing the filter caps with 4 10k modern caps.

The filter caps required designing and 3d printing a new capacitor caddy to handle the difference and can be found here: [Thingiverse - Marantz Filter Adapters](https://www.thingiverse.com/thing:6117276)

The volume knob and shaft was also missing. Originally, I [designed and 3d printed](https://www.thingiverse.com/thing:6117280) a replacement knob that would go into the existing hole and engage the potentiometer mechanism. After proving the concept, I purchased 5mm stainless steel rod from amazon and ground it down with a cutoff wheel to fit what I 3d printed.

## Testing:
Since the Marantz 2385 has pre-out and amp-in connections, I tested the amp separate from the preamp+amp to compare the performance of the amp versus the preamp

### Max Power
Factory Specs:
- Rated Power for 8 ohm load: 185 wpc across 20-20k Hz @ 0.05% THD

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-Max Power.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-Max Power.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-Max Power.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-Max Power.png) |

### Amplitude Swept THD
Factory Specs:
- 0.05% THD or -66 dB

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-Amplitude Swept THD.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-Amplitude Swept THD.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-Amplitude Swept THD.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-Amplitude Swept THD.png) |

### Averaged Frequency Response
Factory Specs:
- Power Amp Only: +/- 0.2 dB @ 1 Watt, 20-20kHz
- Preamp + Power Amp: +/- 1 dB from 10-50k Hz

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-Averaged Frequency Response.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-Averaged Frequency Response.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-Averaged Frequency Response.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-Averaged Frequency Response.png) |

### Continuous Frequency Sweep
Factory Specs:
- Power Amp Only: +/- 0.2 dB @ 1 Watt, 20-20kHz
- Preamp + Power Amp: +/- 1 dB from 10-50k Hz

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-Continuous Frequency Sweep.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-Continuous Frequency Sweep.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-Continuous Frequency Sweep.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-Continuous Frequency Sweep.png) |

### Discrete Frequency Sweep
Factory Specs:
- Power Amp Only: +/- 0.2 dB @ 1 Watt, 20-20kHz
- Preamp + Power Amp: +/- 1 dB from 10-50k Hz

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-Discrete Frequency Sweep.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-Discrete Frequency Sweep.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-Discrete Frequency Sweep.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-Discrete Frequency Sweep.png) |

### One Shot IMD
Factory Specs:
- 0.05% or -66 dB

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-One Shot IMD.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-One Shot IMD.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-One Shot IMD.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-One Shot IMD.png) |

### One Shot Phase, Gain, Distortion

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-One Shot Phase, Gain, Distortion.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-One Shot Phase, Gain, Distortion.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-One Shot Phase, Gain, Distortion.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-One Shot Phase, Gain, Distortion.png) |

### One Shot Metrics
Factory Specs:
- IMD 0.05%
- SNR ref to 775mV Input: 92 dB

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-One Shot Metrics.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-One Shot Metrics.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-One Shot Metrics.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-One Shot Metrics.png) |

### Settled Dynamic Range

| Left Channel | Right Channel |
| ---- | ---- |
| Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Left-Settled Dynamic Range.png) | Amp Only ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385_AmpOnly/09072023-1429-Right-Settled Dynamic Range.png) |
| Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Left-Settled Dynamic Range.png) | Amp and Preamp ![]({{ site.baseurl }}/images/tests/marantz2385/Marantz_2385/09072023-1447-Right-Settled Dynamic Range.png) |

