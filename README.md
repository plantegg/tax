# tax
beijing tax 2019

北京个人所得税计算器，综合计税，包含年终奖、股票期权税计算。比较年终奖合并和独立计税的优劣，推荐年终奖合适的纳税方式，减少个人所得税。
其他省市只需要修改五险一金的基数即可通用

几个省税的点:

1)  大部分情况下奖金、工资分开计税税更少，但是如果奖金落在盲区的话合并交税反而税更少（因为利用了工资税扣减数不用除12）

2） 目前奖金、工资可以合并也可以单独计税，二选一，默认单独计税

3） 股票比年终奖少扣税，同样100万，股票收入到手比年终奖多了17万(因为股票税没有盲区）

最后附送一个案例，100万年终奖和100万股票收入的差别，同时100万年终奖跟工资合并计税税更少; 同时如果100万年终奖采用合并计税也比单独计税拿到手要多

a) 股票都是独立计税，税率扣减数跟工资一样，只是没有6万的免税额度
b) 案例：税前月薪为 50000，年终奖为1000000, 股票为1000000， 实际结果100万股票交税比100万年终奖少了17万；100万年终奖和工资合并交税要少交4.6万

```
$python ./tax_Beijing.py 50000-2000+1000000++1000000  (底薪-六项扣减数+年终奖++股票期权收入)
--------------------------------------------------------------------------------------------------------------------------------------------
                                  2019年北京市个人所得税计算方法（税前月薪为 50000，年终奖为1000000, 股票为1000000）
--------------------------------------------------------------------------------------------------------------------------------------------                                  

            应纳税额  ->  五险一金   起征点   专项扣除  适用税率    纳税    ->  到手工资  公积金    ->  年终奖  合并扣税  单独计税     股票
    1月      50,000   ->   5,639     5,000     2,000      10%      1,216    ->   43,145    6,096    ->     0         0         0         0     
    2月      50,000   ->   5,639     5,000     2,000      10%      3,736    ->   40,625    6,096    ->     0         0         0         0     
    3月      50,000   ->   5,639     5,000     2,000      10%      3,736    ->   40,625    6,096    ->     0         0         0         0     
    4月      50,000   ->   5,639     5,000     2,000      20%      4,280    ->   40,080    6,096    ->     0         0         0         0     
    5月      50,000   ->   5,639     5,000     2,000      20%      7,472    ->   36,889    6,096    ->     0         0         0         0     
    6月      50,000   ->   5,639     5,000     2,000      20%      7,472    ->   36,889    6,096    ->     0         0         0         0     
    7月      50,000   ->   5,639     5,000     2,000      20%      7,472    ->   36,889    6,096    ->     0         0         0         0     
    8月      50,000   ->   5,639     5,000     2,000      20%      7,472    ->   36,889    6,096    ->     0         0         0         0     
    9月      50,000   ->   5,639     5,000     2,000      25%      9,285    ->   35,076    6,096    ->     0         0         0         0     
   10月      50,000   ->   5,639     5,000     2,000      25%      9,340    ->   35,021    6,096    ->     0         0         0         0     
   11月      50,000   ->   5,639     5,000     2,000      25%      9,340    ->   35,021    6,096    ->     0         0         0         0     
   12月      50,000   ->   5,639     5,000     2,000      30%      10,757   ->   33,604    6,096    -> 1,000,000  611,750   565,160   731,920  
--------------------------------------------------------------------------------------------------------------------------------------------
    总      600,000   ->   67,668    60,000    24,000     30%      81,580   ->  450,752    73,155   ->              Good             

```
