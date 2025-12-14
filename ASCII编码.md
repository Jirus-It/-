##  ASCII编码

使用我们的Detect it Easy 检查文件是否有壳

经过我们的检查发现没有壳

再使用我们的ida逆向工具打开工具，由于代码比较杂乱，我们直接使用shift+F12查找所有字符

观察一下是否有flag的相关信息

发现{hello world}很像flag提交发现并不是

我们再用鼠标选中“this is the right flag!\n”  ctrl+X 交叉使用，查看了是那段函数引用了该字符串

再使用F5进入伪代码查看

我们先找到this is the right flag!\n 发现sub_1400111D1应该是类似于print的函数输出

发现str2是之前发现的{hello world}

应该是str1，这里‘

 if ( Str2[j] == '111' )
      Str2[j] = 48;

和明显对str的内容进行了替换

再ida里我们可以用鼠标选中按R进行ASCII解码

解码发现把"o"替换成了"0"

答案便迎刃而解







