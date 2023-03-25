# 设置 ARM 实验环境

本节介绍如何使用 Qemu 和 GNU 工具链在 PC 中设置一个简单的 ARM 开发和测试环境。Qemu 是一个机器仿真器，能够模拟各种机器，包括基于 ARM 的机器。你可以编写 ARM 汇编程序，使用 GNU 工具链编译它们，并在 Qemu 中执行和测试它们。

## Qemu ARM

Qemu 将用于模拟 Gumstix 基于 PXA255 的 connex 板。您应该至少具有 Qemu 的 0.9.1 版本才能使用本教程。

PXA255 具有一个 ARM 内核和符合 ARMv5TE 标准的指令集。PXA255 还具有多个片上外设。在本教程的过程中将介绍一些外围设备。

## Installing Qemu in Debian

本教程需要 qemu 0.9.1 或更高版本。Debian Squeeze/Wheezy 中提供的 qemu 软件包满足了这一要求。使用 apt-get 安装 qemu。

`apt-get install qemu`

## 安装用于 ARM 的 GNU 工具链

CodeSourcery（Mentor Graphics 的一部分）已经制作好 GNU 工具链可用于各种架构。可以从这里下载 ARM 的 GNU 工具链，
http://www.mentor.com/embedded-software/sourcery-tools/sourcery-codebench/editions/lite-edition/

解压 tar 文件到 `~/toolchains`

```bash
$ mkdir ~/toolchains
$ cd ~/toolchains
$ tar -jxf ~/downloads/arm-2008q1-126-arm-none-eabi-i686-pc-linux-gnu.tar.bz2
```

添加工具链路径

`$ PATH=$HOME/toolchains/arm-2008q1/bin:$PATH`

您也可以将上一行添加到 .bashrc 中。
