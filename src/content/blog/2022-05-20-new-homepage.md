---
title: New homepage
---

设$F\neq\varnothing\subseteq\mathbb{R}^{2}$是平面上一图形, 记平面上全体保持$F$的正交变换为$G_{F}$, 即$G_{F}=\{\sigma:\mathbb{R}^{2}\to\mathbb{R}^{2}|\sigma(F)=F\text{且}\sigma\text{是正交变换}\}$, 易见它关于映射复合构成群, 称为图形$F$的\textbf{对称群}(symmetry group). 
\begin{lemma}设$P\subseteq\mathbb{R}^{2}$是一个多边形, 那么对任何正交变换$\sigma\in G_{P}$, $\sigma$将多边形的顶点映到顶点.
\end{lemma}
\begin{proof}先证$P$的任一顶点$V$在$\sigma$作用下必定在$P$的边界上. 再说明$\sigma(V)$不可能落在多边形某条边的内部.
$$
\begin{tikzcd}
                                           & C \arrow[rd, no head] &                      &                       &                       \\
                                           &                       & D \arrow[r, no head] & M \arrow[rd, no head] &                       \\
B \arrow[rd, no head] \arrow[ruu, no head] &                       &                      &                       & V \arrow[ld, no head] \\
                                           & A \arrow[rr, no head] &                      & N                     &                      
\end{tikzcd}
$$假设$V^{\prime}=\sigma(V)$在多边形$P$的内部, 那么存在闭圆盘$D$满足$D$以$V^{\prime}$为圆心且$D\subseteq P$. 于是对介于$0^{\circ}$到$360^{\circ}$的任意角$\alpha$, 存在$D$中点$J^{\prime},K^{\prime}(J^{\prime}=\sigma(J),K^{\prime}=\sigma(K),J,K\in P)$使得$\angle J^{\prime}V^{\prime}K^{\prime}=\alpha$, 因为正交变换保持角度, 所以$\angle JVK=\angle J^{\prime}V^{\prime}K^{\prime}=\alpha$.但$P$中任何以$V$为顶点的角都不超过$\angle MVN\textless 360^{\circ}$, 所以选取$\alpha\textgreater\angle MVN$即可得到矛盾, 于是知$V^{\prime}$在$P$的边界上. 下面说明$V^{\prime}$不可能在$P$的某条边的内部. 假设$V^{\prime}$在某条边内部. 当$\angle MVN\textless 180^{\circ}$时, 存在$J^{\prime},K^{\prime}\in P$使得$\angle J^{\prime}V^{\prime}K^{\prime}=180^{\circ}$, 因此$\angle JVK=180^{\circ}$. 但$\angle JVK\leq \angle MVN\textless 180^{\circ}$, 这就得到了矛盾. 
$$
\begin{tikzcd}
                       & C \arrow[rd, no head] \arrow[ld, no head] &                       \\
B \arrow[d, no head]   &                                           & M \arrow[ld, no head] \\
A \arrow[rrd, no head] & V \arrow[rd, no head]                     &                       \\
                       &                                           & N                    
\end{tikzcd}
$$
当$\angle MVN\textgreater 180^{\circ}$时, 对$M^{\prime}=\sigma(M),N^{\prime}=\sigma(N)$, 有$$\angle M^{\prime}V^{\prime}N^{\prime}=\angle MVN\textgreater 180^{\circ},$$ 但$\angle M^{\prime}V^{\prime}N^{\prime}\leq 180^{\circ}$, 矛盾.\end{proof}
\par 根据上面的引理, 若记多边形$P$的顶点集为$\text{Ver}(P)$, 则每个$\sigma\in G_{P}$在$\text{Ver}(P)$上的限制给出了$\text{Ver}(P)$上的置换. 事实上, 每个$\sigma$被它在顶点上的作用唯一确定, 具体地, 对$\sigma,\tau\in G_{P}$, 如果$\sigma|_{\text{Ver}(P)}=\tau|_{\text{Ver}(P)}$, 那么$\sigma=\tau$. 这是因为如果$\sigma|_{\text{Ver}(P)}=\tau|_{\text{Ver}(P)}$, 那么$\sigma\tau^{-1}$作为$\mathbb{R}^{2}$上线性变换固定两个线性无关的向量, 于是$\sigma=\tau$. 下面我们来看正$n$边形的对称群具有何种性质.
\par 将正$n(n\geq 3)$边形的中心置于$\mathbb{R}^{2}$原点, 第$k(1\leq k\leq n)$个顶点置于$v_{k}=(\cos 2k\pi/n,\sin 2k\pi/n)$, 记该正$n$边形的对称群是$D_{n}$, 称为\textbf{正$n$边形的二面体群}(dihedral group). 由前面的讨论知, $D_{n}$中的元素将多边形顶点映至顶点, 我们知道正$n$边形任意两个顶点间的距离最短当且仅当这两个顶点是相邻的, 所以由正交变换保持长度可知$D_{n}$中元素作用每个顶点只可能把该顶点变为相邻顶点.我们已经看到$D_{n}$中任何置换$\sigma$被它在两个顶点上的作用唯一确定, 所以只要确定$D_{n}$中两个顶点被$\sigma$作用后的像就可以确定$\sigma$. $\sigma(v_{1})$有$n$种选取方式, 当$\sigma(v_{1})$确定后$\sigma(v_{2})$只有两种选取方式, 所以$|D_{n}|\leq 2n$. 记$r\in D_{n}$是绕原点逆时针旋转$2\pi/n$的旋转变换, 即满足$r(v_{1})=v_{2},r(v_{2})=v_{3},...,r(v_{n})=v_{1}$的正交变换. 记$s\in D_{n}$是关于$x$轴的镜像反射, 即$s:\mathbb{R}^{2}\to\mathbb{R}^{2},(x,y)\mapsto (x,-y)$, 从而$s(v_{1})=v_{1},s(v_{2})=v_{n},s(v_{3})=v_{n-1},...,s(v_{n})=v_{2}$. 那么$r^{n}=1,r^{k}\neq 1,\forall 1\leq k\leq n-1, s^{2}=1,rs=sr^{-1}$. 因为$s$固定$v_{1}$, 所以$s\neq r^{k},\forall 1\leq k\leq n-1$. 由此可知$D_{n}$中包含下述$2n$个元素：$1,r,r^{2},...,r^{n-1},s,sr,...,sr^{n-1}$, 故$D_{n}=\{1,r,r^{2},...,r^{n-1},s,sr,...,sr^{n-1}\}$恰好有$2n$个元素. 设正整数$n\geq 3$, 现在我们来看$D_{n}$与对称群$S_{n}$的关系.
\begin{proposition}设$n$是正整数且$\sigma=(123\cdots n)$, 
$$\tau=\left(\begin{array}{cccccccccc}
1 & 2 & 3 & 4 & 5 & \cdots & i & \cdots & n-1 & n \\
1 & n & n-1 & n-2 & n-3 & \cdots & n+2-i & \cdots & 3 & 2
\end{array}\right)\in S_{n},$$那么$\sigma\tau=\tau\sigma^{-1},\tau^{2}=(1),\sigma^{n}=(1)$. 记$D=\langle \sigma,\tau\rangle$是$\{\sigma,\tau\}$在$S_{n}$中生成的子群, 那么$D_{n}\cong D$. 特别地, 当$n=3$时, $D_{3}\cong S_{3}$.\end{proposition}
\begin{proof}每个$D_{n}$中元素都可以唯一地表示为$s^{i}r^{j},0\leq s\leq 1,0\leq j\leq n-1$的形式, 命
$$\psi:D_{n}\to D,s^{i}r^{j}\mapsto \tau^{i}\sigma^{j},$$易验证这是满群同态. 如果对$0\leq i,k\leq 1,0,l,j\leq n-1$有$\psi(s^{i}r^{j})=\psi(s^{k}r^{l})$, 那么$\tau^{i}\sigma^{j}=\tau^{k}\sigma^{l}$, 于是$\tau^{i-k}=\sigma^{l-j}$. 因为$\tau=\tau^{-1}\neq \sigma^{m},\forall 0\leq m\leq n-1$, 所以必有$i-k=0$, 从而由$1-n\leq l-j\leq n-1$可得$l-j=0$, 这就得到了$\psi$是单射. 我们得到群同构$D_{n}\cong D$. 当$n=3$时, $|D|=|D_{3}|=6=|S_{3}|$, 这迫使$D=S_{3}$, 因此$D_{3}\cong S_{3}$.\end{proof}
