## [torch 参数更多 ]torch.arctan2
### [torch.arctan2](https://pytorch.org/docs/stable/generated/torch.arctan2.html#torch.arctan2)

```python
torch.arctan2(input,
            other,
            *,
            out=None)
```

### [paddle.atan2](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/atan2_cn.html)

```python
paddle.atan2(x,
             y,
             name=None)
```

其中 Pytorch 相比 Paddle 支持更多其他参数，具体如下：

### 参数映射
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| input | x | 表示输入的 Tensor ，仅参数名不一致。  |
| other | y | 表示输入的 Tensor ，仅参数名不一致。  |
| out | -  | 表示输出的 Tensor ， Paddle 无此参数，需要进行转写。    |


### 转写示例
#### out：指定输出
```python
# Pytorch 写法
torch.arctan2(input, other, out=y)

# Paddle 写法
paddle.assign(paddle.atan2(input, other), output=y)
```
