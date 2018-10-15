### 1. Introduction to deep learning

-------

### 2. Neural Networks Basics

##### 1. Logistic Regression

 1. 推导逻辑回归。模型 => 策略(损失函数) => 算法(梯度下降)

    * 为什么逻辑回归的损失函数，不是平方误差损失函数？

      $$L(\hat{y},y) = -(ylog(\hat{y})+(1-y)log(1-\hat{y}))$$

    * 损失函数($$Loss\ Function\ or\ Error\ Function$$)，单一样本/示例的优化：

      $$L(\hat{y},y) = -(ylog(\hat{y})+(1-y)log(1-\hat{y}))$$

      代价函数($$Cost\ Function$$)，寻找$$W\ \&\ b$$以代价函数整体成本：

      $$J(W,b)=\frac{1}{M}\sum_{i=1}^m{L(\hat{y^{(i)}},y^{(i)})}$$    

      The loss function computes the error for a single training example; the cost function is the average of the loss functions of the entire training set. 损失函数计算单个示例的误差，代价函数是整体训练集的损失函数的平均。

##### 2. Derivatives with a Computation Graph

1. $$(a, b, c) => y = f(a,b,c) $$ ：求Y的输出值，前向传播；
2. $$y = f(a,b,c) => \frac{df}{d(a,b,c)}$$ ：求Y的偏导数，后向传播；

##### 3. Logistic Regression - Loss Function & Cost Function

**Loss Function:**

$$if \ \ \ \ y=1,\ \ \ P(y|x) =\hat{y}=\sigma(z)=\sigma(w^Tx+b) $$

$$if \ \ \ \ y=0,\ \ \ P(y|x) =1-\hat{y}=1-\sigma(z)=1-\sigma(w^Tx+b) $$

$$So:\ \ P(y|x)=\hat{y}^y*(1-\hat{y})^{1-y}$$

$$log(.)$$是绝对单调递增函数，故最大化$$P(y|x)$$等价于最大化$$logP(y|x)$$

由此得到：				$$logP(y|x)=ylog(\hat{y})+(1-y)log(1-\hat{y})$$

最大化概率$$P(y|x)$$等价于最小化损失函数，即：

						$$L(\hat{y},y) = -(ylog(\hat{y})+(1-y)log(1-\hat{y}))$$

**Cost Function:**

$$P(label\ in\ set)=\prod_{i=1}^{m}P(y^{(i)}|x^{(i)})\ \ -基于样本间iid$$

**利用最大似然估计原理：**找到参数$$(w,b)$$，使其能够最大化训练集中样本出现的概率。

$$minimize:\  J(w,b)=logP(...)=\sum_{i=1}^{m}logP(y^{(i)}|x^{(i)})=\frac{1}{M}\sum_{i=1}^m{L(\hat{y^{(i)}},y^{(i)})}$$







