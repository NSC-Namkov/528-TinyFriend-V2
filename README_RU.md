# 528-TinyFriend-V2

**528-TinyFriend-V2** — это **плотная (dense) языковая модель с 169M параметров**, полностью обученная с нуля независимым 15-летним разработчиком **Намковым (Нань Чжань)**. Модель названа в честь домашнего хомяка автора. Обучение проводилось на одной потребительской машине с **RTX 3060 (12GB)** и **Tesla P4**.

> [中文](./README.md) | [English](./README_EN.md)

## Ключевые особенности

- **169M параметров, Dense** — без MoE
- **Обучена с нуля** — 23 ГБ данных, 7 дней на одной RTX 3060
- **Собственная архитектура** (`Liminal`): Engram + mHC + оптимизатор Muon
- **+23,4% к Minimind-3-MoE (197M)** по AlignBench (10 измерений)

## Быстрый старт

Скачать с [ModelScope](https://www.modelscope.cn/models/NSCNamkov/528-TinyFriend-V2)

```bash
pip install -r requirements.txt
python inference.py --model_path ./528-tinyfriend-v2-169m
```

Попробовать онлайн: [ModelScope Studio](https://www.modelscope.cn/studios/NSCNamkov/528-TinyFriend-V2)

## Бенчмарк

| Измерение | Minimind-3-MoE (197M) | **TinyFriend-V2 (169M)** |
|---|---|---|
| Итог | 1.344 | **1.659 (+23,4%)** |

Полные результаты: [MODEL_CARD.md](./MODEL_CARD.md)

## Ограничения

- Слаба в многошаговых математических рассуждениях
- Слаба в предсказании длинного контекста (HellaSwag 27,41%)
- Нет вызова инструментов, нет многоходового диалога
- Собственные ядра пока не оптимизированы

## Лицензия

- Код: MIT
- Веса: CC BY-NC-SA 4.0

## Цитирование и благодарности

См. [MODEL_CARD.md](./MODEL_CARD.md)
