# 主菜单MainMenu

+ 菜单其实是一个场景，所以创建一个场景，然后添加UI里的东西
+ 创建UI里的panel 对于这个panel 需要修改原图像为无 这样才能填满摄像机![image-20221029183641264](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221029183641264.png)

+ **创建按钮渐变效果**

需要再创建一个panel 然后改颜色

+ 在menu下面创建一个button(有text的那个)
+ ![image-20221030003315174](C:\Users\Pluto\AppData\Roaming\Typora\typora-user-images\image-20221030003315174.png)

这里有一个问题，不知道为什么加上background后按下变色就不出来了

+ 代码实现 跳转

+ ```c
  using UnityEngine.SceneManagement;
  public class Menu : MonoBehaviour
  {
      public void PlayGame()
      {
          SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex + 1);
      }
      public void QuitGame()
      {
          Application.Quit();
      }
  }
  
  ```

  这里还有渐变效果，其实就是录制，记得loop关掉就行

  