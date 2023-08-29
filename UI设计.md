UI设计

 创建：在菜单中右键创建UI ![image-20221025211031484](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221025211031484.png)

所有UI都需要canvas（画布）来放置。

画布然后再上面建立文本按钮或其他东西。

然后编代码，你要使用canvas里text这个类，需要在前面加上using unityengine.ui 才能public text xxx；![image-20221025212720053](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221025212720053.png)

然后是设计UI里的内容，要让他改变，也就是要让numbers为cherry的值

![image-20221025213528455](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221025213528455.png)

注意这个CherryNumber.text = Cherry.ToString（）； 将cherry这个int类型转为string类型

![image-20221025214647529](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221025214647529.png)

接下来的问题是这个UI的显示会随着游戏的比例而改变位置，导致看不到

那么可以锁定它在左上角

![image-20221025214850490](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221025214850490.png)

在text中的rect transform里改变.