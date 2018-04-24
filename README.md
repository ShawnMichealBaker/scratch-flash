# 1. 准备工作和下载资源
1. 下载并安装 JDK Gradle
2. 克隆项目 注意是jfeng分支

3. 搭建一个本地服务器 在服务器根目录下简历flex目录
4. 下载 apache-flex-sdk-4.15.0-bin.zip swfobject_2_2.zip OSMF_1.0.zip 放到flex目录
5. 修改apache-flex-sdk中的frameworks/downloads.xml内容，将swfobject和osmf的下载地址改为本地的地址
http://127.0.0.1/flex/swfobject_2_2.zip
http://127.0.0.1/flex/OSMF_1.0.zip
修改好了再压缩成zip（或者直接在压缩包里改）

6. 全都准备好了之后 在终端打开当前项目的路径 运行 ./gradlew build -Ptarget=11.6 进行构建

# 2. 在浏览器中运行

1. 将打包出来的swf文件放到服务器根目录
2. 在服务器根目录下新建index.html文件 里面引用这个swf即可

3. 注意 swf如果要发送请求 需要在服务器中打开index页面(本地以文件形式打开不会发送请求)

4. 还要注意 服务器中还需要 local medialibraries medialibrarythumbnails 等文件来提供swf请求的资源（在scratch-mine仓库中有）

[详细参考](http://www.ieclipse.cn/2016/08/18/other/scratch-compile/)
