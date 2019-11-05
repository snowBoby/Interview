# interview

1. 箭头函数和普通函数的区别  
（1）箭头函数没有prototype原型，所以没有this。  
（2）箭头函数没有constructor属性，所以不能做为构造函数，不能new，自然里面没有new.target（识别是否使用了new关键字）和super。  
（3）箭头函数没有arguments，可以通过rest参数获取。  
  

2. class和普通构造函数有啥区别：  
   class在语法上更贴合面向对象的写法、本质是语法糖，使用的还是prototype来实现继承  
	（1）类的内部所有定义的方法，都是不可枚举的（但是在es5中prototype的方法是可以进行枚举的）  
	（2）类的构造函数，不使用new是没法调用的，会报错。这是它跟普通构造函数的一个主要区别，后者不用new也可以执行  
	（3）Class不存在变量提升（hoist），这一点与ES5完全不同  
	（4）ES5的继承，实质是先创造子类的实例对象this，然后再将父类的方法添加到this上面（Parent.apply(this)）。ES6的继承机制完全不同，实质是先创造父类的实例对象this（所以必须先调用super方法），然后再用子类的构造函数修改this。  
    

3. sessionStorage、localStorage  

	（1）存储内容的数据类型：两者皆储存字符串类型的数据。  
	（2）生命周期：  
		sessionStorage：生命周期是当前窗口或标签页，一旦窗口或标签页被关闭了，那么所有通过sessionStorage存储的数据也就被清空了。sessionStorage只存在当前tab里，打开新的tab就获取不到了，如果是一直单页面跳转就没问题。刷新不会消失，关闭标签才会消失，一般用于表单填写用户信息刷新页面填写信息消失，就可以用此方法  
		localStorage：生命周期是永久，这意味着除非用户显式操作在浏览器提供的UI上清除localStorage信息，否则这些信息将永远存在。  
	（3）信息是否可共享： 不同浏览器无法共享localStorage或sessionStorage中的信息。相同浏览器的不同页面间可以共享相同的localStorage（页面属于相同域名和端口），但是不同页面或标签页间无法共享sessionStorage的信息。这里需要注意的是，页面及标签页仅指顶级窗口，如果一个标签页包含多个iframe标签且他们属于同源页面，那么他们之间是可以共享sessionStorage的。  

