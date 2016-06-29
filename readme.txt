这个项目是编译出一个工具，这个工具是给JVM用的，JVM使用这个工具，把运行时用到的类，都存为class文件，包括动态生成的类。
只需要在src/main/resources/META-INF/MANIFEST.MF中设定好内容：
Manifest-Version: 1.0
Premain-Class: com.woslx.CustomAgent
exportClazzToFile("/home/hy/exportclass/", fileName, classfileBuffer);这里要设置输出类的路径，文件夹要全部预先建立好。
然后在命令行运行java文件的时候，要在classpath根路径上，如果class是带报名的，那么要写满包路径。