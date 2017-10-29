# gargoyle
Gargoyle Router Management Utility  
This is a fork program for custom build,read Wiki for more details  
The origin web site is http://www.gargoyle-router.com/  
## This fork aim for Chines user,and build-in completely LUCI support!
### Pre-set wireless on and open!!!

石像鬼定制界面语言（不修改任何源码文件)  
共3中情况：  
1、使用默认的英文界面，需要语言在插件管理里面安装  
2、设定默认中文界面，但包含英文界面，可以切换，可以安装其他语言  
3、指定使用中文界面，不能更换其他语言  
以NETGEAR WNDR4300 V1为例：  

情况一：make FULL_BUILD=true ar71xx.usb_large_nand  
情况二：make FULL_BUILD=true ar71xx.usb_large_nand TRANSLATION=internationalize ACTIVE_LANG=SimplifiedChinese-ZH-CN  
情况三：make FULL_BUILD=true ar71xx.usb_large_nand TRANSLATION=localize FALLBACK_LANG=English-EN ACTIVE_LANG=SimplifiedChinese-ZH-CN  