# Решение домашних домашнего задания по Методам оптимизации

## ДЗ1

> Учебник Демидовича. Из каждого диопазона по 5 задач:
>
> - 3626-3647
> - 3658-3665
> - 3690-3708<br>

### Блок 1

#### № 3626

Исследование функции $ z = x^3 + y^3 - 3xy $ на экстремум

Вычислим частные производные первого порядка

$$
\frac{\partial z}{\partial x} = 3x^2 - 3y, \quad \frac{\partial z}{\partial y} = 3y^2 - 3x
$$

Найдём стационарные точки, для этого решим систему:

$$
\begin{cases}
3x^2 - 3y = 0 \\
3y^2 - 3x = 0
\end{cases}
\Rightarrow
\begin{cases}
y = x^2 \\
x = y^2
\end{cases}
\Rightarrow
\begin{cases}
y = x^2 \\
x(x^3 - 1) = 0
\end{cases}
$$

Получаем две стационарные точки:

$$
P_0(0, 0);\quad P_1(1, 1)
$$

Вычислим частные производные второго порядка

$$
\frac{\partial^2 z}{\partial x^2}=6x
,\quad
\frac{\partial^2 z}{\partial x\partial y}=-3
,\quad
\frac{\partial^2 z}{\partial y^2}=6y
$$

Таким образом, матрица квадратичной формы равна

$$
A =
\begin{pmatrix}
6x & -3 \\
-3 & 6y
\end{pmatrix}
$$

Вычислим главные миноры:

$$
\Delta_1 = 6x
,\quad
\Delta_2 = 36xy-9
$$

В точке $ (0, 0) $ получаем:

$$
\Delta_1 = 0
,\quad
\Delta_2 = -9 < 0
$$

Квадратичная форма не определена $\Rightarrow$ в точке $(0, 0)$ экстремума нет

В точке $ (1, 1) $ получаем:

$$
\Delta_1 = 6 > 0
,\quad
\Delta_2 = 27 > 0
$$

Квадратичная положительно определена $\Rightarrow$ $(1, 1)$ это точка минимума

Значение функции в этой точке:

$$
z(1,1) = -1
$$

Ответ:

- Минимум $ z = -1 $ при $ x = 1,\ y = 1 $
- Экстремума нет при $ x = 0,\ y = 0$

#### № 3627

Исследование функции $ z = x^4 + y^4 - x^2 - 2xy - y^2 $ на экстремум

Вычислим частные производные первого порядка

$$
\frac{\partial z}{\partial x} = 4x^3 - 2x - 2y, \quad \frac{\partial z}{\partial y} = 4y^3 - 2x - 2y
$$

Найдём стационарные точки, для этого решим систему:

$$
\begin{cases}
4x^3 - 2x - 2y = 0 \\
4y^3 - 2x - 2y = 0
\end{cases}
$$

Вычтем второе уравнение из первого:

$$
4x^3 - 4y^3 = 0 \implies x^3 = y^3 \implies x = y
$$

Подставим $x = y$ в первое уравнение:

$$
4x^3 - 4x = 0 \implies 4x(x^2 - 1) = 0
$$

Получаем три стационарные точки:

$$
P_0(0, 0);\quad P_1(1, 1);\quad P_2(-1, -1)
$$

Вычислим частные производные второго порядка

$$
\frac{\partial^2 z}{\partial x^2} = 12x^2 - 2
,\quad
\frac{\partial^2 z}{\partial x\partial y} = -2
,\quad
\frac{\partial^2 z}{\partial y^2} = 12y^2 - 2
$$

Таким образом, матрица квадратичной формы равна

$$
A =
\begin{pmatrix}
12x^2 - 2 & -2 \\
-2 & 12y^2 - 2
\end{pmatrix}
$$

Вычислим главные миноры:

$$
\Delta_1 = 12x^2 - 2
,\quad
\Delta_2 = (12x^2 - 2)(12y^2 - 2) - 4
$$

В точке $ (0, 0) $ получаем:

$$
\Delta_1 = -2 < 0
,\quad
\Delta_2 = (-2)(-2) - 4 = 0
$$

Квадратичная форма не определена $\Rightarrow$ в точке $(0, 0)$ экстремума нет

В точке $ (1, 1) $ получаем:

$$
\Delta_1 = 10 > 0
,\quad
\Delta_2 = 10 \cdot 10 - 4 = 96 > 0
$$

Квадратичная форма положительно определена $\Rightarrow$ $(1, 1)$ это точка минимума.

Значение функции в этой точке:

$$
z(1,1) = -2
$$

В точке $ (-1, -1) $ получаем:

$$
\Delta_1 = 10 > 0
,\quad
\Delta_2 = 10 \cdot 10 - 4 = 96 > 0
$$

Квадратичная форма положительно определена $\Rightarrow$ $(-1, -1)$ это точка минимума.

Значение функции в этой точке:

$$
z(-1,-1) = -2
$$

Ответ:

- Минимум $ z = -2 $ при $ x = 1,\ y = 1 $ и $ x = -1,\ y = -1 $
- Экстремума нет при $ x = 0,\ y = 0 $

#### № 3628

Исследование функции $ z = xy + \frac{50}{x} + \frac{20}{y} $ на экстремум при $x>0$, $y>0$

Вычислим частные производные первого порядка:

$$
\frac{\partial z}{\partial x} = y - \frac{50}{x^2}, \quad \frac{\partial z}{\partial y} = x - \frac{20}{y^2}
$$

Найдём стационарные точки, решая систему:

$$
\begin{cases}
y - \dfrac{50}{x^2} = 0 \\\\
x - \dfrac{20}{y^2} = 0
\end{cases}
\Rightarrow
\begin{cases}
y = \dfrac{50}{x^2} \\\\
x = \dfrac{20}{y^2}
\end{cases}
$$

Подставим первое уравнение во второе:

$$
x = \frac{20}{\left(\frac{50}{x^2}\right)^2} = \frac{20x^4}{2500} = \frac{x^4}{125}
$$

Получаем:

$$
x^4 - 125x = 0 \Rightarrow x(x^3 - 125) = 0
$$

Учитывая $x>0$, имеем единственное решение:

$$
x = 5 \Rightarrow y = \frac{50}{25} = 2
$$

Стационарная точка:

$$
P(5, 2)
$$

Вычислим частные производные второго порядка:

$$
\frac{\partial^2 z}{\partial x^2} = \frac{100}{x^3},\quad \frac{\partial^2 z}{\partial x\partial y} = 1,\quad \frac{\partial^2 z}{\partial y^2} = \frac{40}{y^3}
$$

Матрица квадратичной формы в точке $(5,2)$:

$$
A = \begin{pmatrix}
\dfrac{100}{125} & 1 \\\\
1 & \dfrac{40}{8}
\end{pmatrix}
= \begin{pmatrix}
0.8 & 1 \\
1 & 5
\end{pmatrix}
$$

Главные миноры:

$$
\Delta_1 = 0.8 > 0,\quad \Delta_2 = 0.8 \cdot 5 - 1 \cdot 1 = 4 - 1 = 3 > 0
$$

Квадратичная форма положительно определена $\Rightarrow$ точка $(5,2)$ является точкой минимума.

Значение функции в этой точке:

$$
z(5,2) = 5 \cdot 2 + \frac{50}{5} + \frac{20}{2} = 10 + 10 + 10 = 30
$$

Ответ:

- Минимум $ z = 30 $ при $ x = 5,\ y = 2 $

#### № 3631

Исследование функции $ z = 1 - \sqrt{x^2 + y^2} $ на экстремум

Вычислим частные производные первого порядка:

$$
\frac{\partial z}{\partial x} = -\frac{x}{\sqrt{x^2 + y^2}}, \quad \frac{\partial z}{\partial y} = -\frac{y}{\sqrt{x^2 + y^2}}
$$

Найдём стационарные точки, решая систему:

$$
\begin{cases}
-\dfrac{x}{\sqrt{x^2 + y^2}} = 0 \\\\
-\dfrac{y}{\sqrt{x^2 + y^2}} = 0
\end{cases}
$$

Система имеет единственное решение:

$$
x = 0, \quad y = 0
$$

Проверим поведение функции в точке (0,0):

Вычислим вторые частные производные:

$$
\frac{\partial^2 z}{\partial x^2} = -\frac{y^2}{(x^2 + y^2)^{3/2}}
$$

$$
\frac{\partial^2 z}{\partial y^2} = -\frac{x^2}{(x^2 + y^2)^{3/2}}
$$

$$
\frac{\partial^2 z}{\partial x \partial y} = \frac{xy}{(x^2 + y^2)^{3/2}}
$$

Получаем матрицу квадратичной формы:

$$
A =
\begin{pmatrix}
-\dfrac{y^2}{(x^2 + y^2)^{3/2}} & \dfrac{xy}{(x^2 + y^2)^{3/2}} \\\\
\dfrac{xy}{(x^2 + y^2)^{3/2}} & -\dfrac{x^2}{(x^2 + y^2)^{3/2}}
\end{pmatrix}
$$

Вычислим главные миноры:

$$
\Delta_1 = -\dfrac{y^2}{(x^2 + y^2)^{3/2}}<0
,\quad
\Delta_2 = \frac{y^2 x^2 - x^2 y^2}{(x^2 + y^2)^3}=0
$$

Таким образом сделать выводы на основе миноров невозможно. Исследуем поведение функции в окрестности точки $(0,0)$.

Можно заметить, что функции убывает при удалнее от точки $(0,0)$ так как значение $\sqrt{x^2 + y^2}$ возрастает. Таким образом $(0, 0)$ это точка максимума.

Значение функции в этой точке:

$$
z(0,0) = 1
$$

Ответ:

- Максимум $ z = 1 $ при $ x = 0 $, $ y = 0 $

#### № 3635

Исследование функции $z = x^2 + xy + y^2 - 4\ln{x} - 10\ln{y}$ на экстремум

Вычислим частные производные первого порядка:

$$
\frac{\partial z}{\partial x} = 2x + y - \frac{4}{x}, \quad \frac{\partial z}{\partial y} = x + 2y - \frac{10}{y}
$$

Найдём стационарные точки, решая систему:

$$
\begin{cases}
2x + y = \dfrac{4}{x} \\\\
x + 2y = \dfrac{10}{y}
\end{cases}
$$

Из первого уравнения:

$$
y = \frac{4}{x} - 2x
$$

Подставим во второе:

$$
x + 2\left(\frac{4}{x} - 2x\right) = \frac{10}{\dfrac{4}{x} - 2x}
$$

После преобразований получаем биквадратное уравнение:

$$
3x^4-19x^2+16=0
$$

Решае его полчаем следующие равенства:

$$
\begin{cases}
x^2=1 \\\\
x^2 = \dfrac{16}{3}
\end{cases}
$$

Исключая отрицательные корни, получаем единственное решение:

$$
x=1,\quad y=2
$$

Стационарная точка:

$$
P(1, 2)
$$

Вычислим частные производные второго порядка:

$$
\frac{\partial^2 z}{\partial x^2} = 2 + \frac{4}{x^2}, \quad \frac{\partial^2 z}{\partial y^2} = 2 + \frac{10}{y^2}, \quad \frac{\partial^2 z}{\partial x \partial y} = 1
$$

Квадратичная форма в точке $(1, 2)$ имеет вид:

$$
A = \begin{pmatrix}
6 & 1 \\
1 & 4.5
\end{pmatrix}
$$

Главные миноры:

$$
   \Delta_1 = 6 > 0, \quad \Delta_2 = 26 > 0
$$

Значит квадратичная форма положительно определена, и точка $(1, 2)$ это точка минимума.

Значение функции в этой точке:

$$
  z(1,2) = 7 - 10\ln{2} ≈ 0.0685
$$

Ответ:

- Локальный минимум $z ≈ 0.0685$ при $x = 1,\ y = 2$

### Блок 2

#### № 3658

Исследование функции $ z = \cos^2x + \cos^2y $ при условии $ x - y = \frac{\pi}{4} $

Запишем функцию Лагранжа:

$$
\mathcal{L}(x,y,\lambda) = \cos^2x + \cos^2y + \lambda\left(x - y - \frac{\pi}{4}\right)
$$

Вычислим частные производные и приравняем их к нулю:

$$
\begin{cases}
\dfrac{\partial\mathcal{L}}{\partial x} = -2\cos x\sin x + \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial y} = -2\cos y\sin y - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial\lambda} = x - y - \dfrac{\pi}{4} = 0
\end{cases}
$$

Упростим систему, используя тождество $\sin 2x = 2\sin x\cos x$:

$$
   \begin{cases}
   -\sin 2x + \lambda = 0 \\
   -\sin 2y - \lambda = 0 \\
   x - y = \frac{\pi}{4}
   \end{cases}
$$

Сложим первые два уравнения:

$$
-\sin 2x - \sin 2y = 0 \Rightarrow \sin 2x = -\sin 2y
$$

Используем тождество $\sin A = -\sin B \Rightarrow A = -B + 2\pi n$ или $A = \pi + B + 2\pi n$:

$$
2x = -2y + 2\pi n \quad \text{или} \quad 2x = \pi + 2y + 2\pi n
$$

Рассмотрим оба случая с учетом условия $x - y = \frac{\pi}{4}$:

a) $x = -y + \pi n$:

$$
(-y + \pi n) - y = \frac{\pi}{4} \Rightarrow -2y = \frac{\pi}{4} - \pi n \Rightarrow y = -\frac{\pi}{8} + \frac{\pi n}{2}
$$

$$
x = \frac{\pi}{8} + \frac{\pi n}{2}
$$

b) $x = \frac{\pi}{2} + y + \pi n$:

$$
\left(\frac{\pi}{2} + y + \pi n\right) - y = \frac{\pi}{4} \Rightarrow \frac{\pi}{2} + \pi n = \frac{\pi}{4}
$$

Это уравнение не имеет решений при целых n.

7. Таким образом, критические точки:

   $$
   x = \frac{\pi}{8} + \frac{\pi n}{2}, \quad y = -\frac{\pi}{8} + \frac{\pi n}{2}, \quad n \in \mathbb{Z}
   $$

8. Вычислим значения функции в этих точках:
   $$
   z = \cos^2\left(\frac{\pi}{8} + \frac{\pi n}{2}\right) + \cos^2\left(-\frac{\pi}{8} + \frac{\pi n}{2}\right)
   $$

Для n = 0:

$$
z = \cos^2\frac{\pi}{8} + \cos^2\frac{\pi}{8} = 2\cos^2\frac{\pi}{8} = 1 + \cos\frac{\pi}{4} = 1 + \frac{\sqrt{2}}{2}
$$

Для n = 1:

$$
z = \cos^2\left(\frac{5\pi}{8}\right) + \cos^2\left(\frac{3\pi}{8}\right) = \sin^2\frac{3\pi}{8} + \cos^2\frac{3\pi}{8} = 1
$$

9. Анализ экстремумов:
   Максимальное значение достигается при n четных: $1 + \frac{\sqrt{2}}{2}$
   Минимальное значение 1 достигается при n нечетных.

Ответ:

- Максимум $ z = 1 + \frac{\sqrt{2}}{2} $ при $ x = \frac{\pi}{8} + \pi k $, $ y = -\frac{\pi}{8} + \pi k $
- Минимум $ z = 1 $ при $ x = \frac{5\pi}{8} + \pi k $, $ y = \frac{3\pi}{8} + \pi k $
  где $ k \in \mathbb{Z} $

#### № 3659

Исследование функции $u = x - 2y + 2z$ при ограничении $x^2 + y^2 + z^2 = 1$ методом множителей Лагранжа

Составляем функцию Лагранжа:

$$
\mathcal{L}(x,y,z,\lambda) = x - 2y + 2z + \lambda(1 - x^2 - y^2 - z^2)
$$

Находим частные производные и приравниваем их к нулю:

$$
\begin{cases}
\dfrac{\partial\mathcal{L}}{\partial x} = 1 - 2\lambda x = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial y} = -2 - 2\lambda y = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial z} = 2 - 2\lambda z = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial\lambda} = 1 - x^2 - y^2 - z^2 = 0
\end{cases}
$$

Из первых трех уравнений выражаем переменные:

$$
x = \frac{1}{2\lambda},\quad y = -\frac{1}{\lambda},\quad z = \frac{1}{\lambda}
$$

Подставляем в уравнение ограничения:

$$
\left(\frac{1}{2\lambda}\right)^2 + \left(-\frac{1}{\lambda}\right)^2 + \left(\frac{1}{\lambda}\right)^2 = 1
$$

$$
\frac{1}{4\lambda^2} + \frac{1}{\lambda^2} + \frac{1}{\lambda^2} = 1
$$

$$
\frac{9}{4\lambda^2} = 1 \implies \lambda = \pm\frac{3}{2}
$$

Получаем две критичекие точки:

$$
\lambda = \frac{3}{2}\quad P_1 = \left(\frac{1}{3}, -\frac{2}{3}, \frac{2}{3}\right)
$$

$$
\lambda = -\frac{3}{2}\quad P_2 = \left(-\frac{1}{3}, \frac{2}{3}, -\frac{2}{3}\right)
$$

Запишем матрицу Гессе из вторых производных:

$$
A = \begin{pmatrix}
-2\lambda & 0 & 0 \\
0 & -2\lambda & 0 \\
0 & 0 & -2\lambda
\end{pmatrix}
$$

Миноры:

$$
\Delta_1 = -2\lambda
,\quad
\Delta_2 = 4\lambda^2
,\quad
\Delta_2 = -8\lambda^3
$$

В точке $P_1$ получаем:

$$
\Delta_1 = -3 < 0
,\quad
\Delta_2 = 9 > 0
,\quad
\Delta_2 = -27 < 0
$$

Квадратичная форма отрицательно определена, значит $P_1$ это точка максимума

Значение функции в это точке:

$$
u = 3
$$

В точке $P_2$ получаем:

$$
\Delta_1 = 3 > 0
,\quad
\Delta_2 = 9 > 0
,\quad
\Delta_2 = 27 > 0
$$

Квадратичная форма положительно определена, значит $P_2$ это точка минимума

Значение функции в это точке:

$$
u = -3
$$

Ответ:

- Максимум: $u = 3$ в точке $\left(\dfrac{1}{3}, -\dfrac{2}{3}, \dfrac{2}{3}\right)$

- Минимум: $u = -3$ в точке $\left(-\dfrac{1}{3}, \dfrac{2}{3}, -\dfrac{2}{3}\right)$

#### № 3660

Исследование функции $u = x^my^nz^p$ при ограничении $x + y + z = a$ методом множителей Лагранжа $(m,n,p,a > 0)$

Функция Лагранжа:

$$
\mathcal{L}(x,y,z,\lambda) = x^m y^n z^p + \lambda(a - x - y - z)
$$

Система уравнений:

$$
\begin{cases}
\dfrac{\partial\mathcal{L}}{\partial x} = m x^{m-1} y^n z^p - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial y} = n x^m y^{n-1} z^p - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial z} = p x^m y^n z^{p-1} - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial\lambda} = a - x - y - z = 0
\end{cases}
$$

Из первых трех уравнений получаем соотношения:

$$
\frac{m}{x} = \frac{n}{y} \Rightarrow y = \frac{n}{m}x
$$

$$
\frac{m}{x} = \frac{p}{z} \Rightarrow z = \frac{p}{m}x
$$

Подставляем в ограничение:

$$
x + \frac{n}{m}x + \frac{p}{m}x = a \Rightarrow x\left(1 + \frac{n}{m} + \frac{p}{m}\right) = a
$$

$$
x = \frac{a m}{m + n + p}, \quad y = \frac{a n}{m + n + p}, \quad z = \frac{a p}{m + n + p}
$$

Матрица Гессе:

$$
H = \begin{pmatrix}
m(m-1)x^{m-2}y^nz^p & mn x^{m-1}y^{n-1}z^p & mp x^{m-1}y^nz^{p-1} \\\\
mn x^{m-1}y^{n-1}z^p & n(n-1)x^m y^{n-2}z^p & np x^m y^{n-1}z^{p-1} \\\\
mp x^{m-1}y^nz^{p-1} & np x^m y^{n-1}z^{p-1} & p(p-1)x^m y^n z^{p-2}
\end{pmatrix}
$$

Проверка миноров:

Для точки $(\frac{am}{S}, \frac{an}{S}, \frac{ap}{S})$, где $S = m+n+p$:

Главные миноры:

1. $\Delta_1 = m(m-1)x^{m-2}y^nz^p < 0$ (при $m < 1)
2. $\Delta_2 = mn(1-S)x^{2m-2}y^{2n-2}z^{2p} > 0$ (при S > 1)
3. $\Delta_3 = mnp(2-S)x^{3m-3}y^{3n-3}z^{3p-3} < 0$ (при S > 2)

Анализ экстремума:

- При $m+n+p > 1$ - точка является максимумом
- Значение функции в критической точке:
  $$
  u_{max} = \left(\frac{am}{S}\right)^m \left(\frac{an}{S}\right)^n \left(\frac{ap}{S}\right)^p = \frac{a^{S} m^m n^n p^p}{(m+n+p)^{S}}
  $$

Ответ:

- Максимум:
  $$u = \frac{a^{m+n+p} m^m n^n p^p}{(m+n+p)^{m+n+p}}$$
  достигается при
  $$x = \frac{a m}{m+n+p}, y = \frac{a n}{m+n+p}, z = \frac{a p}{m+n+p}$$

#### № 3661

Исследование функции $u = x² + y² + z²$ при ограничении $x²/a² + y²/b² + z²/c² = 1$ методом множителей Лагранжа $(a>b>c>0)$

ункция Лагранжа:

$$
\mathcal{L}(x,y,z,\lambda) = x^2 + y^2 + z^2 + \lambda\left(1 - \frac{x^2}{a^2} - \frac{y^2}{b^2} - \frac{z^2}{c^2}\right)
$$

Система уравнений:

$$
\begin{cases}
\dfrac{\partial\mathcal{L}}{\partial x} = 2x - \dfrac{2\lambda x}{a^2} = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial y} = 2y - \dfrac{2\lambda y}{b^2} = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial z} = 2z - \dfrac{2\lambda z}{c^2} = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial\lambda} = 1 - \dfrac{x^2}{a^2} - \dfrac{y^2}{b^2} - \dfrac{z^2}{c^2} = 0
\end{cases}
$$

Возможные критические точки :

$$
(\pm a,0,0)
,\quad
(0,\pm b,0)
,\quad
(0,0,\pm c)
$$

Матрица Гессе:

$$
A = \begin{pmatrix}
2 - \dfrac{2\lambda}{a^2} & 0 & 0 \\\\
0 & 2 - \dfrac{2\lambda}{b^2} & 0 \\\\
0 & 0 & 2 - \dfrac{2\lambda}{c^2}
\end{pmatrix}
$$

Для точек вида $(\pm a,0,0)$ получим:

$$
λ = a^2
\Rightarrow
A = \begin{pmatrix}
0 & 0 & 0 \\\\
0 & 2 - \dfrac{2a^2}{b^2} & 0 \\\\
0 & 0 & 2 - \dfrac{2a^2}{c^2}
\end{pmatrix}
$$

Так как $a > b$ и $a > c$, форма отрицательно определена и это точка максимума

Значение функции в этой точке:

$$
u(\pm a,0,0) = a^2
$$

Для точек вида $(0,\pm b,0)$ получаем что в них форма не определена.

В точках вида $(0,0,\pm c)$ получаем что форма положительно определена а значит это точки минимума.

Значение функции в этой точке:

$$
u(0,0,\pm c) = c^2
$$

Ответ:

- Минимум $u=c^2$ в точках вида $(0,0,\pm c)$
- Минимум $u=a^2$ в точках вида $(\pm a,0,0)$

#### № 3664

Исследование функции $u = sin x sin y sin z$ при ограничении $x + y + z = π/2$ методом множителей Лагранжа (x,y,z > 0)

Функция Лагранжа:

$$
\mathcal{L}(x,y,z,\lambda) = \sin x \sin y \sin z + \lambda\left(\frac{\pi}{2} - x - y - z\right)
$$

Система уравнений:

$$
\begin{cases}
\dfrac{\partial\mathcal{L}}{\partial x} = \cos x \sin y \sin z - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial y} = \sin x \cos y \sin z - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial z} = \sin x \sin y \cos z - \lambda = 0 \\\\
\dfrac{\partial\mathcal{L}}{\partial\lambda} = \frac{\pi}{2} - x - y - z = 0
\end{cases}
$$

Из первых трех уравнений получаем:

$$
\cos x \sin y \sin z = \cos y \sin x \sin z \Rightarrow \tan x = \tan y
$$

Аналогично

$$
\tan x = \tan z
$$

В интервале $(0, π/2)$ функция tan инъективна, поэтому:

$$
x = y = z
$$

Подставляем в ограничение:

$$
3x = \frac{\pi}{2} \Rightarrow x = y = z = \frac{\pi}{6}
$$

Матрица Гессе ограниченной задачи:

$$
A = \begin{pmatrix}
-\sin x \sin y \sin z & \cos x \cos y \sin z & \cos x \sin y \cos z \\\\
\cos x \cos y \sin z & -\sin x \sin y \sin z & \sin x \cos y \cos z \\\\
\cos x \sin y \cos z & \sin x \cos y \cos z & -\sin x \sin y \sin z
\end{pmatrix}
$$

В критической точке получаем:

$$
H = \begin{pmatrix}
-\dfrac{\sqrt{3}}{4} & \dfrac{1}{4} & \dfrac{1}{4} \\\\
\dfrac{1}{4} & -\dfrac{\sqrt{3}}{4} & \dfrac{1}{4} \\\\
\dfrac{1}{4} & \dfrac{1}{4} & -\dfrac{\sqrt{3}}{4}
\end{pmatrix}
$$

Вычислям миноры:

$$
\Delta_1 = -\frac{\sqrt{3}}{2} < 0
,\quad
\Delta_2 = \frac{1}{2} > 0
,\quad
\Delta_3 = -\frac{3\sqrt{3}}{16} + \frac{3}{16} < 0
$$

Получае что квадратичная форма отрицательно определена, а значит рассматриваемая точка это точка максимума.

Значение функции:

$$
u\left(\frac{\pi}{6}, \frac{\pi}{6}, \frac{\pi}{6}\right) = \sin^3\left(\frac{\pi}{6}\right) = \left(\frac{1}{2}\right)^3 = \frac{1}{8}
$$

Ответ:

- Максимум: $u = \dfrac{1}{8}$ достигается при $x = y = z = \dfrac{π}{6}$
