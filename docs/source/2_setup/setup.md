# 装机必备工具



## Github

每次`git push`都需要输入账号密码？不妨使用下面的方法:

下面命令会将下次弹框的账号和密码保存起来，永久使用。

``` git
git config --global credential.helper store
```

如果想要清除该账号和密码，使用如下命令：

```
git config --global credential.helper reset
```

想要临时存储（默认15min），使用如下命令

``` git
git config --global credential.helper cache
```

windows下的临时存储命令不是上面的，应该使用下面的命令:  

``` git
git config --global credential.helper wincred
```

## Visio

### Visio 16

以管理员的身份：

```
cd "C:\Program Files (x86)\Microsoft Office\Office16"
cscript ospp.vbs /inpkey:PD3PC-RHNGV-FXJ29-8JK7D-RJRJK
cscript ospp.vbs /sethst:kms.03k.org
cscript ospp.vbs /act
```

### Vision 19

1.打开记事本。

2.复制下面代码到记事本，保存为*.bat格式，名称随意。

```
@echo off
title Activate Microsoft Visio 2019&cls&echo ============================================================================&echo #Visio: Activating Microsoft software products for FREE without software&echo ============================================================================&echo.&echo #Supported products:&echo - Microsoft Visio Standard 2019&echo - Microsoft Visio Professional Plus 2019&echo.&echo.&(if exist "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles%\Microsoft Office\Office16")&(if exist "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles(x86)%\Microsoft Office\Office16")&cscript //nologo ospp.vbs /inslic:"..\root\Licenses16\pkeyconfig-office.xrm-ms" >nul&(for /f %%x in ('dir /b ..\root\Licenses16\client-issuance*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&(for /f %%x in ('dir /b ..\root\Licenses16\visioprovl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&(for /f %%x in ('dir /b ..\root\Licenses16\visiopro2019vl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&echo.&echo ============================================================================&echo 正在尝试激活...&cscript //nologo ospp.vbs /unpkey:7VCBB >nul&cscript //nologo ospp.vbs /inpkey:9BGNQ-K37YR-RQHF2-38RQ3-7VCBB >nul&set i=1
:server
if %i%==1 set KMS_Sev=kms8.MSGuides.com
if %i%==2 set KMS_Sev=kms9.MSGuides.com
if %i%==3 set KMS_Sev=kms7.MSGuides.com
if %i%==4 goto notsupported
cscript //nologo ospp.vbs /sethst:%KMS_Sev% >nul&echo ============================================================================&echo.&echo.
cscript //nologo ospp.vbs /act | find /i "successful" && (echo 已完成，按任意键退出) || (echo 连接KMS服务器失败! 试图连接到另一个… & echo 请等待... & echo. & echo. & set /a i+=1 & goto server)
pause >nul
exit
```

3.右键使用管理员权限身份打开。

4.等待一会，激活成功。



## SSR

ssr-cloud

## 写作

+ typora



## 编程

+ vscode

  1. remote development
  2. 
+ VS
+ git bash
+ navicat premium
+ notepad
+ Google Chrome
  1. AdBlock
  2. CF-predictor
  3. Coplay(视频播放同步)
  4. crxMouse Chrome
  5. gitZip for github
  6. Imagus(图放大)
  7. LastPass
  8. Octotree
  9. tampermonkey
  10. zotero connector
  11. 书签侧边栏
  12. 广告终结者
  13. 有道词典



## 其他

+ xmind zen
+ zotero
+ 坚果云
+ MPC-HC x64 播放器
+ VM Station
+ OBS
+ QQ
+ 微信
+ Steam
+ UltraEdit
+ Texstudio
+ ubuntu WSL
+ 7zip
+ docker desktop
+ screen to gif
+ picgo
+ U盘启动盘制作工具：rufus
+ 

