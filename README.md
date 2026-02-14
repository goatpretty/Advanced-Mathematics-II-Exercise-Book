# 高等数学（下）习题集

本项目基于 `ExBook` 模板（`ExBook.cls`）进行整理与扩展，汇总了高等数学（下）的常见题目，适用于刷题整理与快速排版。

## 项目说明
- 模板基础：`ExBook.cls`
- 内容范围：高等数学（下）选择题、填空题、综合大题
- 入口示例：`example_text_type.tex`

## 相比原模板的修改
1. 优化距离
- 在 `standard` 版式下按题型自动控制题后留白：
- `[choice]`：不额外留白
- `[blank]`：题后 `4mm`
- `[big]`：题后 `4cm`

2. 增加缩进与版式优化
- 调整题目与小问排版细节，增强阅读连续性
- 统一题型写法，减少手动 `\vspace` 的依赖

## 最新参考示例（已汇入）

### 选择题
```latex
\begin{bbox}[choice]
  \qitem 向量 $\vec{a}$ 与 $\vec{b}$ 的位置关系是\blankbox。
  \fourchoices{平行}{垂直}{相交}{以上都不是}
\end{bbox}
```

### 填空题
```latex
\begin{bbox}[blank]
  \qitem 方程 $-\dfrac{x^{2}}{4}+\dfrac{y^{2}}{9}=1$ 表示的空间曲面是\blankline。
\end{bbox}
```

### 综合大题（含小问）
```latex
\begin{bbox}[big]
  \qitem 已知 $A\left(1,2,0\right)$、$B\left(2,-1,3\right)$，求：
  \begin{subqitems}
    \subqitem 向量 $\overrightarrow{AB}$ 在三个坐标轴上的投影；
    \subqitem 向量 $\overrightarrow{AB}$ 的方向余弦。
  \end{subqitems}
\end{bbox}
```

## 使用方法
1. 在 `example_text_type.tex` 中录入或替换题目内容。
2. 在 `config.tex` 中配置封面、页眉页脚、主题色等信息。
3. 使用 XeLaTeX 编译生成 PDF。

## 相关文件
- `example_text_type.tex`：完整示例
- `BBOX_TYPE_CHANGES.md`：`bbox` 题型参数与间距规则说明

## 原项目引用
- ExBook 官网：https://exbook.github.io/
- ExBook GitHub：https://github.com/ExBook
