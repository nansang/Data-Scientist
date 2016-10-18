#Django

> 创建及进入虚拟环境
> 
> python3 -m venv djangogirls_venv
> 
> source djangogirls_venv/bin/activate

###django project (专案资料夹，我的理解其实就是一个工程，然后里面就有很多app（也就是模块功能）)
> 建立project
> 
> django-admin.py startproject mysite
> 
> python manage.py runserver (-h) 执行命令
> 
> 创建第一个django app 
> 
> python manage.py startapp <name>
> 



### Djdango的MTV 架构

这一块是网络请求及响应的基础。请求框架都是有的，直接调用就好了。注意要导入相关的库

request处理流程：

- 浏览器送出http request
- django依据url configuration分配至对应的view
- view进行资料库的操作或其它运算，并回传httpresponse物件
- 浏览器依据http response显示网页画面

> 这里要注意的是两个文件，一个是app(上面已提到如何创建)中的views.py文件
> 
- 從 django.http 模組中引用 HttpResponse 類別
- 宣告 hello_world 這個 view
- 當 hello_world 被呼叫時，回傳包含字串 Hello World! 的 HttpResponse 物件。

另一个是mysite 中的urls.py 定位要显示的相关内容（URL Conf）

- 通常定義在 urls.py
- 是一連串的規則 (URL patterns)
- Django 收到 request 時，會一一比對 URL conf 中的規則，決定要執行哪個 view function

> 地址写法 url(regex, view)
> 
>  例子 url(r'^hello/$', hello_world),
	
	-regex -- 定義的 URL 規則
		規則以 regular expression（正規表示式）來表達
		
	r'^hello/$' 代表的是 hello/ 這種 URL
		view -- 對應的 view function
		指的是 hello_world 這個 view
		
		
##templates（html/css单独写，增加可读性）
##models（定义资料库的结构，为实现各类数据库的互通）
##admin（字面意思，为了增加一个管理者，管理后台）
##django orm（数据库的相关操作，增删改查）
##template tags（）
>Django template tags 讓你可以在 HTML 檔案裡使用類似 Python 的語法，動態存取從 view function 傳過來的變數，或是在顯示到瀏覽器之前幫你做簡單的資料判斷、轉換、計算等等。


##dynamic url（实现界面的跳转）
##deploy(部署到服务器上)


后面的简写了，如果能明白之前的那部分详情，基本就没有问题了，最后一个是部置到云服务器上。具体实现可以参考这个网址：

[django](https://djangogirlstaipei.gitbooks.io/django-girls-taipei-tutorial/content/django/deploy.html)

我照着上面弄实现了一个自己的一个网站，还比较简单。
> https://djangoboydiary.herokuapp.com/
