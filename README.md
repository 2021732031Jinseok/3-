## P3.1 풀이
## (a) 상태변수 설정
$$
x_1 = y,  \quad   x_2 = \dot{y}
$$

(따라서 출력은 \( y = x_1 \))

---

## 🧮 (b) 상태방정식 (벡터형)

$$
\begin{aligned}
\dot{x}_1 &= x_2 \\
\dot{x}_2 &= -\frac{\dot{k}}{M}x_1 - \frac{b}{M}x_2 + \frac{1}{M}u
\end{aligned}
$$

즉,

$$
\boxed{
\dot{\mathbf{x}} =
\underbrace{\begin{bmatrix}
0 & 1 \\[3pt]
-\tfrac{k}{M} & -\tfrac{b}{M}
\end{bmatrix}}_{A}
\mathbf{x} +
\underbrace{\begin{bmatrix} 0 \\[3pt] \tfrac{1}{M} \end{bmatrix}}_{B} u,
\quad
y =
\underbrace{\begin{bmatrix} 1 & 0 \end{bmatrix}}_{C} \mathbf{x} +
\underbrace{[\,0\,]}_{D}u
}
$$

---

## 🧩 (c) 상태미분방정식 (스칼라형)

$$
\boxed{
\begin{aligned}
\dot{x}_1(t) &= x_2(t) \\
\dot{x}_2(t) &= -\frac{k}{M}x_1(t) - \frac{b}{M}x_2(t) + \frac{1}{M}u(t) \\
y(t) &= x_1(t)
\end{aligned}
}
$$

---

## 📈 (d) 전달함수

출력 \( y \), 입력 \( u \) 에 대한 전달함수:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{1}{M s^2 + b s + k}
$$

---

## 💡 참고

- 이 상태공간 표현은 SISO(단일 입력 단일 출력) 2차 시스템의 **표준 형태**입니다.  
- 다른 상태변수 선택(예: \( x_1 = y, x_2 = M\dot{y} \))도 가능하지만, 위 형태가 가장 일반적으로 사용됩니다.
