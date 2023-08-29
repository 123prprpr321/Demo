# unity知识

+ 对于ontriggerenter 2d来说，需要知道触发条件。

1. 两个物体都必须有碰撞器（Collider）组件

2. 其中一个物体的碰撞器（Collider）的IsTrigger属性必须勾上
3. 最重要的一点，其中一个物体必须有刚体（Rigidbody）组件

因为这个第三点，导致出过bug...，所以知道这个条件很有必要。

+ #### 父类设置方法（父子类设置方法以及脱离父子类关系）

  ```c#
  playerTransform = GameObject.FindGameObjectWithTag("Player").transform.parent;
  
   other.gameObject.transform.parent = gameObject.transform;
  
   other.gameObject.transform.parent = playerTransform;
  ```

  transform.parent表示变换的父类，可以通过此将其归属于另一个物体变成子类

+ ### 子类解除方法

1. 第一种就是直接像上面一样，原本没有父子类关系，那么先留存一份，之后换回
2. 第二种

```c#
this.transform.DetachChildren();
```



### BOSS制作

+ 用的简单的switch语句 和 动画帧事件 和play实现简单boss
+ 其中每个技能都设置冷却时间 
+ 关键在于搞清楚触发条件，然后切换动画即可
+ **用好动画关键帧事件很重要！！！**
+ 为物体添加重力，然和通过random函数来给定初始值，这样就可以做到随机从天上掉落物品。

之后生成火柱，可以如果碰到了ground图层，那么，生成预制体，播放动画，产生伤害。

产生其他东西也是一样

##### 死亡后不再移动

添加rigibody 2d

rb = new v2（0,0） 这样即可

# unity 修改transform.rotation的两种方法

transform.localPosition和transform.localScale都是直接赋值三元数，给旋转赋值需要用 
　　方法一： 
　　xxx.transform.localEulerAngles = new Vector3 (0.0f,0.0f,0.0f); 
　　方法二： 
　　 xxx.transform.rotation=Quaternion.Euler(0.0f,0.0f,0.0f);
