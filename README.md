# Note

2018-09-23
运行强化学习进行关系抽取的程序（可能一周才能有结果）

2018-09-27
过程：
工程地址：/home/chenjiafeng/Desktop/TensorFlow_RLRE-master
将训练集，开发集，测试集替换成相应的文件(vec.txt是怎么获取到的)（已完成）
处理类似于 No module named tqdm的异常（已完成）

XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
运行python3 initial.py生成npy文件（已完成）
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX


XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
运行python3 cnnmodel.py（其中epoch从1开始到3,每次执行1742次）
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
  train model
  reading wordembedding
  reading training data
  epoch 1 loss=8.255053 accuracy=0.743333:   10/1742
  epoch 1 loss=8.063448 accuracy=0.753333:   10/1742
  
  然后produce reward sentence_ebd  average_reward for rlmodel（一共执行280579次）
  average_reward = -0.21306534111499786
  

XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
运行python3 rlmodel.py（一共执行26×280579次）
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

  chosen sentence size: 224149
  total_reward: -0.24561
  best_reward -0.24561

  select training data
  326941
  use the selected data to train cnn model
  reading wordembedding
  reading training data
  epoch 1 loss=0.275411 accuracy=0.950000: 
  epoch 2 loss=0.260439 accuracy=0.943333: 
  epoch 3 loss=0.262039 accuracy=0.946667: 

运行python3 cnnrlmodel.py

  epoch: 0
  chosen sentence size: 326941
  total_reward: -0.13297
  best_reward -0.13297
  average score -0.21285311877727509
  best score -0.21285311877727509
  update the rlmodel(一共执行280579次)
  update the cnnmodel(一共执行1090次)
  produce new embedding(一共执行280579次)
  
there are 522,611 sentences
, 281,270 entity pairs
, and 18,252 relational facts in the training data; 
and 172,448 sentences
, 96,678 entity pairs 
and 1,950 relational facts in the test data.
  
  

0：将数据集变成原来的1/10,看一下效率是否可以提高十倍（暂时全量处理）
1：训练关系分类的模型（正在运行，还不知道多久能运行完）
2：训练强化学习的模型
关键点：
1：运行完之后如何获取强化学习生成的数据集


2018-10-01
在联合抽取的数据集上运行强化学习的程序（可能还是一周才有结果）
关键点：
1：把联合抽取的数据集转化成关系抽取的数据集
2：关系的统计与分批处理


运行联合抽取的程序（这个程序自己之前已经运行过了）

删除usr/bin/python后的恢复方法
https://blog.csdn.net/shaojunbo24/article/details/48496133

2018-10-06
1：讲python升级到3.6.5，，，然后继续实验
2：将联合抽取的数据集转化成强化学习的数据集
3：抽取出一批数据
4：用抽取的数据进行实验


2018-10-07
在强化学习抽取的新的数据集上运行联合抽取的程序（可能一周才能有结果）
关键点：
1：强化学习的数据集怎么跟联合抽取的数据集对应起来
