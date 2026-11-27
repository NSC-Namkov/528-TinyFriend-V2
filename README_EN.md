# 528-TinyFriend-V2

**528-TinyFriend-V2** is a **169M-parameter dense language model** trained entirely from scratch by a 15-year-old independent developer, **Namkov (Nan Zhan)**. The model is named after the author's pet silver-fox hamster. Training was done on a single consumer-grade machine with an **RTX 3060 (12GB)** and a **Tesla P4**.

> [中文](./README.md) | [Русский](./README_RU.md)

## Highlights

- **169M parameters, Dense** — no MoE, no distillation
- **Trained from scratch** — 23GB of data, 7 days on one RTX 3060
- **Custom architecture** (`Liminal`): Engram + mHC + Muon optimizer
- **+23.4% over Minimind-3-MoE (197M)** on AlignBench (10 dimensions)

## Quick Start

Download from [ModelScope](https://www.modelscope.cn/models/NSCNamkov/528-TinyFriend-V2)

```bash
pip install -r requirements.txt
python inference.py --model_path ./528-tinyfriend-v2-169m
```

Try it online: [ModelScope Studio](https://www.modelscope.cn/studios/NSCNamkov/528-TinyFriend-V2)

## Benchmark

| Dimension | Minimind-3-MoE (197M) | **TinyFriend-V2 (169M)** |
|---|---|---|
| Overall | 1.344 | **1.659 (+23.4%)** |

Full results: [MODEL_CARD.md](./MODEL_CARD.md)

## Limitations

- Weak at multi-step mathematical reasoning
- Weak at long-context prediction (HellaSwag 27.41%)
- No tool use, no multi-turn dialogue
- Custom kernels are not yet optimized

## License

- Code: MIT
- Weights: CC BY-NC-SA 4.0

## Citation & Acknowledgments

See [MODEL_CARD.md](./MODEL_CARD.md)
