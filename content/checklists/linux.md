---
title: "Linux checklist"
date: 2023-03-03T22:48:35+03:00
---

- **Your system has a Host Security ID (HSI) level 3 or higher**

  Having a secure system is vital. Having a HSI 3 and higher means that your
  device adheres to all of the modern security standards and supports the latest
  protection features.

  If you use GNOME, you can check your HSI level by going to Settings -> Privacy
  -> Device Security. Otherwise, it can be checked by running
  `fwupdmgr security`.

- **You use systemd as your init system**

  Despite being a
  [pointlessly](https://0pointer.de/blog/projects/the-biggest-myths.html)
  controversial piece of software, systemd brings many improvements to the core
  of the Linux system. It significantly streamlines and improves the security of
  many areas of system administration, such as service management, network
  management, encryption, system logs and much more.

- **You use Wayland**

  X11 is an obsolete protocol which is not suitable for modern day. It is slow,
  heavy, insecure and laggy. It also does many things behind the scenes in a
  really weird way. While the X.Org server recieves small security patches from
  time to time, the X11 protocol is not being updated for modern use cases.

  Wayland is a modern display protocol which is a replacement for X11. A few
  edge cases aside, it works flawlessly for most people and doesn't have any
  major issues. Wayland is what X was supposed to be. You can check the
  theoretical [plans for X12](https://www.x.org/wiki/Development/X12/). It
  basically describes Wayland.

- **You use Pipewire**

  PulseAudio is the old audio server for Linux. It misses many crucial security
  features, such as audio isolation. It doesn't have great hardware
  compatibility, _especially_ with Bluetooth hardware. It's also hard to
  configure and has a high latency, which means that audio producers have to use
  JACK, a separate audio engine.

  Pipewire is a modern drop-in replacement for PulseAudio which is more secure,
  robust and extensible. It also has compatibility with PulseAudio and JACK
  applications.

- **You use a modern kernel**

  Using the latest kernel is important for having all of the new performance and
  security patches. Do not use an LTS kernel on desktop systems, they are only
  suitable for servers where frequent updates are not possible or dangerous.

  DO NOT use linux-libre. It prioritises ideology over security,
  [removing important security mitigations](https://www.phoronix.com/scan.php?page=news_item&px=GNU-Linux-Libre-5.7-Released)
  and [disabling kernel warnings](https://news.ycombinator.com/item?id=29674846)
  about possible vulnerabilities.

- **You encrypt your storage with LUKS**

  Encrypting your storage means that even if your device gets stolen, your data
  remains secure. On modern platforms like Android, macOS or iOS, the storage is
  encrypted by default. Most Linux distros allow you to enable drive encryption
  during installation.

- **You use a modern filesystem**

  ext4, the most widely used Linux filesystem, generally works fine, so this is
  not a critical step. However, modern replacements such as btrfs provide many
  additional features, including better performance, snapshots, subvolumes,
  deduplication and much more.
