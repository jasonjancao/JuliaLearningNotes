# 安装
 学习的第一步当然是下载安装程序环境了，直接到Julia官网<https://julialang.org/>下载即可。这个安装仅带一个交互环境REPL(所谓Read-Eval-Print Loop)的控制台。
脚本可以直接用其他IDE甚至notebook生成，然后在这个控制台上运行。最便捷的直接下载JuliaPro（类似Anaconda之于Python)这个软件，目前也是免费的，不过需要注册一下或使用Github帐号登录，
不管你用什么安装，你最终会在控制台程序看到如下画面:
![JuliaStart](https://github.com/jasonjancao/JuliaLearningNotes/blob/master/NotesBook/fig/JuliaStart.png)
注意到界面中有一个：Julia> 提示符，这就是我们控制台输入的入口处。
# 运行第一个程序
 安装好了以后，试运行一下经典的程序：在Julia>提示符下输入：print("Hello,world!\n")或者println("Hello,World!")然后按回车键，不出意外的话就会得到计算机的回应（hello world 的程序是从C开始的，几乎每一个程序员练习编程软件久负盛名的传统）。
 ![helloworld](https://github.com/jasonjancao/JuliaLearningNotes/blob/master/NotesBook/fig/HelloWorld.png)
 
 需要说明的是`println()`是`print()`函数的自带换行符的版本，所以在"print"后面加字母"l+n",不是数字"1+n"。
# 控制台的其他4种工作模式
 - 帮助模式(help?>):在julia>提示符下输入"?"（注意英文问号,不是中文的问号）就进入了帮助模式，继续输入"println"回车，就会看到`println()`的帮助文件，并自动回到julia模式。
```julia
help?> println
search: println printstyled print sprint isprint

  println([io::IO], xs...)

  Print (using print) xs followed by a newline. If io is not supplied, prints to stdout.

  Examples
  ≡≡≡≡≡≡≡≡≡≡

  julia> println("Hello, world")
  Hello, world
```

- pkg>模式：在julia模式下，输出右中括号"]",就会进入程序包的管理模式，在此模式下可以进行各种程序包的安装、移除、更新、固定等工作。退出pkg模式只需在`*pkg>`提示符下按退格键即可，也可以同时按"ctrl"和"c"键(为方便输入，以后把同时按键写成如"ctrl"+"c"的形式)退出pkg模式。包管理模式以后还会详述。

- shell模式，在 julia>提示符输入英文分号`;`，就会进入到 shell 模式。这种模式下可以执行普通的 Shell 命令。当我们需要时不时地操纵文件系统时，这样会很方便，省去了我们在多个命令行之间切换的工作量。与帮助模式类似，在执行完一个 shell 命令之后，REPL 环境会自动地退出 shell 模式并切换回 julia 模式。

- 与MALAB命令窗口类似，REPL 会记录输入过的语句表达式与当时的状态。只需在julia>提示符下按向上(Up)或向下(Down)方向键，可连续按下，当需要的语句出现后，按下回车，便可重新执行该语名。也可按"ctrl"+"r"复合键打开历史搜索模式，以进行相关语句的搜索。
