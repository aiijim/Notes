#SWift快速参考

##类实现

	class MyClass : OptionalSuperClass, OptionalProtocol1, OptionalProtocol2
	{
	     var myProperty:String
	     var myOptionalProperty:String?
		     
		  //更多属性
		  //如果是继承的父类方法只需要override关键字
		  override init()
	     {
	        myProperty = "Foo"
	     }
		     
		  //更多方法
	}

##函数

	func doIt() -> Int 
	{
	    return 0
	}
	
	func doIt(a:Int) -> Int
	{
	    return a
	}
	
	func doIt(a:Int, b:Int) -> Int 
	{
	    return a + b
	}

##创建/使用实例

	var a = MyClass()
	a.myProperty
	a.doIt()
	a.doIt(1)
	a.doIt(2,b:3)

##枚举
	enum CollisionType : Int
	{
	    case Player = 1
	    case Enemy = 2
	}
	
	var type = CollisionType.Player

##声明变量

	//变量
	var mutableDouble:Double = 1.0
	mutableDouble = 2.0
	
	//常量
	let constantDouble:Double = 1.0
	
	var mutableInferredDouble = 1.0
	
	var optionalDouble:Double? = nil
	if let definiteDouble = optionalDouble
	{
	    definiteDouble
	}
	
	数据类型
	Int、Float、Double、Bool、String、ClassName

##控制流
	//条件控制
	var condition = true
	if condition 
	{
	} 
	else 
	{
	}
	
	var val = 5
	switch val 
	{
		case 1:
		   "foo"
		case 2:
		   "bar"
		default:
			"baz"
	}
	//循环控制 
	for i in 0..<3   //包括上限使用... 
	{
	}
##字符串
	var personOne = "Ray"  
	var personTwo = "Marco"  
	var combinedString = "\(personOne):Hello, \(personTwo)"
	var tipString = "2499"
	var tipInt = NSString(string: tipString).intValue
	
	tipString = "24.99"
	var tipDouble = NSString(string: tipString).doubleValue

##数组
	var person1 = "Ray"
	var person2 = "Marco"
	var array:[String] = [person1,person2]
	array.append("Waldo")
	for person in array 
	{
	    print("person:\(person)")
	}
	var waldo = array[2]
##字典
	var dict:[String:String] = ["Frog":"Kermit","Pig":"Ms. Piggy","Weirdo":"Gonzo"]
	dict["Weirdo"] = "Felipe"
	dict["Frog"] = nil
	for (type, muppet) in dict
	{
		print("type:\(type),muppet:\(muppet)")
	}