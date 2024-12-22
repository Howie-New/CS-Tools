# how to use vim 

## #进入vim

vim 进入vim主界面

vim filename 进入该文件

vim flodername 进入文件夹内浏览文件，按Enter进入某个文件

## #vim有两大种模式，即普通模式（命令模式和移动模式和可视化模式）和插入模式

### 1.普通模式：

#### 即操作文本，对文件保存，退出，文本光标移动，选择文本等操作

默认进入时是普通模式

esc 退出插入模式进入普通模式

#### （1）命令模式

:w 保存/写入（write）

:q 退出(quit)

:q! 退出不保存

##### 查找

/查找的词汇  查找词汇

n 查找下一个匹配的词汇

Shift + N 查找上一个匹配的词汇

number + gg 跳到第number行

##### 替换

:s/word1/word2/g  把一行中的word1替换成word2 g(global) 全局

:%s/word1/word2/g  把全局文件中的word1替换成word2

:%s/word1/word2/gc  把全局文件中的word1替换成word2 c(comment) 提示

:set number 显示行号

:num1,num2s/word1/word2/g  把文件中第num1行到第num2行的word1替换成word2

#### （2）移动模式

h j k l 向左向下向上向右移动

Ctrl + F 向下一页

Ctrl + B 向上一页

Ctrl + E 向下滚轮翻页

Ctrl + Y 向上滚轮翻页

Shift + G 移动到最后一行

gg 移动到第一行

b 跳跃到单词首字母 向前跳跃单词（光标永远在单词首字母）

e 跳跃到单词尾字母 向后跳跃单词（光标永远在单词尾字母）

w 向后跳跃单词（光标永远在单词首字母）

Shift + b/e/w 大跳单词

Shift + 6 ^  跳跃到行首

Shift + 4  $ 跳跃到行尾

Shift + { 移动到上一个段落（代码块）之前

Shift + } 移动到下一个段落（代码块）之前

#### （3）复制，选择文本，可视化模式

y (yanked 猛拉)

y + w 复制一个单词，汉字语句

y + Shift + 4($) 复制一行

y + number（数字） 复制从光标开始多少行

v (visual)  开启可视化模式，主要用来选择文本复制剪切，就知道具体选择了那些文本

可视化模式下搭配移动键位选择文本，然后可以剪切（x或d）和复制（y）

选择单词 a + w

选择包含括号a + b (bracket)

选择包含大括号a + B

选择包含尖括号a + <

全选 当光标在文本首时按shift + G 当光标在文本尾时按g

当选择了一些文本时，按o可以跳到选择的首部或尾部继续选择

Shift + V (visual line) 选择行

Ctrl + v (visual block)选择矩阵（块）

Shift + < / > 向左向右缩进

Shift + ~ 大小写切换

u 全部转化为小写

Shift + U 全部转化为大写

0 补全角落



### 2.插入模式：

#### 即编辑文本，对文本的增删改

i 进入插入模式（insert）在光标位置前面插入

a 在光标位置后边插入

o 回车，跳到下一行首插入

x 删除光标所在字符

dd 删除光标所在一行 / 剪切 （相当于把这一行放入vim寄存库中，再按p从寄存库中释放出来）

u 撤销上一步操作

d + w 删除光标所在的单词

r 替换（修改）字母

shift + R 持续替换（replace）（修改）字母   Esc退出

p 粘贴

Ctrl + Shift + V 从外部文本粘贴