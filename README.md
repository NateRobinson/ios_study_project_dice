# ios_study_project_dice

通过这个项目学到

1. 在做本地项目和 github 仓库关联的时候，如果在创建 github 仓库的时候，不是一个完全空的仓库，这个时候如果要把本地的仓库 pull 上去会报 `refusing to merge unrelated histories` , [解决方案](https://blog.csdn.net/u012145252/article/details/80628451)

2. 可以通过 `touch .gitignore` 和 `open .gitignore` 方式添加并编辑 ignore 规则，借助 [https://www.gitignore.io](https://www.gitignore.io) 这个网站可以自动帮我们生成 ignore 文件规则，非常的方便

3. 如果不是在 xcode 中创建的文件，无法直接在 xcode project navigator 中看到，需要通过右击鼠标，在弹出的菜单中选择 `Add Files to (Dice)` ,使得文件夹下创建的文件可以直接在 xcode 中查看

4. storyboard 和页面做关联的时候，修改关联的话必须去 storyboard 对应的元素上修改之前的 reference，不然运行会报错

5. iphone 的感应检测器使用，超级简单，只要在 viewcontroller 中 override 一个系统自己的方法，在里面实现自己的业务逻辑就可以

    ```swift
    override func motionEnded(_ motion: UIEvent.EventSubtype, with event: UIEvent?) {
    updateDiceImages()
    }
   ```
