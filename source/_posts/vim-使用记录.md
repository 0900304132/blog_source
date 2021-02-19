---
title: vim 使用记录
date: 2021-02-18 15:14:56
tags: [vim]
category: [开发环境]
---

1. ## Caps 映射成 Esc

   [Vim 技巧——将 CapsLock 键映射成 Esc 键](https://kang000feng.github.io/blog/2015/02/04/remap-capslock-key/)  
   Windows 下将 CasLock 转换成 Esc

   ***

   将下面的代码保存为 capslock2esc.reg:

   ```dll
   Windows Registry Editor Version 5.00

   [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout]
   "Scancode Map"=hex:00,00,00,00,00,00,00,00,02,00,00,00,01,00,3a,00,00,00,00,00
   ```

   双击写入注册表

2. ## vscode 安装 Vim

   ### 退出编辑模式的时候输入法自动选择成英文

   1.安装[im-select](https://github.com/daipeihust/im-select#installation)  
    2.vim 中 setting.json 插入

   ```json
   "vim.autoSwitchInputMethod.enable": true,
   "vim.autoSwitchInputMethod.defaultIM": "1033",
   "vim.autoSwitchInputMethod.obtainIMCmd": "D:\\im-select\\im-select.exe",
   "vim.autoSwitchInputMethod.switchIMCmd": "D:\\im-select\\im-select.exe {im}",
   ```

3. ## chrome 安装 surfingKey
