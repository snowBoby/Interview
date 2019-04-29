# interview

1、箭头函数和普通函数的区别
  （1）箭头函数没有prototype原型，所以没有this。
  （2）箭头函数没有constructor属性，所以不能做为构造函数，不能new，自然里面没有new.target（识别是否使用了new关键字）和super。
  （3）箭头函数没有arguments，可以通过rest参数获取。
  
2、class和普通构造函数有啥区别：
   class在语法上更贴合面向对象的写法、本质是语法糖，使用的还是prototype来实现继承
	（1）类的内部所有定义的方法，都是不可枚举的（但是在es5中prototype的方法是可以进行枚举的）
	（2）类的构造函数，不使用new是没法调用的，会报错。这是它跟普通构造函数的一个主要区别，后者不用new也可以执行
	（3）Class不存在变量提升（hoist），这一点与ES5完全不同
	（4）ES5的继承，实质是先创造子类的实例对象this，然后再将父类的方法添加到this上面（Parent.apply(this)）。ES6的继承机制完全不同，实质是先创造父类的实例对象this（所以必须先调用super方法），然后再用子类的构造函数修改this。
	
