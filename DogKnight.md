# 升级URP渲染

Window菜单  ->  包管理器  ->  搜索Universal RP

![image-20230419205537298](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230419205537298.png)

在 Project 窗口中单击右键，然后选择 **Create > Rendering > URP Asset**

![image-20230419211259873](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230419211259873.png)



edit -> 项目设置  ->  Graphics（图形）

![image-20230419211427039](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230419211427039.png)

None那里放入刚刚创建的Render

接下来前往Quality  那里的None也选择Render



## 项目升级渲染管线（2020及以下）

edit  ->  Render Pipeline  ->  Universal Render Pipline  ->  项目升级URP

## 项目升级渲染管线（2021）

[Unity 2021.2升级URP材质记录 - 哔哩哔哩 (bilibili.com)](https://www.bilibili.com/read/cv14043269/)

# 添加素材

天空盒子：3D  可以切换  就是天空  

切换方法：Window Rendering lighting environment 更换skyBox

影子相关：渲染管线设置  shadows  例如Max Distance    Cascade Count渲染级数，在范围内实际渲染，范围外虚渲染

ReSoulution：渲染的性能

抗锯齿

soft shadows

## 光照设置

还是找到lighting ->  New Lighting Settings

改变光的类型（一般为baked indirect）  然后渲染一般使用GPU  然后右下角生成渲染
![image-20230420123403340](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420123403340.png)

此时地面变成skyBox颜色，因为environment中光源就是skyBox，可以改为color为原本颜色



###  素材放置

**自动吸附： 按住v键，鼠标拖动**

**改变摄像机位置，ctrl shift f（改变繁体，取消即可）**

## 3D场景搭建

包管理器   poly brush   导入URP样例

工具打开poly brush 选中地图可以改变场景

![image-20230420130341587](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420130341587.png)

第一个调整地图

![image-20230420130415694](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420130415694.png)

可以通过设置改变xyz轴或者vertex normal

第二个调整羽化，消除突出的点使用

第三个改变颜色

但是需要先为素材导入材质   

![image-20230420130630164](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420130630164.png)

在刚才导入的样例中点击creat 创建材质

![image-20230420130715821](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420130715821.png)

然后上色  其中flood是改变所有颜色

第四个复制预制体

![image-20230420131120111](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420131120111.png)

将预制体拖放到current palette中，然后选择要的，就可以随机放上预制体

如果不需要，则按下ctrl然后点按就可以删除  但是注意别按ctrl+z



## 场景变大

probuilder插件

![image-20230420131916387](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20230420131916387.png)

shift按下可以显示功能