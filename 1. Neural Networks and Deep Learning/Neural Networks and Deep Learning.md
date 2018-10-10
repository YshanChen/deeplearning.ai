#### 1. Introduction to deep learning

#### 2. Neural Networks Basics

##### 1. Logistic Regression

 1. 推导逻辑回归。模型 => 策略(损失函数) => 算法(梯度下降)

    * 为什么逻辑回归的损失函数，不是平方误差损失函数？

      $$L(\hat{y},y) = -(ylog(\hat{y})+(1-y)log(1-\hat{y}))$$

    * 损失函数($$Loss\ Function\ or\ Error\ Function$$)，单一样本/示例的优化：

      $$L(\hat{y},y) = -(ylog(\hat{y})+(1-y)log(1-\hat{y}))$$

      代价函数($$Cost\ Function$$)，寻找$$W\ \&\ b$$以代价函数整体成本：

      $$J(W,b)=\frac{1}{M}\sum_{i=1}^m{L(\hat{y^{(i)}},y^{(i)})}$$    

      The loss function computes the error for a single training example; the cost function is the average of the loss functions of the entire training set. 损失函数计算单个示例的误差，代价函数是整体训练集的损失函数的平均。


