# Tensorflow & Keras
- machine learning 모델 개발, 학습시키는 핵심 오픈소스 라이브러리

- Keras: tensorflow 쉽고 편하게 사용할 수 있게 해주는 high level API 제공  
Tensorflow 2.x에서 Keras 딥러닝 공식 API로 채택, Tensorflow 내 하나의 framework로 개발됨  
```python
#import
import tensorflow as tf
from tensorflow import keras
```

### - tensor  
- multi-dimensional array
- tensorflow의 기본 data type
- 보통 1차원=vector, 2차원=metrics, 3차원 이상=tensor > 모든 차원 다 합쳐서 tensor라고 부르기도 함
- numpy와 유사
```python
#tensor 생성 방법
print(tf.constant([3, 3], dtype=tf.float32)
outcome) tf.Tensor([3. 3.], shape=(2, ), dtype=float32)

#type() 출력 결과
<class 'tensorflow.python.framework.ops.EagerTensor'>

#list, numpy to tensor
tf.convert_to_tensor(list/np)

#tensor to numpy
tensor.numpy()
```

- variable  
: tensor 값 변경 :exclamation:불가능:exclamation: 변할 수 있는 상태 저장하는데 사용되는 특별한 텐서인 variable  
  DL에서 학습해야 하는 가중치 (weight, bias)들을 variable로 생성
```python
variable = tf.Variable(tensor)

variable[0,0].assign(2) #(0,0) 자리값을 2로 바꿔줘

#weight 만들어 놓고 gradient 계산해서 여기에 learning rate 곱한 값을 빼주는 과정에서 사용됨
variable.assign_sub(tensor) 
```
