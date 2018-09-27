# Note

2018-09-23
运行强化学习进行关系抽取的程序（可能一周才能有结果）

2018-09-27
过程：
工程地址：/home/chenjiafeng/Desktop/TensorFlow_RLRE-master
将训练集，开发集，测试集替换成相应的文件(vec.txt是怎么获取到的)（已完成）
处理类似于 No module named tqdm的异常（已完成）
运行python3 initial.py生成npy文件（已完成）
运行python3 cnnmodel.py（其中epoch从1开始到3,每次执行1742次）
  train model
  reading wordembedding
  reading training data
  epoch 1 loss=8.255053 accuracy=0.743333:   10/1742
  epoch 1 loss=8.063448 accuracy=0.753333:   10/1742
  
  然后produce reward sentence_ebd  average_reward for rlmodel（一共执行280579次）
  average_reward = -0.21306534111499786
运行python3 rlmodel.py（一共执行280579次）
  chosen sentence size: 224149
  total_reward: -0.24561
  best_reward -0.24561
  
  

运行python3 cnnrlmodel.py
  
  

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


2018-10-07
在强化学习抽取的新的数据集上运行联合抽取的程序（可能一周才能有结果）
关键点：
1：强化学习的数据集怎么跟联合抽取的数据集对应起来
