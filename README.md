# melon-form
Create winform application with .net and javascript


## 简介
### 使用javascript调用.net库，编写接口，配合html+css编写UI，轻松创建windows form应用程序。
### UI可使用WebForm（html+css），也可使用原生WinForm控件，随心所欲。

## 接口说明

```
//使用js编写接口，可调用.net库

Text="MelonForm";   //窗口标题
Width=990;          //窗口宽度
Height=700;         //窗口高度
MaximizeBox=false;  //是否允许最大化窗口

//WebForm可与原生控件混合使用，也可以将WebForm隐藏

// browser.Visible=false;   //隐藏WebForm，仅使用原生控件
// var a=new Button();      //创建WinForm原生按钮
// var b=new TextBox();     //创建WinForm原生文本框
// a.Text="Click Me";       //给原生控件添加属性，请参考微软相关文档
// this.Controls.Add(a);    //将控件添加到窗体中

//创建接口函数，可任意调用.net类库，在此定义的函数可在main.htm中使用
netApi.getTime=function(){
	return System.DateTime.Now.ToString('yyyy-MM-dd hh:mm:ss');
}

netApi.getHostName=function(){
	return System.Net.Dns.GetHostName().ToString();
}
```
