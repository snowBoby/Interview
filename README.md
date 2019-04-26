# interview

1、箭头函数和普通函数的区别
  （1）箭头函数没有prototype原型，所以没有this。
  （2）箭头函数没有constructor属性，所以不能做为构造函数，不能new，自然里面没有new.target（识别是否使用了new关键字）和super。
  （3）箭头函数没有arguments，可以通过rest参数获取。
