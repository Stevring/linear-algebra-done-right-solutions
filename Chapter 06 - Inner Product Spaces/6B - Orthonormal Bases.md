[TOC]

# Chapter 6: **Inner Product Spaces**

## _Exercise 1_

_(a)_
One can easily check that each of the four vectors has norm $\sin^2 \theta + \cos^2 \theta$, which equals $1$.
Moreover, we have

$$
\begin{aligned}
\langle (\cos\theta, \sin\theta), (-\sin\theta, \cos\theta) \rangle &= -\cos\theta \sin\theta + \sin\theta \cos\theta = 0\\\\
\langle (\cos\theta, \sin\theta), (\sin\theta, -\cos\theta) \rangle &= \cos\theta \sin\theta - \sin\theta \cos\theta = 0,
\end{aligned}
$$

which shows that they are orthogonal.

_(b)_
Clearly, for any $v$ and $u$ in $\mathbb{R}^2$ with $||v|| = ||u|| = 1$, we can write $v = (\cos \theta, \sin \theta)$ and $v = (\cos \alpha, \sin \alpha)$ for some angles $\theta$ and $\alpha$.
If $v, u$ is an orthonormal basis, then we must have

$$
0 = \langle v, u \rangle = \langle (\cos \theta, \sin \theta), (\cos \alpha, \sin \alpha) \rangle = \cos\theta \cos\alpha + \sin\theta \sin\alpha = \cos(\theta - \alpha).
$$

One solution is to take choose $\theta$ and $\alpha$ such that $\theta - \alpha = \frac{\pi}{2}$.
Then

$$
\begin{aligned}
(\cos \alpha, \sin \alpha) &= (\cos(\theta + \frac{\pi}{2}), \sin(\theta + \frac{\pi}{2}))\\\\
&= (\cos\theta \cos\frac{\pi}{2} - \sin\theta\sin\frac{\pi}{2}, \sin\theta \cos\frac{\pi}{2} + \sin\frac{\pi}{2} \cos\theta)\\\\
&= (-\sin\theta, \cos\theta).\\\\
\end{aligned}
$$

Which shows that $v, u$ is of the first form given in part (a).

## _Exercise 2_

The backward direction follows directly from 6.30.

Suppose

$$
||v||^2 = |\langle v, e_1 \rangle|^2 + \dots + |\langle v, e_m \rangle|^2. \tag{1}
$$

By 6.35 we can extend $e_1, \dots, e_m$ to an orthonormal basis $e_1, \dots, e_m, f_1, \dots, f_n$ of $V$.
Then, by 6.30, we have

$$
||v||^2 = |\langle v, e_1 \rangle|^2 + \dots + |\langle v, e_m \rangle|^2 + |\langle v, f_1 \rangle|^2 + \dots + |\langle v, f_n \rangle|^2. \tag{2}
$$

Subtracting (1) from (2) yields

$$
0 = |\langle v, f_1 \rangle|^2 + \dots + |\langle v, f_n \rangle|^2,
$$

showing that $\langle v, f_j \rangle = 0$ for each $j$.
From 6.30 again, we have

$$
v = \langle v, e_1 \rangle e_1 + \dots + \langle v, e_m \rangle e_m + \langle v, f_1 \rangle f_1 + \dots + \langle v, f_n \rangle f_n = \langle v, e_1 \rangle e_1 + \dots + \langle v, e_m \rangle e_m,
$$

which shows that $v \in \operatorname{span}(e_1, \dots, e_m)$.

## _Exercise 3_

Applying the Gram-Schmidt Procedure to the given basis, we get the following basis

$$
(1, 0, 0),\\:\frac{1}{\sqrt{2}}(0, 1, 1),\\:\frac{1}{\sqrt{2}}(0, -1, 1).
$$

As in the proof of 6.37, we see that the matrix of $T$ with respect to this basis is upper triangular.

## _Exercise 5_

Applying the Gram-Schmidt Procedure, we get the following basis

$$
1, \\: 2\sqrt{3}(x - \frac{1}{2}), \\: 6\sqrt{5}(x^2 - x + \frac{1}{6}).
$$

## _Exercise 6_

Let $D$ denote the differential operator.
Note that $D$ is already upper-triangular with respect to the standard basis of $\mathcal{P}_2{\mathbb{R}}$.
Therefore, by the same reasoning used in the proof of 6.37, $\mathcal{M}(D)$ is upper-triangular with respect to the basis found in Exercise 5.

## _Exercise 7_

Defining $\varphi(p) = p(\frac{1}{2})$ and $\langle p, q \rangle = \int_{0}^{1} p(x)q(x)\ dx$ and using the formula from 6.43 together with the basis found in Exercise 5, we find that

$$
q(x) = -15x^2 + 15x - \frac{3}{2}.
$$

## _Exercise 8_

Using the orthonormal basis found in Exercise 5 and the formula in 6.43, we get $q(x) = \frac{-24}{\pi^2}\left(x - \frac{1}{2}\right)$.

## _Exercise 9_

Suppose $v_1, \dots, v_m$ is a lienarly dependent list in $V$.
Let $k$ be the smallest integer such that $v_k \in \operatorname{span}(v_1, \dots, v_{k-1})$.
Then $v_1, \dots, v_{k-1}$ is linearly independent and we can apply the Gram-Schmidt Procedure to produce an orthonormal list $e_1, \dots, e_{k-1}$ whose span is the same.
Therefore $v_k \in \operatorname{span}(e_1, \dots, e_{k-1})$ and, by 6.30,

$$
v_k = \langle v_k, e_1 \rangle e_1 + \dots + \langle v_k, e_{k-1} \rangle e_{k-1}.
$$

But the right hand side is exactly what we subtract from $v_k$ when calculating $e_k$, hence the Gram-Schmidt Procedure cannot continue because we can't divide by $0$.
If, however, you discard $v_k$ (and every other vector to which happens the same thing), you end up producing an orthonormal basis whose span equals $\operatorname{span}(v_1, \dots, v_m)$.

## _Exercise 10_

Just apply the Gram-Schmidt Procedure once on $v_1, \dots, v_m$ to get the orthonormal an $e_1, \dots, e_m$.
Note that, if we switch the order of this list without relabeling the vectors, we still have $\operatorname{span}(v_1, \dots, v_j) = \operatorname{span}(e_1, \dots, e_j)$ for all $j \in \\{1, \dots, m\\}$, because the vectors themselves remain the same.
There $2^m$ such permutations.

## _Exercise 11_

Let $w \in V$.
Define $\varphi(v) = \langle v, w \rangle_1$ and $\psi(v) = \langle v, w \rangle_2$.
Since $\varphi(v) = 0$ if and only if $\psi(v) = 0$, it follows that $\operatorname{null} \varphi =\operatorname{null} \psi$.
By Theorem 1 in Chapter 3 notes we have

$$
\operatorname{span}(\varphi) = (\operatorname{null} \varphi)^0 = (\operatorname{null} \psi)^0 = \operatorname{span}(\psi).
$$

Thus $\varphi = c\psi$ for some $c \in \mathbb{F}$.
Hence, for each fixed $w$ we have $\langle v, w \rangle_1 = c\langle v, w \rangle_2$ for every $v \in V$.
Chosing $v = w$ now implies that $c$ is real and positive.
Fix $w_1, w_2 \in V$ and let $c_1, c_2 \in \mathbb{F}$ such that

$$
\begin{aligned}
\langle v, w_1 \rangle_1 &= c_1 \langle v, w_1 \rangle_2\\\\
\langle v, w_2 \rangle_1 &= c_2 \langle v, w_2 \rangle_2.\\\\
\end{aligned}
$$

Pluging $v = w_2$ in the first equation and $v = w_1$ in the second yields

$$
\begin{aligned}
\langle w_2, w_1 \rangle_1 &= c_1 \langle w_2, w_1 \rangle_2\\\\
\langle w_1, w_2 \rangle_1 &= c_2 \langle w_1, w_2 \rangle_2.\\\\
\end{aligned}
$$

Then

$$
c_1 \langle w_2, w_1 \rangle_2 = \langle w_2, w_1 \rangle_1 = \overline{\langle w_1, w_2 \rangle_1} = \overline{c_2 \langle w_1, w_2 \rangle_2} = \bar{c_2} \langle w_2, w_1 \rangle_2.
$$

Hence $c_1 = \bar{c_2}$.
Because both are real, it follows that $c_1 = c_2$.
Therefore, the constant is the same for all $v, w \in V$.

## _Exercise 17_

_(a)_
For additivity, suppose $u_1, u_2 \in V$.
Then, for $v \in V$, we have

$$
(\Phi(u_1 + u_2))(v) = \langle v, u_1 + u_2 \rangle = \langle v, u_1 \rangle + \langle v, u_2 \rangle = (\Phi u_1)(v) + (\Phi u_2)(v).
$$

For homogeneity, suppose $u \in V$ and $c \in \mathbb{R}$.
Then, for $v \in V$, we have

$$
(\Phi(cu))(v) = \langle v, cu \rangle = c\langle v, u \rangle = c(\Phi u)(v).
$$

_(b)_
If $\mathbb{F} = \mathbb{C}$, then the homogeneity property of linear maps is not satisfied, because we would have $(\Phi(cu))(v) = \bar{c}(\Phi u)(v)$, but $c = \bar{c}$ if and only if $c$ is a real number.

_(c)_
This is the same as the second part in the proof of 6.42.
Suppose there are $u_1$ and $u_2$ in $V$ such that $\Psi u_1 = \Psi u_2$.
Then

$$
0 = (\Psi u_1 - \Psi u_2)(v) = (\Psi(u_1 - u_2))(v) = \langle v, u_1 - u_2 \rangle
$$

for all $v \in V$.
Choosing $v = u_1 - u_2$ shows that $u_1 - u_2 = 0$ and thus $u_1 = u_2$.

_(d)_
From (c), we get that $dim null \Phi = 0$.
Thus, from 3.22, we have

$$
\operatorname{dim} V = \operatorname{dim} \operatorname{null} \Phi + \operatorname{dim} \operatorname{range} \Phi = \operatorname{dim} \operatorname{range} \Phi.
$$

However, $\operatorname{dim} V = \operatorname{dim} V'$.
This shows that $\Phi$ also surjective.
Hence $\Phi$ is invertible, that is, an isomorphism from $V$ to $V'$.
