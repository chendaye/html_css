# css动画

## 动画类型

> transition补间（过度）动画 ：开头结尾确定，补中间
- 位置、平移：left、right、margin、transform
- 方位、旋转：transform
- 大小、缩放：transform
- 透明度：opacity
- 其他-线性变换：transform

> keyframe 关键帧动画

- 补间动画需要有状态改变触发；关键帧动画不需要

> 逐帧动画 

- 使用 keyframe实现
- 无法补间计算的动画，资源较大 
- 使用steps(1) 去掉关键帧之间的补间