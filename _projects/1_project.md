---
layout: page
title: High-Speed UART Flow Control Application
description: Firmware-level test application to validate UART communication under high-speed conditions.
img: assets/img/uart flow control.png
importance: 1
category: work
related_publications: false
---

As part of my role at Microchip Technology, I worked on developing and validating a UART-based communication tool designed to ensure robust high-speed data transfer using hardware flow control.

The application focused on testing UART interfaces at varying baud rates, under real-time operating conditions, while ensuring consistent buffer handling, no data loss, and clean signal behavior — especially at 460800 and 921600 bps.

**Objective**  
To validate MCU UART hardware flow control (RTS/CTS) across edge-case timing scenarios, and establish internal tooling for product demos and certification readiness.

**My Role**

- Wrote firmware-level test application using MPLAB Harmony drivers
- Configured and tested hardware UART on WFI32 and PIC32 platforms
- Used oscilloscopes and logic analyzers to monitor RTS/CTS signal integrity
- Logged and resolved buffer overflow edge cases during full-duplex testing
- Created documentation to assist internal teams with porting and reuse

**Tools & Platforms**  
PIC32, WFI32, MPLAB X IDE, MPLAB Harmony, Salea Logic Analyzer, Digital Oscilloscopes

<!--
You may want to embed links to code or design docs here later
<a href="https://github.com/rohxander/uart-tool" class="btn btn-sm z-depth-0" target="_blank">
  <i class="fas fa-code"></i> View Source
</a>
-->

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/WFI32E02.png" title="WFI32 Development Board was used for UART testing" class="img-fluid rounded z-depth-1" %}
  </div>
    <!-- <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/oscilloscope_uart.jpg" title="Logic analyzer trace during stress test" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pic32_board.jpg" title="PIC32 test setup" class="img-fluid rounded z-depth-1" %}
    </div> -->
</div>

<!-- <div class="caption">
    Left: RTS/CTS at high-speed; Middle: full-duplex trace on logic analyzer; Right: target board used for tests.
</div> -->

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
    (Optional future section showing test interface and firmware code layout)
</div>
-->
