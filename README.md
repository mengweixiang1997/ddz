## 斗地主
1. 斗地主是什么？
    https://zh.wikipedia.org/wiki/%E9%AC%A5%E5%9C%B0%E4%B8%BB
2. 为什么要做斗地主？
    某砖家说：“长期斗地主有益身心健康”
3. 本项目做了哪些？
    本项目主要业务逻辑集中在后台，玩家叫地主，出牌，比牌，等等。。。前台写得很粗糙。有心人可以fork下来代码，用不同语言来实现斗地主的界面。

#### 牌型大小：初始默认大小2>A>K>Q>J>10>....>4>3，牌型大小只有在同一组合中分大小。王炸都比任何牌大，数字大的炸弹比数字小的炸弹大。
    1、王炸：也就是大小王、最大的牌，最大的炸弹。
    2、炸弹：四张同数值牌，如AAAA这种牌。
    3、四张带两张：四张一样的牌+两张单牌。(注意：四带二不是炸弹)。如：4444+65
    4、三顺：二个或更多的连续三张牌(如：555666、 555666777 )。2和双王不能带入。
    5、飞机带翅膀：三顺+同数量的单牌(或同数量的对牌)。
    6、三张牌：数值相同的三张牌，如777或者KKK。
    7、三张带一对：数值相同的三张牌+一张单牌或一对牌。如：777+33。
    8、顺子：五张或五张以上的连续单牌(如：56789 或8910JQK )。2和双王不能带入。
    9、双顺：三对或三对以上的连续对牌(如：QQKKAA、33445566 )。2和双王不能带入。
    10、单对：数值相同的两张牌，如AA或者22这种双牌。
    11、单牌：单个牌，单张出牌即是单牌。

    From: https://zhidao.baidu.com/question/630346354503276484.html


#### 技术栈 

    前端 REACT
    1. https://github.com/microsoft/TypeScript-React-Starter
    2. Socket-io v2

    后端 Golang
    1. Socket-io
    2. github.com/graarh/golang-socketio

#### 前端交互flow
    name:set
    game:list 
    game:join
    game:wait || game:ready
    [sub] cards:changed && game:options
    game:deal

#### 测试
    在selenium目录下，运行python进行测试

