# 528-TinyFriend-V2

**528-TinyFriend-V2** 是一个仅有 **169M 参数**的稠密（Dense）语言模型，由 15 岁独立开发者 **南栈（Namkov）** 完全从零训练，原型是作者养的银狐仓鼠。训练硬件仅为一台搭载 **RTX 3060 (12GB)** 和 **Tesla P4** 的消费级主机。

> [English](./README_EN.md) | [Русский](./README_RU.md)

## 亮点

- **169M 参数，Dense** —— 非 MoE
- **从零训练** —— 23GB 数据，单张 RTX 3060 预训练 7 天
- **自定义架构**（`Liminal`）：Engram + mHC + Muon 优化器
- **AlignBench 十维度总分 +23.4%**，超越 Minimind-3-MoE (197M)

## 快速开始

从 [ModelScope](https://www.modelscope.cn/models/NSCNamkov/528-TinyFriend-V2) 下载

```bash
pip install -r requirements.txt
python inference.py --model_path ./528-tinyfriend-v2-169m
```

在线体验：[ModelScope Studio](https://www.modelscope.cn/studios/NSCNamkov/528-TinyFriend-V2)

## 评测

| 维度 | Minimind-3-MoE (197M) | **TinyFriend-V2 (169M)** |
|---|---|---|
| 总分 | 1.344 | **1.659 (+23.4%)** |

完整结果见 [MODEL_CARD.md](./MODEL_CARD.md)

## 局限性

- 多步数学推导能力弱
- 长文本预测差（HellaSwag 27.41%）
- 无工具调用、无多轮对话
- 自定义算子尚未优化

## 许可证

- 代码：MIT
- 权重：CC BY-NC-SA 4.0

## 引用与致谢

见 [MODEL_CARD.md](./MODEL_CARD.md)
