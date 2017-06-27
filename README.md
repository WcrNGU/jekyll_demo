# Jekyll构建的个人博客
   这是一个未来的程序员用jekyll框架在github page页面创建的个人博客，目前比较简陋，有空会改善  
   [页面连接](wcrngu.github.io/jekyll_demo/)

   > 此博客采用github page做服务器，利用jekyll框架自动生成页面（js也可以实现，因为js解释器在客户端集成，不受github page的限制），利用一些简单的html+css知识以及本人很low的审美水平写基本页面，支持用markdown和html两种方法在-post文件夹下添加博文
   
   注意事项：  
1. 写博文不能使用windows自带的笔记本，会有一些格式上的错误，推荐使用notepad++
2. 写博文的jekyll头部时，layout和title的冒号后面必须加一个空格，否则不能识别（具体原因为utf-8无DOM模式，用windows自带记事本写的文件开头会有一个标记，显示在github编辑页面如下图）[无法显示图片](wcrngu.github.io/jekyll_demo/image/utf-8-wrong.jpg)
	   
   待实现的功能：  
1. 博文分组、点击分组标签显示相应分组的博文
2. 代码高亮
	       
更新：查阅了jekyll的官方文档后发现jekyll本身自带代码高亮语法，语法格式如下
``` 
{% highlight ruby linenos %}	//linenos意为显示行数
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}
``` 
