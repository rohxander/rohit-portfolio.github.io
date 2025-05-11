---
layout: page
title: High-Speed UART Flow Control Application
description: Firmware-level test application to validate UART communication under high-speed conditions.
img: assets/img/uart_flow_control.png
importance: 1
category: Industrial
related_publications: false
---

As part of my role at Microchip Technology, I was responsible for developing a high-speed UART validation application to test **hardware UART flow control (RTS/CTS)**. The tool was designed to validate signal integrity and reliable communication at baud rates up to **10 Mbps**, with final tests achieving stable operation at **25 Mbps**.

### 🔍 Problem

Testing true UART hardware flow control proved challenging with standard USB-to-UART converters. Despite using **FTDI cables** with RTS/CTS support, the **PC’s CTS line remained low**, making the system behave like conventional UART without flow control. Even enabling hardware flow control within **Tera Term** (the initial terminal application used) had no effect — likely due to the abstraction layer introduced by the USB interface.

### 🛠️ My Role & Approach

- Studied PIC32 UART modules in-depth using the reference manual and Harmony v3 framework
- Developed a test firmware application on **WFI32E02** and **PIC32** to evaluate high-speed full-duplex UART
- Identified the baud rate ceiling in Tera Term (~2.5 Mbps) and replaced it with a **Saleae Logic Analyzer** to monitor and verify RTS/CTS transitions at higher speeds
- Debugged scenarios like buffer overruns and misaligned handshaking under stress
- Created reusable documentation and setup guidelines for internal test teams

### ✅ Outcome

The application became part of Microchip’s internal firmware validation toolset and was used in product-level demos and performance evaluations.

### 🔧 Tools & Platforms

PIC32, WFI32, MPLAB Harmony v3, MPLAB X IDE, Saleae Logic Analyzer, FTDI Cables, Tera Term

<!-- Optional: Embed link to source code if available in the future
<a href="https://github.com/rohxander/uart-tool" class="btn btn-sm z-depth-0" target="_blank">
  <i class="fas fa-code"></i> View Source
</a>
-->

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/WFI32E02.png" title="WFI32E02 Development Board" class="img-fluid rounded z-depth-1" %}
  </div>
  <!-- 
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/oscilloscope_uart.jpg" title="Logic analyzer trace during stress test" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/pic32_board.jpg" title="PIC32 test setup" class="img-fluid rounded z-depth-1" %}
  </div>
  -->
</div>

<div class="caption">
  Left: WFI32 Development Board used for UART testing
  <!-- Middle: full-duplex trace on logic analyzer; Right: PIC32 test setup -->
</div>

<!--
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/code_sample.jpg" title="UART initialization snippet" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/test_gui.jpg" title="Test GUI (Python-based)" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Optional: Future section showing firmware GUI or code layout
</div>
-->
