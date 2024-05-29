---
marp: true
theme: uncover
headingDivider: 3
# footer: 統計学入門 | Intro to Statistics ![width:30px](../images/yoh%20with%20globe.png)
paginate: true
---

<style>
small {font-size:0.6em}
medium {font-size:0.8em}
large {font-size:2em}
xlarge {font-size:4em}
gray {padding:20px;background-color:whitesmoke;font-weight:800;line-height:2.5}
plum {padding:20px;background-color:plum;line-height:3;font-weight:800}
t1 { font-size:4em;font-weight:100;line-height:1}
xl { font-size:2.5em;font-weight:100;line-height:1}
xls { font-size:1.5em;font-weight:100;line-height:1}
h1,h2,h3,h4,h5{font-family:serif}
section {font-size:2em;font-weight:300;}
left {text-align:left;}
latex {font-size:2em;color:#444;line-height:1;font-weight:lighter}
</style>


# Introduction to Statistics
#### 統計学入門

Week 9 | June 20, 2023


## Week 8 小テスト
#### 😬 😱 🫦 🙀

##
![](../images/w9/results.png)


## Last week

### 標準偏差の公式
(population・母集団)

<latex>

$$ \sigma =\sqrt{\frac{1}{N}\sum\limits_{i=1}^N (x_i - \mu)^2} $$

</span>


### 正規分布
![width:800](../images/bell%20curve.png)
The "bell" curve

##
![Alt text](../images/sd1.png)

##

![Alt text](../images/sd2.png)




# Topic #1: 変動係数<br>Coefficient of Variation

データの相対的な<plum>ばらつき</plum>を表す統計量

## 

<span style="font-size:4em;font-weight:lighter">
CV= σ/μ
​</span>
変動係数 = 標準偏差/平均値
​

##

変動係数っていつ使うの？

ある測定をカテゴリー別で<plum>比べたい</plum>時！

##

例えば：男子・女子の50m走

<large>

6歳の時と19歳の時のデータの
ばらつきはどう違う？

</large>

##

![width:600](images/cv1.png)

##

![width:600](images/cv2.png)

##

![width:600](images/cv3.png)


## ではやってみよう！

1. グループに分かれる
1. [このページ](https://www.e-stat.go.jp/stat-search/files?page=1&layout=datalist&toukei=00402102&tstat=000001088875&cycle=0&tclass1=000001133904&tclass2val=0)から好きな項目を選ぶ
1. EXCELファイルをダウンロードして開く
1. 変動係数を計算する
1. 面白く発表！


# Topic #2: 標準化とZ得点<br>Z-Score

![Alt text](../images/standardize.png)

#

<latex>

$$ Z得点 = \frac{x_i - \mu}{\sigma} $$

</latex>

### 

このクラスの平均身長
<span style="font-size:3.5em;font-weight:lighter">165cm(μ)</span>
標準偏差
<span style="font-size:3.5em;font-weight:lighter">7cm(σ)</span>
先生の身長は177cm ➡︎ 標準化すると？

##


<latex>

$$ Z得点 = \frac{177 - 165}{7} = 1.71 $$

</latex>



###
![Alt text](../images/standardization%201.png)

###
![Alt text](../images/standardization%202.png)

###
![Alt text](../images/standardization%203.png)

###
![Alt text](../images/standardization%204.png)

### すなわち

![Alt text](../images/standardization%205.png)

###

![Alt text](<images/cv chart.png>)
https://www.mathsisfun.com/data/standard-normal-distribution-table.html

# Topic #3: 偏差値

##

偏差値は、テストや試験の結果を分かりやすく比較するための指標です。偏差値は、あなたのスコアが他の人々と比べてどれくらいの位置にあるかを示す数値です。

##

それって変動係数と一緒じゃないの？

##

You are right! But the difference is...

偏差値のスケールでは、<plum>50</plum>が平均値とされ、標準偏差が<plum>10</plum>とされています。

偏差値の計算には、次の手順を使用します。


##

偏差値の計算:

<latex>

$$ 偏差値 = Z得点 \times 10 + 50 $$

</latex>

##

先ほどの先生の身長は177cmだと、偏差値は？

<latex>

$$ 偏差値 = 1.71 \times 10 + 50 = 67.1 $$

</latex>




### 
では、あなたは？


### Excel playground

![width:1000](../images/excel%20w9.png)

## EXCEL Hints

(カッコの中の英数字はデータによって異なる)

<gray>平均　= AVERAGE(D4:D30)
<gray>合計　= SUM(E4:E30)
<gray>偏差　= SUM(=C4/$C$31)（ドル縛り）
<gray>偏差二乗　= D4^2
<gray>分散の平方根　= SQRT(J5)
<gray>Nは？　= COUNTA(B4:B30)