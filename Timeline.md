Window界面找到顺序->时间轴（Timeline）



在场景空物体Tiemline，保存文件，别乱保存在某个地方，方便找到



==timeline轨道==

●ActivationTrack：选择控制在Timeline上何时激活轨道
●AnimationTrack(动画轨道):允许直接导入动画片段、或者直接再Timeline中重建动画
●AudioTrack(声音轨道):首先，这个轨道无法再Play模式外预览声音，允许导入现有音频资源片段、做出编辑
●ControlTrack：可以控制事件相关的游戏对象中的元素，比如例子系统、PlayableDirector组件
●PlayableTrack：允许触发其他Timeline Sequences时间序列
●SignalTrack：将Timeline和外部系统建立通信通道
●CinemachineTrack:允许再Timeline内控制Cinemachine虚拟相机
●DialogueTrack：自定义的对话轨道(自己编写代码添加轨道)



常用轨道 Activation Track，Animation Track 

添加密匙	Add Key，两个不同位置的密匙产生位移



关键帧录制，与动画类似，但是有些区别，并且无法在timeline外编辑具体动画，通常还需要director（导演）





**在选择Timeline物体时，在选择拖动其他物体时不小心点到timeline界面会变成选择物体的界面（没有创建）,所以在对Timeline操作时可以点击Timeline右上角🔒状态，锁定界面;**



一般不需要开始就播放，timeline很适合用来做开场动画，过场动画



**timeline动画可以叠加播放**