# js拼图小游戏

```flow
st=>start: 初始化加载图片 
op=>operation: 开始游戏
cond=>condition: 完成拼图(是或否?)
sub1=>subroutine: 重新开始
io=>inputoutput: 输出拼图时间
e=>end: 游戏结束
st->op->cond
cond(yes)->io->e
cond(no)->sub1(right)->op
```

#### 功能描述



 - [x] 将图片划成块
    - [x] 随机分割图片
    - [x] 判断是否拼好
 - [x] 拖拽图片
 - [x] 游戏
    - [x] 开始
    - [x] 重开
 - [x] 游戏计时
 - [ ] 拖拽上传

##### 1.step1 拖拽上传

- 设置元素为可拖放

  - 拖动什么dragstart 

  - 放到何处drag 

  - 进行放置 dragend 

- 思路：
  - 拖放事件：（分为拖放元素事件和目标元素事件）
  - 拖放元素事件（*拖拽文件监听的事件*）：
    - dragstart : 拖拽前触发
    - drag : 拖拽前、拖拽结束之间，连续触发
    - dragend : 拖拽结束触发 
  - 目标元素事件（*拖拽进目标区域监听的事件*）：
    - dragenter : 进入目标元素触发
    - dragover : 进入目标、离开目标之间，连续触发
    - dragleave : 离开目标元素触发
    - drop : 在目标元素上释放鼠标触发 

##### 2.step2 随机分割图片

##### 3.step3  判断是否拼好

