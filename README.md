# ADBCommand

1. 查看所有已安装的app的包名

    adb shell pm list package -3
	
2. 根据包名卸载已安装的app
	
    adb uninstall *package_name*
	
3. 进入到手机的shell

    adb shell

4. 退出手机的shell(在手机的shell中输入）

    exit
    
5. 列出所有Activity信息

    adb shell dumpsys activity
    
6. 上面输出的信息比较多，过滤出栈顶的Activity

    adb shell dumpsys activity | grep "mFocusedActivity"
    
7. 进入root权限的shell

    adb root shell
    
8. 取出对应的包名的app的安装包.包名需要在手机的`data/app/`目录下查看

    adb pull /data/app/*package_name*/base.apk
    
9. 对手机进行截图并保持到SD卡中

    adb shell /system/bin/screencap -p /sdcard/screenshot.png



