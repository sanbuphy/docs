## [ 仅 paddle 参数更多 ]torch.scatter_add

### [torch.scatter_add](https://pytorch.org/docs/1.13/generated/torch.scatter_add.html#torch.scatter_add)

```python
torch.scatter_add(input,
              dim,
              index,
              src)
```

### [paddle.put_along_axis](https://www.paddlepaddle.org.cn/documentation/docs/zh/api/paddle/put_along_axis_cn.html)

```python
paddle.put_along_axis(arr,
                      indices,
                      values,
                      axis,
                      reduce='assign')
```

其中 Paddle 相比 Pytorch 支持更多其他参数，具体如下：

### 参数差异
| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| input        | arr         | 表示输入 Tensor ，仅参数名不一致。                                     |
| dim          | axis        | 表示在哪一个维度 scatter ，仅参数名不一致。                             |
| index        | indices     | 表示输入的索引张量，仅参数名不一致。                                    |
| src          | values      | 表示需要插入的值，仅参数名不一致。                                      |
| -            | reduce      | 表示插入 values 时的计算方式，PyTorch 无此参数，Paddle 应设置为 'add' 。|
