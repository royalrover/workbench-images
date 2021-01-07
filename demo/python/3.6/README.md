## 系统文件

- .workbench
  - 不可删除，云开发平台应用部署配置文件
  - fcRouteDefault，「路由/函数入口」配置入口,默认为“/*”,无需特殊配置

- requirements.txt
  - 配置项目依赖文件（如果有）
  - 如果项目有依赖，则需要打开 CloudIDE 的「终端」输入以下命令进行安装，否则可以忽略此文件和下面的安装步骤
  ```
  sudo pip install -r requirements.txt --target ./
  ```
  
- prepare.sh
  - 为阿里云云开发平台构建用户自定义镜像的前置操作，处理环境变量以及启动命令等操作 
  - 该脚本会生成dockerfile入口文件 “start.sh”，开发者需要在prepare.sh的指定位置添加服务启动命令

- Dockerfile
  - 根据提供的Dockerfile模板进行定制
  - **云开发平台默认只提供容器8080端口的映射**
  
## 开发测试
- 接下来可以正常开发你的 Python 应用了，可以打开云开发平台Cloud IDE在线开发调试应用
- 确保应用镜像可运行后，通过Cloud IDE的左上角插件点击部署

## 部署
- 测试确定应用如预期工作，没有问题后，点击「WB」插件，打开「部署」面板，选择「日常环境」，点击「部署」，等待部署完成即可
