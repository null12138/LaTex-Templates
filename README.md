# LaTeX习题集盒子使用指南

## 1. 普通习题盒子 `exercise`

**语法：**
```latex
\begin{exercise}{题号}
题目内容
\end{exercise}
```

**示例：**
```latex
\begin{exercise}{1.1}
求函数 $f(x) = x^2 + 2x + 1$ 的最小值。
\end{exercise}
```

## 2. 重点习题盒子 `importantexercise`

**语法：**
```latex
\begin{importantexercise}{题号}
重点题目内容
\end{importantexercise}
```

**示例：**
```latex
\begin{importantexercise}{1.2}
已知函数 $f(x) = ax^2 + bx + c$，若 $f(1) = 0$，$f(2) = 3$，$f(0) = -1$，求 $a$、$b$、$c$ 的值。
\end{importantexercise}
```

## 3. 挑战题盒子 `challengeexercise`

**语法：**
```latex
\begin{challengeexercise}{题号}
难题内容
\end{challengeexercise}
```

**示例：**
```latex
\begin{challengeexercise}{1.3}
证明：对于任意实数 $x$，不等式 $x^4 + x^2 + 1 \geq \sqrt{3}x^2$ 恒成立。
\end{challengeexercise}
```

## 4. 答案盒子 `answer`

**语法：**
```latex
\begin{answer}
答案内容
\end{answer}
```

**示例：**
```latex
\begin{answer}
函数的最小值为 $0$，当 $x = -1$ 时取得。

解：$f(x) = x^2 + 2x + 1 = (x+1)^2 \geq 0$

当 $x = -1$ 时，$f(x) = 0$，所以最小值为 $0$。
\end{answer}
```

## 5. 提示盒子 `hint`

**语法：**
```latex
\begin{hint}
提示内容
\end{hint}
```

**示例：**
```latex
\begin{hint}
可以尝试配方法，将二次函数化为顶点式。
\end{hint}
```

## 6. 知识点盒子 `knowledge`

**语法：**
```latex
\begin{knowledge}
知识点内容
\end{knowledge}
```

**示例：**
```latex
\begin{knowledge}
二次函数的一般形式：$f(x) = ax^2 + bx + c$ (其中 $a \neq 0$)

顶点坐标为：$\left(-\frac{b}{2a}, f\left(-\frac{b}{2a}\right)\right)$
\end{knowledge}
```

## 完整使用示例

```latex
\chapter{函数}

\section{二次函数}

\begin{knowledge}
二次函数是形如 $f(x) = ax^2 + bx + c$ 的函数，其中 $a \neq 0$。
\end{knowledge}

\begin{exercise}{1.1}
求函数 $f(x) = x^2 - 4x + 3$ 的最小值。
\end{exercise}

\begin{hint}
使用配方法或者求导数。
\end{hint}

\begin{answer}
$f(x) = x^2 - 4x + 3 = (x-2)^2 - 1$

所以最小值为 $-1$，当 $x = 2$ 时取得。
\end{answer}

\begin{importantexercise}{1.2}
已知二次函数 $f(x) = ax^2 + bx + c$ 的图像过点 $(0,1)$、$(1,4)$、$(2,9)$，求该函数的解析式。
\end{importantexercise}

\begin{challengeexercise}{1.3}
证明：对于任意二次函数 $f(x) = ax^2 + bx + c$ ($a > 0$)，都存在实数 $m$，使得 $f(x) \geq m$ 对所有实数 $x$ 成立。
\end{challengeexercise}
```

## 自定义选项

所有盒子都支持可选参数来自定义样式：

```latex
\begin{exercise}[colback=yellow!20]{1.1}
带黄色背景的习题
\end{exercise}

\begin{answer}[arc=0pt]
带直角的答案盒子
\end{answer}
```

## 注意事项

1. **题号参数**：习题盒子需要提供题号作为必需参数
2. **数学公式**：在盒子内可以正常使用数学公式
3. **嵌套使用**：可以在一个盒子后面跟着另一个盒子
4. **分页**：盒子会自动处理分页问题
5. **颜色主题**：所有盒子的颜色都与文档的主色调保持一致
