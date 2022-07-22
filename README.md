# MIKROE 4-20 mA R & T Click ![Latest release](https://img.shields.io/github/v/release/Dennis-van-Gils/MIKROE_4_20mA_RT_Click) ![Build Status](https://github.com/dennis-van-gils/MIKROE_4_20mA_RT_Click/workflows/Arduino%20Library%20CI/badge.svg) [![License:MIT](https://img.shields.io/badge/License-MIT-purple.svg)](https://github.com/Dennis-van-Gils/MIKROE_4_20mA_RT_Click/blob/master/LICENSE) [![Documentation](https://img.shields.io/badge/Docs-Doxygen-blue)](https://dennis-van-gils.github.io/MIKROE_4_20mA_RT_Click)

An Arduino library for the 4-20 mA R & T Click Boards of MIKROE.

Supported:
- 4-20 mA R Click (MIKROE-1387)
    - 4-20 mA current loop receiver
    - MCP3201 12-bit ADC SPI chip
    - max SPI clock 1.6 MHz
    - max 100 ksps

- 4-20 mA T Click (MIKROE-1296)
    - 4-20 mA current loop transmitter
	- MCP4921 12-bit DAC SPI chip
	- max SPI clock 20 MHz
	- settling time of 4.5 μs

Single R Click readings tend to fluctuate a lot. To combat the large
fluctuations this library optionally provides an exponential moving average
(EMA) applied to the R Click readings. It does not rely on storing an array
of data and is hence very memory efficient.

It does this by oversampling the R Click readings at a user-supplied
interval. Subsequently, it will low-pass filter the readings using a
smoothing factor that is calculated from a user-supplied low-pass filter
cut-off frequency. Technically, the exponential moving average is a
single-pole infinite-impulse response (IIR) filter.

See the examples in the [examples](./examples) folder.

The API documentation can be found here: https://dennis-van-gils.github.io/MIKROE_4_20mA_RT_Click
