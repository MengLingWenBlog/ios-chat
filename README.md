## 说明
本系统有4部分组成，服务器/iOS客户端/Android客户端/协议栈库。其中iso和android都依赖于协议栈库。本工程为iOS客户端


### 编译

下载之后要先编译一遍协议栈，编译方法参考协议栈文档。然后打开ios-chat.xcworkspace工程，对每个项目进行编译。

### 工程说明

工程中有3个项目，1个应用和2个库。chatclient库是IM的通讯能力，是最底层的库，chatuikit是IM的UI控件库，依赖于chatclient。chat是IM的demo，依赖于这两个库，chat需要正确配置服务器地址。

### 配置

在项目的Config.m文件中，修改IM服务器地址配置。把```IM_SERVER_HOST```和```IM_SERVER_PORT```设置成火信的地址和端口。另外需要搭配应用服务器，请按照说明部署好[应用服务器](https://github.com/wildfirechat/app_server)，然后把```APP_SERVER_HOST```和```APP_SERVER_PORT```设置为应用服务器的地址和端口。

### 登陆
使用手机号码及验证码登陆，
> 在没有短信供应商时，可以使用[superCode](https://github.com/wildfirechat/app_server#短信资源)进行测试验证。