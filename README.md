# ConvCapusleNets
This project implements convolutional capsule net, based on [Hinton's paper](https://arxiv.org/abs/1710.09829), <br> 
The implementation is based on other implementations, including [capsuleEM](https://github.com/gyang274/capsulesEM), [CapsNet-Keras](https://github.com/XifengGuo/CapsNet-Keras), and [tensorflow](https://github.com/Sarasra/models). <br>
<br>
It provides an easy interface for capsnet. <br>
Library functions include: <br>
1. create_init_capsule (create_init_capsule_v2), input is a 2D image with mutli channels, output is a 2D capsule layer, output shaoe is [None,Height, Width,capsule_channel,capsule_dim], where capsule_channel is number of capsules, capsule_dim is the length of each vector.<br>
2. capsule_conv, input is of shape [None, Height, widtion, capsule_channel, capsule_dim], output shape is [None, Height2, widtion2, capsule_channel2, capsule_dim2], performs dynamic routing in a convolutional way. <br>
3. capsule_fc, fully connected capsule layer<br>
4. capsule_length, calculate length of each vector.<br>
5. flatten_conv_capsules, reshape [None, Height, Widtion, channel, dim] into [None, capsule_number,dim]<br>
6. flatten_capsule, reshape [None,capsule_number, capsule_dim] into [None,-1]<br>
<br>
The structure of network will be updated later. <br>
<br>
Requirements:<br>
python >= 3.6, tensorflow, keras <br>
<br>
Usage:<br>

```
$ python main.py
```
To do:<br> 
<del>1. Include routing algorithm </del><br>
2. Extend the idea of dense net.
