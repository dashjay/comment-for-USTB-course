**概念**

1. 两个整数$a, b$，其最大公因数和最小公倍数的关系为$ab=[a,b](a,b)$
2. 给定一个正整数m，两个整数a, b叫做模m同余，如果 $m|a-b$，记作 $a\equiv b \pmod m$；否则，叫做模 m 不同余，记作 $a \not\equiv b \pmod m$
3. 设m，n是互素的两个正整数，则$\varphi(mn)=\varphi(m)\varphi(n)$。
4. 设 m > 1 整数，a 是与 m 互素的正整数。则使得 $a^e \equiv 1 \pmod m $成立的最小正整数 e 叫做 a 对 模 m 的指数。记作 $ord_m(a)$。如果 a 对模 m 的指数是 $\varphi(m)$，则 a 叫做 模m的 原根。
5. 设 n 是一个奇合数，设整数 b 与 n 互素，如果整数 n 和 b 满足条件 $b^{n-1} \equiv 1 \pmod n$ 则 n 叫做对于基b的拟素数。
6. 设 $G, G'$ 是两个群，f 是 $G$ 到 $G'$ 的一个映射，如果对任意 $a,b \in G$，都有 $f(ab)=f(a)f(b)$，那么 $f$ 叫做 $G$ 到 $G'$ 的一个同态
7. 加群 Z 每个子群 H 都是 **循环群**，并且由 $H=<0>$ 或者 $H=<m>$。
8. 我们称交换环 R 为一个域，如果 R 对于加法构成一个**交换**群，$R'=\frac{R}{\{0\}}$ 对于乘法构成一个交换群。

**eg（证明构成群）.** 设 m 是大于1的正整数，记 $U(m)=\{\bar{a} \in Z_m | (a,m)=1\}$，则 $U(m)$ 关于剩余类的乘法构成群。

证：

（1）对任意的 $\bar{a},\bar{b} \in U(m)$，有 $(a, m)=1, (b, m)=1$,于是$(ab, m)=1$，从而 $\overline{ab} \in U(m)$。所以剩余类乘法 "$\cdot$" **是$U(m)$的代数运算。**

（2）对任意 $\bar{a}, \bar{b}, \bar{c} \in U(m)$，有$$(\bar{a} \cdot\bar{b}) \cdot \bar{c}=\overline{ab} \cdot \overline{c}=\overline{(ab)c}=\overline{a(bc)}=\bar{a}\cdot \overline{bc}=\bar{a}\cdot(\bar{b}\cdot\bar{c})$$

所以**结合律**成立。

（3）因为 $(1,m)=1$，从而 $\bar{1} \in Z_m$。对任意的 $\bar{a} \in U(m)$有

$$\bar{a} \cdot \bar{1}=\overline{a\cdot1}=\bar{a}$$，且

$$\bar{1} \cdot \bar{a}=\overline{1 \cdot a}=\bar{a}$$

所以 1 是 $U(m)$ 的**单位元**

（4）对 $\forall{\bar{a}} \in U(m)$，有 $(a, m)=1$，由证书的性质可知。存在 $u,v \in Z$，使 $au + mv=1$，显然 $(u, m)=1$，所以 $\bar{u} \in U(m)$，且

$$\bar{a} \cdot \bar{u}=\overline{au}=\overline{au+mv}=\bar{1}$$

$$\bar{u} \cdot \bar{a}=\overline{ua}=\overline{au}=1$$

所以 $\bar{u}$ 为 $\bar{a}$ 的逆元。**从而，$U(m)$的每个元素在$U(m)$中都可逆**，就证明了$U(m)$关于剩余类的**乘法构成群**。

**eg（证明素理想）** 设 $p$ 是素数，则 $P=(p)$ 是整数环 Z 的素理想。

证：

对任意 $a,b $，若 $ab \in P = (P)$ ，则 $p|ab$。

于是 $p|a$ 或 $p|b$。

因此得到，$a \in P$ 或 $b \in P$。

因此，$P=(p)$ 是整数环 $Z$ 的素理想。

**eg（证明原根）** 设 p 是一个奇素数，并且 $\frac{p-1}{2}$ 也是一个奇素数设 a 是与 p 互素的正整数，如果 $a\neq1, a^2 \neq 1, a^{\frac{p-1}{2}} \neq 1 \pmod p$ 则a是模 p 的原根。

证：a 的指数等于 p-1，也就是满足 $a^{p-1} \equiv 1 \pmod p$ 的 p-1 是最小的。

假设存在整数 $X < p-1, st(a^x) \equiv 1 \pmod p$，因为 $\frac{p-1}{2}$ 为奇素数，$p-1=\frac{p-1}{2} \times 2$

因为 $a \neq 1, a^{\frac{p-1}{2}} \neq 1 \pmod p$ 所以 x 不存在，即 p-1 为最小。

**eg（解二次剩余）**求所有素数 p 使得 5 为模 p 的二次剩余

解：求所有素数 P， $st(\frac{5}{p})=1$，易知，P 是大于 5 的素数，根据二次互反律 $\frac{5}{p}=(-1)(\frac{p-1}{2})(\frac{5-1}{2})(\frac{p}{5})=\frac{5}{p}$

$$(\frac{p}{5})=(\frac{1}{5})=1, p=1 \pmod 5 \\ (\frac{2}{5})=1, p=2 \pmod 5 \\(\frac{3}{5})=1, p=3 \pmod 5 \\(\frac{-1}{5})=1, p=-1 \pmod 5$$

所以 $P \equiv 1 \pmod 5$ 或者 $P \equiv -1 \pmod 5$

**eg（求方程的解）** 求满足方程 $E: y^2=x^3+2x+1 \pmod 7$ 的所有点。

解对 $x=0,1,2,3,4,5,6$ 分别求出 y。

$x=0, y^2 \equiv1 \pmod 7, y \equiv 1,6 \pmod 7$

$x=1,y^2 \equiv 4 \pmod 7, y \equiv 2,5 \pmod 7$

$x=2 ,y^2 \equiv 6 \pmod 7 $ 无解

$x=3 ,y^2 \equiv 6 \pmod 7 $ 无解

$x=4 ,y^2 \equiv 3 \pmod 7 $ 无解

$x=5 ,y^2 \equiv 3 \pmod 7 $ 无解

$x=6 ,y^2 \equiv 5 \pmod 7 $ 无解

**eg（雅克比符号同余方程是否有解）** 判断同余式 $x^2 \equiv 286 \pmod {563}$ 是否有解。

$\frac{286}{563}=(\frac{2}{563})(\frac{143}{563})=(-1)^{\frac{563^2-1}{8}}(-1)^{\frac{143-1}{2} \cdot \frac{563-1}{2}}(\frac{563}{143})=\frac{-9}{143}=\frac{-1}{143}=-1$

**eg（求同余方程的解）** 求出下列一次同余数的所有解 $6x \equiv 3 \pmod 9$

解：

（1）求同余式 $6x \equiv 3 \pmod 9$ 的解，运用广义欧几里得除法得：$x \equiv 5 \pmod 3$

（2）求同余式 $6x \equiv 3 \pmod 9$ 的一个特解：$x \equiv 5 \pmod 3$

（3）写出同余式 $6x \equiv 3 \pmod 9$ 的全部解：

$X \equiv 5 + 3t \pmod 9 (t=0,1,2)$

**eg（求解一次同余方程）**$17x=14 \pmod {21}$

$\because (17,21)=1 | 14$ ，$\therefore$ 原式有解

又 $\because 17x \equiv 1 \pmod {21}$ ，$\therefore x_0 \equiv 5 \pmod {21}$。

同余式 $17x=14 \pmod {21}$ 的一个特解为 $x_0 \equiv 14 \times x_0=14 \times 5 \equiv 7 \pmod {21}$

所有的解为 $x \equiv 7 \pmod {21}$

**eg（解同余方程组）**
$$
\begin{cases}
x \equiv 2 \pmod 3 \\
x \equiv 3 \pmod 5 \\
x \equiv 2 \pmod 7
\end{cases}
$$

令 $m_1 =3, m_2=5, m_3=7, m=3 \times 5 \times 7 = 105$

$M_1=5 \times 7=35, M_2 = 3 \times 7 = 21 M_3 = 3 \times 5 = 15$

分别求解 $M'_iM_i \equiv 1 \pmod{m_i}(i=1,2,3)$  

得到 $M_1'=2, M_2'=1, M_3'=1$ 所以同余式的解为
$x \equiv M_1'M1 \times 2 + M_2'M_2 \times 3+M_3'M_3 \times 2 \pmod {105} \\ \ \ \equiv 23 \pmod{105}$

**eg（广义欧几里得算法）** 令 $a=1613, b=3589$。用欧几里得算法求整数 $s, t$ 是的 $sa + tb = (a,b)$。
$$
3589=2 \times 1613 + 363 \\1613=4 \times 363 + 161 \\ 363 = 2 \times 161 + 41 \\ 161 = 3 \times 41 + 38 \\ 41=1 \times 38 + 3 \\ 38 = 12 \times 3 + 2 \\ 3 = 1 \times 2 + 1 \\ 2 = 2 \times 1
$$

$(a,b)=1$，从而
$$
1=3-1 \times 2 \\
= 3 -1 \times(38-12\times3)\\
=-38+13 \times(41-1 \times 38) \\
= 13 \times 41 -14 \times (161 - 3 \times 41) \\
= -14 \times161 +55 \times (363-2 \times 161) \\
= 551 \times 3589 + (-1226) \times 1613 \\
\therefore s=-1226, t=551
$$

**eg（一元二次同余式的解数）** 求同余方程 $x^2 \equiv -1 \pmod {67}$ 的解数。
$$
(\frac{-2}{67})=(\frac{65}{67}) \\
=(\frac{13}{67})(\frac{5}{67}) \\
= (-1)^{12\times\frac{66}{4}}(-1)^{4\times \frac{66}{4}}(\frac{2}{13})(\frac{2}{5}) \\
= 1 \times 1 \times (-1)^{\frac{13 \times 13-1}{8}})(-1)^{\frac{5\times5 -1}{8}}
= -1 \times (-1) = 1
$$

$\therefore -2$ 是 $67$ 的二次剩余

$\therefore x^2 \equiv -2 \pmod {67}$ 有两个解

**eg（指数ord）** 计算 3 模 19 的指数 $ord_{19}(3)$。

$\because \varphi(19)=18, \therefore$ 只需要对 18 的因数 $d=1,2,3,6,9,18$ 计算 $a^d \pmod {19}$

$\because 3^1 \equiv 3 , e^2 \equiv 9, 3^3 \equiv 8, 3^6 \equiv 7, 3^9 \equiv -1, 2^{18} \equiv 1 \pmod{19}$

所以 3 模 19 的指数为18。

**eg（整除证明）** 如果 a 是整数，则 $a^3-a$能被6整除。

证
$$
\because a^3-a=(a-1)\cdot a\cdot(a+1) \\
当 a = 3k,\  k \in Z,\  3|a,\ 则 3 |a^3-a \\
当 a = 3k-1,\ k \in Z,\ 3|(a+1),\ 则 3|a^3-a \\
当 a = 3k+1,\ k \in Z,\ 3|(a-1),\ 则 3|a^3 -a \\
所以 a^3 -a 能被 3 整除，又 \because (a-1),\ a,\ (a+1)\ 是3个连续的整数，所以至少有一个是偶数，\\
从而 2 | a^3 -a。因此， a^3-a 能被6整除
$$
**eg（正规子群）** $f$ 是群 $G$ 到$G'$ 的一个同态，$kerf=\{a|a \in G, f(a)=e'\}$，其中$e'$是$G'$的单位元。

证明：$kerf$ 是 G 的正规子群。

证：$\forall a., b \in kerf$，有$f(a)=e',f(b)=e'$，从而$f(ab^{-1})=f(a)f(b^{-1})=f(a)f(b)^{-1}=f(a)f(a)^{-1}=e'$。

因此，$b \in kerf$，$kerf$ 是群 G 的子群，对 $\forall a \in G, b \in kerf$，我们有 $f(aba^{-1})=f(a)f(b)f(a^{-1})=f(a)\cdot e\cdot f(a)^{-1}=f(a)f(a)^{-1}=e'$。这说明 $aba^{-1} \in kerf$。从而，$ker f$ 是群 G的正规子群

**eg（证明）** 如果 p 和 q 是不同素数，则$p^{q-1} + q^{p-1} \equiv 1 \pmod{pq}$
$$
\because (p,q)=1,\ p,q\ 都是素数，\therefore \varphi(p)=p-1,\ \varphi(q)=q-1 \\
由 Euler 定理知：p^{\varphi(q)} \equiv1 \pmod q,\ \ q ^{\varphi(p)} \equiv1 \pmod p \\
即 p^{q-1} \equiv 1 \pmod q,\ \ q^{p-1} \equiv 1 \pmod p \\
又 q^{p-1} \equiv 0 \pmod q,\ \ p^{q-1} \equiv 0 \pmod p \\
\therefore p^{q-1} + q^{p-1} \equiv 1 \pmod q,\ \ q^{p-1}+p^{q-1} \equiv 1 \pmod p \\
又 \because [p,q]=pq,\ \ \therefore p^{q-1}+q^{p-1} \equiv 1 \pmod{pq}
$$

**eg（RSA）** RSA公钥加密算法的秘钥生成步骤如下：选择两个大素数 $p$ 和 $q$ ，计算 $n = pq$，选择两个正整数 $e$ 和 $d$，满足： $ed=1 \pmod{\varphi(n)}$。BOb的公钥是 $(n,e)$，对外公布。Bob的私钥是 $d$，自己私藏。如果攻击者分解 $n$ 得到 $p=47, q=23$，并且一直 $e=257$，试求出 Bob 的私钥 d。

解：$p=47, q=23, n=pq=1081$，要求 Bob 的私钥 d，即解同余式 $257d=1\pmod{1012}$

利用欧几里得算法解得改同余式的解为 $949$。所以Bob的私钥是$d=949$。



**eg（求同余式）**

$1997^{365 \pmod{15}}$

解：
$$
(133\times15+2)^{365} \pmod {15} \\
2^{365} \pmod {15} \\
\varphi(15)=8,根据欧拉定律 2^8 \equiv 1 \pmod {15} \\
2^{365} \equiv 2^{45\times8\times5} \equiv2^5 \equiv 2 \pmod {15}
$$
