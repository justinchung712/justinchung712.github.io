---
title: "Day 1: Getting Started with Firmware"
last_modified_at: 2026-11-20T14:51:00-08:00
---

Hi! I'm Justin Chung, and I studied computer science during my time as an undergrad student at UCSB.
While working as an AI reviewer, I recently found myself picking up a newfound interest in firmware and embedded systems engineering.

There are no more assigned homework problems, projects, or exams to act as checkpoints for my growth, which is where this blog comes in!
Not only will I show you the cool things about firmware engineering I'll get to learn about, I'll also be making sure that I'm learning and improving my skills at a solid pace.

I also won't really be worrying too much about my writing style or how sophisticated my writing sounds here — the more important thing is getting to show you all the interesting things about embedded systems, microcontrollers, and all that fun stuff.
This also means absolutely no AI use whatsoever anywhere on this site, for authenticity.
Come along for the ride!

### Here's what went down today:

* Learned some STM32 basics:
  * Obtained an STM32 Nucleo-F446RE
  * Started a project from STM32CubeMX + STM32CubeIDE
  * Blinked the onboard LED and output messages via UART

## Key Concepts/Challenges:

### UART

* First time using `screen` since I'm on Mac, so no putty
* Why specifically use `USART2` instead of `USART1`, `USART3`, `USART6`, `UART4`, or `UART5`?
* What even is the difference between USART and UART?
* From my understanding so far, UART is strictly asynchronous while USART can be synchronous, but I'm using asynchronous anyways.
* BUT used USART2 specifically because based on the schematic for this microcontroller, USART TX and RX is connected to the ST-LINK RX and TX. And that USART is linked to pins PA2 and PA3, which are under USART2 in CubeMX. And I need the one that I can read from ST-LINK so I can actually read the UART output from my USB-connected Mac.
* Understanding baud rate

### Reading the Schematic

