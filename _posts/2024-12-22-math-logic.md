---
title: "[Math] Logic"
last_modified_at: 2024-12-09T22:20:02-05:00
categories:
  - Math
tags:
  - 
---

## Propositions

#### Conditions

variable에 따라 True, False 가 달라지는 expression.

$$x^2 = 4$$

* $x= \pm 2$ 이면 True.
* otherwise: False

비교: true/false propositions
* true proposition: 항상 true.
* false proposition: 항상 false.

#### Truth Sets

어떤 condition을 만족하는 element들로 구성된 set.

condition이 정해지면, truth set이 지정됨.

> condition을 통해 set이 정해짐.

## Logical Operations

**Unary Operations**

* $\neg$ : Logical Negation

**Binary Operations**

* $\land$ : Logical Conjunction (= `and`)
* $\lor$ : Logical Disjunction (= `or`)
* $\implies$ : Logical Implication
* $\oplus$ : Logical Exclusive Disjunction (= `xor`)

참고: [Truth Table](https://dsaint31.me/mkdocs_site/CE/ch01/ch01_13_boolean_algebra/#symbols-and-truth-table)

#### Logical Implications

Truth Table of Logical Implication

> cause $p$가 False 경우 무조건 True임.
>
> 무죄 추정의 원칙?

$$p \implies q$$

| $p$ | $q$ |  |
| :---: | :---: | :---: |
| False | False | True |
| False | True | True |
| True | False | False |
| True | True | True |

#### Sufficiency and Necessity
참고: [Sufficiency and Necessity](https://dsaint31.tistory.com/314)

#### Converse, Contrapositive, Inverse

$$p \implies q$$

* **converse (역)**: $q\implies p$
* **inverse (부정)**: $\neg p \implies \neg q$
* **contrapositive (대우)**: $\neg q \implies \neg q$

## All and Existent

#### For All $\forall$

$\forall x, p$: 모든 $x$ 에 대해 $p$가 만족함.

* $\forall x, 0x = 0$
* $\forall x \text{ except }x=0, x\frac{1}{x}=1$

#### There Exists $\exists$

$\exists x, q$: 최소한 하나 이상의 $x$에서 $q$가 만족함.

* $\exists x, x+3 = 0$
* $\exists x, x^2=1$

#### Identities and Inverses

Additive Identities and Inverse

$$\begin{aligned} \forall x, \exists a, x+a =x & \implies a=0 \\ \forall x, \exists a, x+a = 0 &\implies a=-x \end{aligned}$$

Multiplicative Identities and Inverse

$$\begin{aligned} \forall x \text{ except } x=0, \exists a, xa=x &\implies a=1 \\ \forall x \text{ except } x=0, \exists a, xa=1 &\implies a=x^{-1} \end{aligned} $$

## Logical Computations

#### Commutativity

교환법칙

* $p \land q \iff q \land p$
* $p \lor q \iff q \land p$

#### Associativity

결합법칙

* $(p \land q) \land r \iff p \land (q \land r)$
* $(p \lor q) \lor r \iff p \lor (q \lor r)$

#### Distributivity

분배접칙

* $p \land (q \lor r) \iff (p \land q) \lor (p \land r)$
* $p \lor (q \land r) \iff (p \lor q) \land (p \lor r)$

* $(p \implies q) \iff (\neg q \implies \neg p)$
* $(p \oplus q) \iff [\{p \land (\neg q)\} \lor \{ (\neg p) \land q \} ]$

---

---

## 같이보면 좋은 자료들

* 참고: [De Morgan's Law](https://dsaint31.me/mkdocs_site/CE/ch01/ch01_13_boolean_algebra/#de-morgans-law)
* [Week01](/math/math-week01/#logic)