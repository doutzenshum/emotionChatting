#使用
这里可以随便起名字，但是密码统一为在Servlet中设置的密码，这样才能出现聊天中的名字，才有意思嘛
需要说明的是，目前没有登录用户无法发送消息，需要登录后才能发送
#聊天内容总体存储方式
1、List<String> OnLineUserList = new ArrayList<String>(); //存储用户的arrayList
2、static List<String> strSendConentList=new ArrayList<String>();//存储聊天内容的arrayList
3、另外此聊天室还涉及文件共享，而文件共享部分使用了MySQL来存储用户上传的文件信息，所以使用了mysql-jdbc包，需要建立一个file的数据库，然后建立一个file名字的表，字段分别为id,user,path,realname
#所有请求几乎都是ajax请求
这里就不单独介绍ajax了，可以自己了解一下。
#最后说明：
目前代码，我直接将所有用户信息和聊天信息都存在了arrayList中，明显是不合适的，要想使用必须稳定存储所有信息，目前这样存储只是为了方便理解。
