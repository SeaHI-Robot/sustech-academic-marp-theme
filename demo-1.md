---
marp: true
theme: academic-sustech-1
paginate: true
math: katex
---

<!-- _class: lead -->

# 南方科技大学汇报

#### *"每天叫醒我们的不是闹钟,而是中国高教改革的梦想"*

> 
<br>

<br>

**朱清时**
南方科技大学创校校长
YYYY/MM/DD



---

<!-- _header: 目录 -->

<br>

#### 1. 简介
#### 2. 代码块
#### 3. 公式
#### 4. 插图

---

<!-- _header: 简介 -->

- Marp 是一款用于在 **Markdown** 中创建**幻灯片**的软件。
  - 支持基本 Markdown 语法。
- 您只需在 Markdown 中插入“---”分隔符即可移动到下一页$^1$。
- 该主题参考了[marp-theme-academic](https://github.com/kaisugi/marp-theme-academic)$^2$


> 1: Marp 是根据 CommonMark Markdown 规范开发的，因此它不提供 CommonMark 中未包含的“脚注”语法（使用 '[^1]'）。 因此，我们参考了 https://github.com/marp-team/marp/discussions/150#discussioncomment-1302384 并实现了一个伪脚注。
> 2：一个无聊的脚注

---

<!-- _header: 代码块 -->

```python
import torch
print(torch.cuda.is_available())
```

你可以编写这样的代码块。

```python
from transformers import AutoModelForMaskedLM, AutoTokenizer
model = AutoModelForMaskedLM.from_pretrained("cl-tohoku/bert-base-japanese-whole-word-masking")
tokenizer = AutoTokenizer.from_pretrained("cl-tohoku/bert-base-japanese-whole-word-masking")

inputs = tokenizer.encode_plus("私はとても[MASK]です。", return_tensors='pt')
outputs = model(**inputs)
tokenizer.convert_ids_to_tokens(outputs.logits[0][1:-1].argmax(axis=-1))
```

宽度是可自行缩放的（请参阅 [auto-scaling](https://github.com/marp-team/marp-core#auto-scaling-features) 文档中的自动缩放）。

---

<!-- _header: 公式 -->
<br>

$$ I_{xx}=\int\int_Ry^2f(x,y)\cdot{}dydx $$

$$
f(x) = \int_{-\infty}^\infty
    \hat f(\xi)\,e^{2 \pi i \xi x}
    \,d\xi
$$

你可以写一个这样的公式。 当然，您也可以使用内联 $LaTeX$。  

顺便说一句，您还可以使用表情符号:smile: :art: :fire:

---

<!-- _header: 插图 -->

1. 首先，右键单击从 [链接](https://www.irasutoya.com/2018/10/blog-post_723.html) 下载图像('kenkyu_woman_seikou.png')。
2. 在此 Markdown 目录中创建一个名为“images”的目录，并放置您刚刚下载的图片。 现在你已经准备好了。

<br>

![w:300 center](./images/kenkyu_woman_seikou.png)
