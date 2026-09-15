---
author: Hu bang
pubDatetime: 2026-06-03T00:00:00.000Z
modDatetime: 2026-06-03T00:00:00.000Z
title: I2C Tool(TODO)
slug: i2c-tool
featured: true
draft: false
tags:
  - Projects
  - I2C_Tool
description: "一个 i2c 调试工具."
---

## 项目介绍

一直听说I2C会出现死锁, 但是由于我调试经验比较少, 所以还没有碰到过。而且在真实场景中, 我觉得死锁也是一种偶发性的问题, 在开发过程中很难复现。昨晚我在逛Reddit的时候看到这个东西: [i²c Doctor](https://www.reddit.com/r/embedded/comments/1vy199b/i_got_tired_of_wasting_time_chasing_simple_i%C2%B2c/), 好像挺有用的, 所以打算复刻一下。

实现方案, 首先MCU是一个I2C模拟器, 支持模拟主机和从机。然后还需要一个上位机, 上位机上可以配置I2C从机的寄存器值, 包括故障的类型和发生的位置也要可以修改。I2C模拟器这个我看淘宝上已经有了, 就是USB转I2C模拟器。那我这里就是需要增加一个故障模拟功能。
