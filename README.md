## 本分支默认集成Openwrot LUCI Web界面，默认设置适用于中文用户!
### 默认开启WiFi，务必按需修改系统设置!!!

定制界面语言（不需修改任何源码文件)  以NETGEAR WNDR4300 V1为例：  
#### 一：Gargoyle默认设置，英文界面，需在插件管理里面安装语言包插件
        make FULL_BUILD=true ar71xx.usb_large_nand  
#### 二：（推荐）默认界面使用中文，但包含英文界面，可以切换，可以安装其他语言
        make FULL_BUILD=true ar71xx.usb_large_nand TRANSLATION=internationalize ACTIVE_LANG=SimplifiedChinese-ZH-CN  
#### 三：（小Flash使用）指定使用中文界面，不能更换其他语言
        make FULL_BUILD=true ar71xx.usb_large_nand TRANSLATION=localize FALLBACK_LANG=English-EN ACTIVE_LANG=SimplifiedChinese-ZH-CN  

#### 编译x86_x64固件：
    make FULL_BUILD=true x86.x64 TRANSLATION=internationalize ACTIVE_LANG=SimplifiedChinese-ZH-CN





## License

Gargoyle is copyright (C) 2008-2019 by Eric Bishop
Gargoyle is free software; you can redistribute it and/or modify it under the terms of the [GNU General Public License version 2.0](http://www.gnu.org/licenses/gpl-2.0.html) as published by the Free Software Foundation, with the following clarificaiton/exception that permits adpating the program to configure proprietary "back end" software provided that all modifications to the web interface portion remain covered by this license:

> The GNU General Public License (GPL) is vague as to what constitutes “mere aggregation” under section 2, and what contitutes a work “based on the Program.” In the special case in which the Program is modified for the purpose of configuring other (potentially GPL-incompatible) software, the combination of the Program and this other software shall be considered "mere aggregation" if and only if the ONLY interaction between the Program and the other software being configured takes place via CGI (Common Gateway Interface) scripts and/or programs. However, these CGI scripts/programs as well as any other additions and modifications necessary for the configuration of the other software shall be considered “based on the Program” for the purposes of this license. Further, if any portion of the Program is used as part of an interface that can be rendered via a web browser, all portions of that interface that can be rendered via a web browser (including, but not limited to, javascript, svg/ecmascript, css, html, and shell/perl/php/other cgi scripts) shall be considered “based on the Program.”
> This clarification/exception shall apply to the license of all derived works, and must appear in all relevant documentation. If you choose to release your modification to the Program under a later version of the GPL that directly contridicts this clarification/exception, this clarification/exception shall supersede any contradictory language in that version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

## Acknowledgments

* Eric Bishop - Project founder and lead developer
* The community - For using, supporting and contributing to Gargoyle
