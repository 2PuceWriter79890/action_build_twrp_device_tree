##### 此仓库复刻于 [momo54181](https://github.com/momo54181/action_build_twrp_device_tree)
 # TWRP Device Tree生成工具
-----
<details>
<summary>使用方法</summary>

*  1.将此仓库 Fork 到你自己下（不建议设为私有）

*  2.上传你需要编译设备的 recovery.img 到仓库里
 
*  3.通过 View raw 来获取你上传 recovery.img 的链接
 
*  4.点击actions － Make twrp device － Run workflow ，然后在 IMG_URL 里面输入你刚刚获取的链接

*  5.填写完成后点击 Run workflow 开始生成

</details>

-----

## 编译结果
- 可以在 [Release](../../releases) 下载

## 看不懂想要图文教程?
- 看看隔壁那个用github编译twrp教程，与这个大同小异端
- https://github.com/momo54181/Action-Recovery-builder#readme

注意：
1.如果安卓版本低于9.0，需要手动解包recovery.img并在defxx.prop内添加
ro.product.first_api_level=23 #安卓api版本号，如安卓6.0是23
2.如果你的设备是oppo，且出现了AssertionError: Property ro.product.system.device could not be found in build.prop
需要将ramdisk里面的etc/recovery.fstab复制到system/etc/recovery.fstab
system/build.prop和vendor/build.prop的内容一起合并到/prop.default然后打包生成
