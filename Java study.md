03-01-2016
---------------------
* 序列化
     保存在内存中的各种对象的状态（也就是实例变量，不是方法），并且可以把保存的对象状态再读出来。

* 什么情况下需要序列化
  * 当你想把的内存中的对象状态保存到一个文件中或者数据库中时候
  * 当你想用套接字在网络上传送对象的时候
  * 当你想通过RMI传输对象的时候

```
        try{  
            FileOutputStream fs = new FileOutputStream("foo.ser");  
            ObjectOutputStream os =  new ObjectOutputStream(fs);  
            os.writeObject(myBox);  
            os.close();  
        }catch(Exception ex){  
            ex.printStackTrace();  
        }  
```
