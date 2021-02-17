# PlantUML

```puml
@startuml
actor actor
agent agent #green
artifact artifact #lightgreen
boundary boundary #darkseagreen
card card #orange 
cloud cloud #yellowgreen
component component #FF7777
control control #yellow
database database #LightSkyBlue
entity entity
file file #red
folder folder
frame frame
interface  interface
node node #aaaaaa
package package #hotpink
queue queue #olive
stack stack #peru
rectangle rectangle #Silver
storage storage #SaddleBrown
usecase usecase #AAFFFF
note bottom of usecase:This is a note
node node2 [
这是个结点
----
您可以使用
===
不同类型
....
的分隔符
]
folder folder2 [
这是个 <b>文件夹
----
您可以使用
===
不同类型
....
的分隔符
]

[3332]
(666)
"233"

@enduml
```

```puml
@startuml

node node1
node node2
node node3
node node4
node node5
node1 -- node2
node1 .. node3
node1 ~~ node4
node1 == node5

node2 <|-> node3
node3 -o node4
node4 *- node5
@enduml
```

```puml
@startuml

"ddd" -up->"First Activity"
-right-> "Second Activity"
--> "Third Activity"
@enduml
```

```puml
@startuml
object "努尔哈赤" as nu{
太祖
天命
}

object "皇太极" as htj

object 顺治 #yellow

nu--o htj
nu-|> 顺治
@enduml
```

```puml
@startuml
colors
@endtuml
```

```puml
@startuml
colors blue
@endtuml
```

甘特图

```puml
@startuml
project starts the 2018/03/29
saturday are closed
2018/04/17 to 2018/04/19 is closed
[Prototype design] lasts 14 days
[Test prototype] lasts 4 days
[Test prototype] starts at [Prototype design]'s end
[Prototype design] is colored in Fuchsia/FireBrick
[Test prototype] is colored in GreenYellow/Green
[小论文] lasts 3 days and is 30% complete
@enduml
```

```puml
@startmindmap
*[#Orange] Colors
**[#lightgreen] Green
**[#FFBBCC] Rose
**[#lightblue] Blue
@endmindmap
```
