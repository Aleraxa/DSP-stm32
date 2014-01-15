This repository contains source code for the article [Realtime DSP with the STM32F4](http://www.wolinlabs.com/blog/adc_dsp_dac.html) 

<br>
The project is buildable with the GNU Tools for ARM Embedded Processors toolchain v4.7.3, maintained by ARM Ltd.   I used Ubuntu Linux 12.04LTS for the build environment.  Code runs on an STM32F4 Discovery board.


<br>
Contents:

1. ADC_DSP_DAC project code (buildable)
2. STM libraries and headers


<br>
STM's approach toward 'library code': rather than building libraries up front and linking them with your source, you include the individual source files in your project's build.   Some of STM's source files include local headers and modules (i.e. stm32f4xx\_conf.h, stm32f4xx\_it.c/h, system\_stm32f4xx.c, etc) that you modify/store in your source tree.  Because of this, building the library up front wouldn't work properly, as the configuration for some library modules could vary from project to project.




