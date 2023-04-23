                                  Londly 


由于其他不可抗力原因，该项目源码不提供

一款红队在大量的资产中实现子域名收集、指纹识别、漏扫的二开工具

收集的子域名可以是目标单位的域名+控股公司域名+分支机构域名 推荐enscan收集子域名，后期会公布自己写的项目收集子域名

## 0x00 项目概述

 将原理简单概述一下,oneforall和ksubdomain双子域名收集，收集后自动去重，去重后的子域名进行Finger+observer双重指纹识别，xray+nuclei漏扫。

## 0x01 使用方法

 请在Linux环境下使用该工具，将xray nuclei Finger observer oneforall ksubdomain放到根目录下，实现自动化，使用xray高级版效果更佳，xray需要配置反连平台
 
 执行：python3 londly.py -d xxx.com  注意下载的工具文件命名要和脚本的文件命名相同

执行完上面命令，等着收成果即可，建议使用VPS

 

## 0x02 调用的项目地址
 
 observer地址
 https://github.com/0x727/ObserverWard
 
 Finger地址
 https://github.com/EASY233/Finger
 
 nuclei地址
 https://github.com/projectdiscovery/nuclei
 
 xray地址
 https://github.com/chaitin/xray
 
 ksubdomain地址
 https://github.com/knownsec/ksubdomain
 
 OneForAll地址
 https://github.com/shmilylty/OneForAll
 
## 0x03 使用注意事项
 1.将oneforall所有API配置上后在和ksub结合收集的子域名大概率最全，为什么是大概率，因为oneforall导出来结果是80和443端口，像http://xxxx.com:8080是没有的，所以需要将
   oneforall里的ip提取出来，然后用我的另一个项目，进行全端口扫描发现8080资产。
 
 2.调用的项目改为xray_linux_amd64 nuclei ksubdomain OneForAll Finger 否则运行时报错
 
 3.部分用户反映调用的时候没有d.txt文件，原因为：网络差或者换个子域名(可能ksub没有爆破出子域名,所以没有生成d.txt结果)。
 
 4.下载的脚本里带result/onedomain文件夹。因为所有文件保存在根目录感觉太乱了。
 
 5.项目整体文件如下：
 ![图片](https://user-images.githubusercontent.com/118274389/216054336-920f50dd-4211-4cd1-8f40-2f05fec2d82f.png)


## 0x04 免责声明

 该项目仅供授权下使用，禁止使用该项目进行违法操作，否则自行承担后果，请各位遵守《中华人民共和国网络安全法》！
