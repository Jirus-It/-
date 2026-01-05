#  API及获取工具使用方法

简单来说api就是不同软件之间沟通的桥梁。

有些api是在前端js写死的，有Swagger/Openapi文档，

固定命名路径，浏览网络请求，

移动端小程序接口，历史遗留接口（未下线）

* 使用专业api枚举工具（自动化），可以做到提取api隐藏路径，隐藏接口，调试接口
  * 输入代码  git clone https://github.com/GerbenJavado/LinkFinder.git有工具的直接执行下面的代码
    * python3 linkfinder.py -i https://域名/找到带有status == 200并且粘贴当前文件的文件路径 -o cli
      * 为了防止kali linux 禁止pip的安装，我们创建一个虚拟机环境python3 -m venv venv
        * 激活虚拟环境 source venv/bin/activate
          * 安装依赖pip install -r requirements.txt
            * 运行LinkFinder 		（请强制养成安全人员使用Venv/pipx的习惯）
            * LinkFinder只能分析真实存在的js内容
            * 有时候js可能在二级动态路径，使用浏览器F12开发者工具找到带有status == 200并且复制当前文件的文件路径

* api的获取

  * 使用burp suite (kali linux自带)

    * 在Proxy > HTTP histroy里看接口

      * 真实业务api一定会走网络

        

        

        

         

        