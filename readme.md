# Abstract

This paper focuses on sentences built around gradable adjectives, especially measurable ones, used as predicates in Mandarin. These sentences are classified as expressing assignable meaning or comparative meaning according to the lexical entry of the gradable adjective. In terms of the latter type, sentences are further divided into three subtypes, i.e., positivity, superiority and equality. 

The whole research is conducted under the theoretical frame of generative syntax and formal semantics. The paper attempts to give a complete analysis integrating syntax and semantics. DegP hypothesis and DegP-shell are the two main cornerstones of this research.

For the syntactic part, this paper assumes a perspective of the complementary distribution of **DegP-AP** and **DegP-DegP-AP** structures. In detail, the higher DegP serving to introduce the standard is consistently projected, while the lower DegP severing to introduce the gap between the comparee and the standard is projected on the condition of the appearance of a differential phrase strictly greater than zero. 

For the semantic part, this paper makes a clear division of labour among the gradable adjective, the lower functional degree head and the higher functional degree head. Thanks to this division, wrong readings of some constructions on gradable adjectives derived out via previous analyses are successfully corrected. Detailed semantic formalizations and calculations are illustrated with examples of different types of constructions built around gradable adjectives. 

## Example in Positivity

### AST

![](./Image/pos.png)

### Sematic

$$
[\![\xi]\!]=\lambda G_{<d,<e,t>>} \lambda x. \exists d [G(x,d) \land (d=d_{stnd})] \qquad <d,<e,t>,<e,t>>
$$

$$
\exists d [G(x,d) \land (d=d_{stnd})] \Leftrightarrow G(x,d_{stnd}) \enspace where \enspace G(x,d) = G - degree(x) \geq d
$$

$$
[\![\xi]\!]=\lambda G_{<d,<e,t>>} \lambda x. [G(x,d_{stnd})] \qquad <d,<e,t>,<e,t>>
$$

The meaning of the sentence in 'John hen gao.' can be figured out successfully following the semantic calculations illustrated below.

$$
\begin{aligned}[t]
            [\![\xi \enspace gao]\!] &= \lambda G_{<d,<e,t>>} \lambda x. [G(x,d_{stnd})]([\![gao]\!]) \\
            &= \lambda x.[height(x) \geq d_{stnd}] \qquad <e,t>
        \end{aligned}
$$

$$
\begin{aligned}[t]
            [\![John \enspace \xi \enspace gao]\!] &= \lambda x.[height(x) \geq d_{stnd}]([\![John]\!]) \\
            &= height(John) \geq d_{stnd}
        \end{aligned}
$$

## Example in Superiority

### AST

![](./Image/sup.png)

### Sematic

$$
[\![\xi_1]\!] = \lambda G_{<d,<e,t>>} \lambda d \lambda x.[G(x,d)] \qquad <<d,<e,t>>,<d,<e,t>>>
$$

$$
\begin{aligned}[t]
            [\![\xi_1 \enspace gao]\!] &= \lambda G_{<d,<e,t>>} \lambda d \lambda x.[G(x,d)]([\![gao]\!]) \\
            &= \lambda d \lambda x.[height(x) \geq d] \qquad <d,<e,t>>
        \end{aligned}
$$

$$\begin{aligned}[t]
            [\![1.7mi \enspace \xi_1 \enspace gao]\!]
            &= \lambda d \lambda x.[height(x) \geq d](1.7mi) \\
            &= \lambda x.[height(x) \geq 1.7mi] \qquad <e,t>
        \end{aligned}
        $$

$$\begin{aligned}[t]
    [\![bi]\!] = \lambda P.[P] \qquad <<e,t>,<e,t>>
\end{aligned}$$

$$\begin{aligned}[t]
    [\![bi \enspace 1.7mi \enspace \xi_1 \enspace gao]\!] &= [\![bi]\!]([\![1.7mi \enspace \xi_1 \enspace gao]\!])
    &= \lambda x.[height(x) \geq 1.7mi] \qquad <e,t>
\end{aligned}$$

$$\begin{aligned}[t]
    [\![John \enspace bi \enspace 1.7mi \enspace \xi_1 \enspace gao]\!] &= \lambda x.[height(x) \geq 1.7mi](John) \\
    &= height(John) \geq 1.7mi
\end{aligned}$$

## Example in Equality

### AST

![](./Image/eq.png)

### Sematic

$$\begin{aligned}[t]
    [\![yiyang]\!] 
    &= \lambda G_{<d,<e,t>>} \lambda y \lambda x.[Max \enspace d_1 G(x,d_1) -  Max \enspace d_2 G(x,d_2) = 0]\\ &
    <<d,<e,t>>,<e,<e,t>>>
\end{aligned}$$

$$\begin{aligned}[t]
    [\![yiyang_{2}]\!] 
    &= \lambda G_{<d,<e,t>>} \lambda y \lambda x.[Max \enspace d_1 G(x,d_1) =  Max \enspace d_2 G(x,d_2)]\\ &
    <<d,<e,t>>,<e,<e,t>>>
\end{aligned}$$

$$\begin{aligned}[t]
    [\![yiyang \enspace gao]\!] 
    &= \lambda G_{<d,<e,t>>} \lambda y \lambda x.[Max \enspace d_1 G(x,d_1) - Max \enspace d_2 G(x,d_2) = 0]([\![gao]\!] ) \\
    &= \lambda y \lambda x.[Max \enspace d_1 (height(x) \geq d_1) - Max \enspace d_2 (height(y) \geq d_2) = 0] \\
    & <e,<e,t>>
\end{aligned}$$

$$\begin{aligned}[t]
    [\![he &\enspace Mary \enspace yiyang \enspace gao]\!] \\
    &= \lambda y \lambda x.[Max \enspace d_1 (height(x) \geq d_1) - Max \enspace d_2 (height(y) \geq d_2) = 0]([\![he \enspace Mary]\!]) \\
    &= \lambda y \lambda x.[Max \enspace d_1 (height(x) \geq d_1) - Max \enspace d_2 (height(y) \geq d_2) = 0](Mary)  \\
    &= \lambda x.[Max \enspace d_1 (height(x) \geq d_1) - Max \enspace d_2 (height(Mary) \geq d_2) = 0] \\
    & <e,t>
\end{aligned}$$

$$\begin{aligned}[t]
    [\![John &\enspace he \enspace Mary \enspace yiyang \enspace gao]\!] \\
    &= \lambda x.[Max \enspace d_1 (height(x) \geq d_1) - Max \enspace d_2 (height(Mary) \geq d_2) = 0]([\![John]\!]) \\
    &= Max \enspace d_1 (height(John) \geq d_1) - Max \enspace d_2 (height(Mary) \geq d_2) = 0 \\
\end{aligned}$$