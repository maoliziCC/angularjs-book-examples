以上例子详见：
深究AngularJS——自定义服务详解(factory、service、provider)
https://blog.csdn.net/zcl_love_wx/article/details/51404390



例子在"2"文件夹中
AngularJs基础——自定义服务的三种方法以及provider供应商  
https://blog.csdn.net/bboyjoe/article/details/50456869

Provider、Factory、Service三者之间的区别是：
Provider是唯一一种可以传进.config()函数的service.当你想要在service对象启用之前，先进行模块范围的配置，那就应该用provider。

Factory是直接把一个函数当成一个对象的$get方法，可以直接返回字符串。用factory就是创建一个对象，为它添加属性，然后把这个对象返回出来。你把service传进controller之后，在controller里这个对象里的属性就可以通过factory使用了。

Service是用"new"关键字实例化的。因此，你应该给"this"添加属性，然后service返回"this"。你把service传进controller之后，在controller里"this"上的属性就可以通过service来使用了。
