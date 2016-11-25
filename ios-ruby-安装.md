#ruby
 - mac 本身自带ruby
 - ruby官网的地址是:http://www.ruby-lang.org/zh_cn/
 - 查看ruby -v(查看ruby版本)
 - 通过rvm来安装ruby
 - rvm的官网：http://rvm.io/
 - rvm 安装：
  -  gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
  - \curl -sSL https://get.rvm.io | bash -s stable
 - 其中curl是下载curl是利用URL语法在命令行方式下工作的开源文件传输工具，可以详细查询curl教程（mac 自带curl）
 - gpg：GPG是加密和数字签名的免费工具，大多用于加密信息的传递。除了仅用密码加密外，GPG最大的不同是提供了“公钥/私钥”对。利用一方的“公钥”别人加密信息不再需要告诉密码，随时随地都能发送加密信息。而这种加密是单向的，只有一方的“私钥”能解开加密。数字签名又是另一大使用方向。通过签名认证，别人能确保发布的消息来自一方，而且没有经过修改。
 - mac 下软件管理推荐 homebrew：http://brew.sh/
#sas安装流程   
 - $brew install gpg
 - $--keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
 - $\curl -sSL https://get.rvm.io | bash -s stable
 - rvm就安装到mac上来
 - rvm install 2.3.1 便可安装ruby2.3.1
 - rvm list 可查看电脑的ruby列表
 - gem install sass 安装sass

#compass
 - compass是在sass基础上二次开发的一个框架
 - 安装：gem install compass

 

