# EVA8

### Network is in Excel sheet 

## Forward Propagation
$$ h1 = i1 * w1 + i2 * w2 $$
```math
\begin{aligned}

  a\_h1 = \sigma (h1) \\
 \sigma (h1) = 1/(1+\exp (-h1))
 \end{aligned}
 
 ```
 
 
 ``` math 
 o1 = w5 * a\_h1 + w6 * a\_h2 
 ```
 ```math
 a\_o1 = \sigma (o1)

 ```
 ```math
 E1 = 0.5 * (t1 - a\_o1)^2
```
> Similarly for E2

$$ E = E1 + E2 $$

## Backpropagation



> Derivatives : 

```math
\frac{\partial E\_total}{\partial E1} = 1
```
```math
      \frac{\partial E\_total}{\partial E2} = 1 
```

```math 
\frac{\partial a\_o1}{\partial o1} = a\_o1 * (1-a\_o1) 
```

```math 
 \frac{\partial o1}{\partial a\_h1} = w5
 ```
 
```math
\begin{aligned}
\frac{\partial E\_total}{\partial w5} = \frac{\partial E\_total}{\partial a\_o1}* \frac{\partial a\_o1}{\partial o1} * a\_h1  \\
\frac{\partial E\_total}{\partial w8} = \frac{\partial E\_total}{\partial a\_o2}* \frac{\partial a\_o2}{\partial o2}* a\_h2 \\
\end{aligned}
```

 
 ```math 
 \begin{aligned}
 \frac{\partial h1}{\partial w1} = i1 \\
 \frac{\partial h2}{\partial w4} = i2 \\
 \end{aligned}

 
 ```
 
```math 
\frac{\partial a\_h1}{\partial h1} = a\_h1 * (1-a\_h1) 
```

```math 
\frac{\partial E\_total}{\partial o1} = \frac{\partial E\_total}{\partial E1} * 
        \frac{\partial E1}{\partial a\_o1}  * \frac{\partial a\_o1}{\partial o1}
```

```math 
\frac{\partial E\_total}{a\_h1} = \frac{\partial E\_total}{o1} * \frac{\partial o1}{\partial a\_h1} + \frac{\partial E\_total}{o2} * \frac{\partial o2}{\partial a\_h1} 
```

```math 
\begin{aligned}
\frac{\partial E\_total}{\partial w1} = \frac{\partial E\_total}{\partial a\_h1} * \frac{\partial a\_h1}{\partial h1} * \frac{\partial h1}{\partial w1} \\
\frac{\partial E\_total}{\partial w4} = \frac{\partial E\_total}{\partial a\_h2} * \frac{\partial a\_h2}{\partial h2} * \frac{\partial h2}{\partial w4} 
\end{aligned}
```




