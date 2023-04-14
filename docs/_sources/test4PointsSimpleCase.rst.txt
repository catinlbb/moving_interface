================================================
求解样条插值简单测试例子(圆周上4点测试)
================================================
圆上的4点 :math:`x=0,\frac{\pi}{2},\pi, \frac{3\pi}{2},2\pi`， :math:`y=0,1,0,-1,0`, 得到的线性方程组为
(:math:`6/\pi\approx 1.909859317`)



.. math::
 
    \left(
        \begin{array}{cccc}
        2&1/2&0&\frac{1}{2}\\
        \frac{1}{2}&2&\frac{1}{2}&0\\
        0&\frac{1}{2}&2&\frac{1}{2}\\
        \frac{1}{2}&0&\frac{1}{2}&2\\
        \end{array}
    \right)
    \left(
        \begin{array}{c}
        m_0\\
        m_1\\
        m_2\\
        m_3\\
        \end{array}
    \right)=
    \left(
        \begin{array}{c}
        6/\pi\\
        0\\
        -6/\pi\\
        0\\
        \end{array}
    \right)

求解得到:math:`(m_0,m_1,m_2,m_3)=(3/\pi,0,-3/\pi,0)`,(:math:`3\pi\approx0.95492965855`)。

中间步骤检查：LU分解之后得到的矩阵为

.. math::
    L=\left(\begin{array}{cccc}
    2&0&0&0\\
    1/2&8/15&0&0\\
    0&1/2&28/15&0\\
    1/2&-1/8&8/15&12/7\\
    \end{array}
    \right)
    ,\quad
    U=\left(
        \begin{array}{rrrr}
        1&\frac{1}{4}&0&\frac{1}{4}\\
        0&1&\frac{4}{15}&-\frac{1}{15}\\
        0&0&1&\frac{2}{7}\\
        0&0&0&1\\
        \end{array}
    \right)
