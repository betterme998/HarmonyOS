# HarmonyOS

鸿蒙学习

# 1.DevEco Studio 的使用

其是开发 HarmongOS（应用）的一站式集成开发环境，简称为（IDE）

# 2.ArkTS 开发语言介绍

1.TypeScript 快速入门
--1.编程语言介绍
ArkTS 是 HarmonyOS 主力应用开发语言。它在 TypeScript 的基础上，匹配 ArkUI 框架，扩展了声明式 UI，状态管理等相应的能力，让开发者以更简洁，更自然的方式开发跨端应用
.JavaScript 是一种属于网络的高级脚本语言，已经被广泛用于 Web 应用开发，常用来为网络添加各式各样的动态功能，为用户提供流畅美观的浏览效果
.TypeScript 是 JavaScript 的一个超集，它扩展了 JavaScript 的语法，通过在 JavaScript 的基础上添加静态类型定义构建而成，是开源的编程语言
.ArkTS 基于 TypeScript 语言，扩展了声明式 UI，状态管理，并发任务等能力

# --2.基础类型(11 种)

1.布尔值：TypeScript 可以使用 boolean 来表示这个变量是布尔值，可以赋值为 true 或 false
let isDone:boolean = false;

2.数字
TypeScript 里的所有数字都是浮点数，这些浮点数的类型是 number。支持十进制，二进制，八进制，十六进制
let decLiteral:number = 2023

3.字符串
TypeScript 里使用 string 表示文本数据类型，可以使用双引号"或单引号'表示字符串
let name:string = "Jacky"

4.数组
TypeScript 支持以下两种方式声明数组：第一种，可以在元素类型后面接[]，表示由此类型元素组成一个数组；第二种方式是使用数组泛型，Array<元素类型>
let list1:number[] = [1,2,3]
let list2:Array<number> = [1,2,3]

5.元组
元组类型允许表示一个已知元素数量类型的数组，各元素的类型不必相同
let x:[string,number]
x = ['hello',10]

6.枚举
enum 类型是对 JavaScript 标准数据类型的一个补充，使用枚举类型可以为一组数值赋予友好的名字
enum Color {red,green,blue}
let c:Color = Color.Green

7.unknown
我们会想要为那些编程阶段还不清楚类型的变量指定一个类型，那么我们可以使用 unknowm 类型来标记那些变量
let notSure:unknown = 4;
notSure = 'string instead'
notSure = false;

8.void
当一个函数没有返回值时，你通常会见到其返回值类型是 void
function test():void {
console.log('This is function is void')
}

9.null 和 undefined （两种类型）
TypeScript 里，undefined 和 null 两者各自有自己的类型分别叫做 undefined 和 null
let u:undefined = undefined
let n:null = null

10.联合类型
联合类型（Union Type）表示取值可以为多种类型中的一种
let myFavoriteNumber:string|number;
myFavoriteNumber = 'seven'
myFavoriteNumber = 7

# --3.条件语句

条件语句用于基于不同的条件来执行不同的动作。TypeScript 条件语句是通过一条或多条语句执行结果（true 或 false）来决定执行的代码块

1.if 语句，if...else 语句，if...else if...else 语句

2.switch...case 语句

# --4.函数

函数是一组一起执行一个任务的语句，函数声明要告诉编译器函数的名称，返回类型和参数，TypeScript 可以创建有名字的函数的匿名函数

<!-- 有名函数，变量为number -->

function add(x:number,y:number):number {
return x+y
}

<!-- 匿名函数 -->

let myAdd = function(x:number,y:number):number{
return x+y
}

在 TypeScript 里我们可以在参数名旁使用（？）实现可选参数的功能

function buildName(firstName:string,lastName?:string){

  <!-- 这一步判断是必须的 -->

if(lastName){
return firstName + '' + lastName
}else{
return firstName
}
}
let result1 = buildName('Bob');
let result2 = buildName('Bob','Adams');

函数的剩余参数
剩余参数会被当做一个不限的可选参数。可以一个都没有，同意也可以任意一个，可以使用省略号（...）进行定义
function getEmployeeName(firstName:string,...restOfName:string[]){
return firstName + '' + restOfName.join('')
}

let employeeName1 = getEmployeeName('tom')
let employeeName2 = getEmployeeName('tom','sandy',lucas)

箭头函数
ES6 版本 TypeScript 提供了一个箭头函数，它是定义匿名函数的简写语法，用于函数表达式，它省略了 function 关键字
([param1,param2,...paramn]) => {//代码块}
其中，括号内是函数的入参，可以有 0 到多个参数。可以赋值给变量
let arrowFun = ([param1,param2,...paramn]) => {//代码块}

# --5.类

TypeScript 支持基于类的面向对象的编程方式，定义类的关键字为 class，后面紧跟类名，
--6.模块
--7.迭代器

# 2.ArkTS 基础知识

--ArkTS 简介
--UI 描述规范
--常用修饰器@Component@Entry
--渲染控制
--状态管理
3.Arkts 开发实战
