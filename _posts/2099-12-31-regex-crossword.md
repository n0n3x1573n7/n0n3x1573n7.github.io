---
title: "Regex Crossword is Hard, even when restricted!"
date: 2099-12-31 00
categories:
  - study
tags:
  - CS
  - 퍼즐
hidden: true
---

Regex Crossword는 Regular Expression을 활용한 퍼즐입니다. 여기에서는 Regex Crossword의 NP-completeness에 대해 논해보겠습니다.

---

# Regular Expression과 Regex Crossword

Formal Language Theory에서는, finite alphabet $$\Sigma$$에 대해 다음과 같이 Regular Language를 재귀적으로 정의합니다:

> 다음은 regular language입니다:
>
> - [Empty Set] $$\emptyset$$
> - [Singleton] $$\{a\}$$, where $$a \in \Sigma$$
>
> 또한 $$R$$과 $$L$$이 regular language라면, 다음 역시 Regular Language입니다.
>
> - [Union] $$R \cup L$$, 또는 $$R|L$$
> - [Concatenation] $$R \cdot L$$, 또는 $$RL$$
> - [Kleene Star] $$R^{*}$$[^a]

현대에 사용하는 Regular Expression은 위의 Regular Language의 연산들을 확장하여, 다음 규칙을 따릅니다:

| 기호          | 설명                                                         |
| ------------- | ------------------------------------------------------------ |
| `.`           | newline을 제외한 어떤 한 문자든 매칭됩니다.                  |
| `[ ]`         | 해당 괄호 안에 있는 문자 중 하나와 매칭됩니다. `-` 캐릭터를 사용해 ascii 문자를 기준으로 사이에 있는 모든 문자를 사용할 수 있습니다. |
| `[^ ]`        | 해당 괄호 안에 있지 않는 문자 중 하나와 매칭됩니다.          |
| `*`           | 바로 앞에 나오는 것이 0번 이상 나오면 매칭됩니다.            |
| `?`           | 바로 앞에 나오는 것이 0번 또는 1번 나오면 매칭됩니다.        |
| `+`           | 바로 앞에 나오는 것이 1번 이상 나오면 매칭됩니다.            |
| `|`           | 바로 앞에 나오는 것 또는 바로 뒤에 나오는 것과 매칭됩니다.   |
| `{n}`         | 앞에 나오는 문자열이 정확히 n번 등장하면 매칭됩니다.         |
| `{m,n}`       | 앞에 나오는 문자열이 m번 이상 n번 이하로 등장하면 매칭됩니다. m 또는 n을 생략할 수 있습니다. |
| `^`           | 문자열의 시작에 매칭됩니다.                                  |
| `$`           | 문자열의 끝에 매칭됩니다.                                    |
| `( )`         | subexpression을 만들어 묶습니다.                             |
| `\n`[^b]      | n번째 subexpression과 매칭됩니다. 1-based indexing을 사용합니다. |
| `n(?=o)`[^b]  | n 뒤에 o가 올 때, n만을 매칭합니다.(positive lookahead)      |
| `n(?!o)`[^b]  | n 뒤에 o가 오지 않을 때, n만을 매칭합니다.(negative lookahead) |
| `n(?<=o)`[^b] | n 앞에 o가 올 때, n만을 매칭합니다.(positive lookbehind)     |
| `n(?<!o)`[^b] | n 앞에 o가 오지 않을 때, n만을 매칭합니다.(negative lookbehind) |

Regular Language에서 사용되는 두 가지 연산자, Kleene Star(`*`)과 Union(`|`)과 문자열의 시작/끝과 매칭되는 `^`과 `$`[^c], 표기상의 ambiguity를 피하기 위한 subexpression(`( )`), 그리고 non-regular으로 표기된 제외한 나머지는 syntactic sugar입니다. 가령, `a?`는 `(a|)`의, `[abc]`는 `(a|b|c)`이죠.

어떤 Regular Expression $$R$$이 표현할 수 있는 모든 string의 집합을 $$L(R)$$으로 표현하겠습니다.

Regex Crossword는 Character set $$\Sigma$$[^d]와 $$n \times m$$의 직사각형 그리드[^e] $$G=\pmatrix{g_{ij}}$$의 각 행과 열에 대해 Regular Expression $$C_i(1\le i\le n)$$, $$R_j(1 \le j \le m)$$이 주어집니다.  $$\forall 1\le i \le n, \cdot_{k=1}^{n}g_{ki} \in L(C_i)$$, $$\forall 1\le j \le m, \cdot_{k=1}^{n}g_{jk} \in L(R_j)$$를 모두 만족하는 $$G=\pmatrix{g_{ij}}$$를 찾는다면 이 퍼즐을 해결한 것입니다. [아래 예시](https://mrtyx.github.io/2017/06/19/Regex%20Crossword/Regex-Crossword-Intermediate-Solutions/)와 같은 방식입니다:

![해결된 Regex Crossword](https://mrtyx.github.io/images/regex/int4.JPG)

이 예시에서, $$C_1=\verb|[DEF][MNO]*|$$는 $$g_{11}g_{12}g_{13}=\verb|"DON"| \in L(C_1)$$이고, 나머지 행과 열 역시 마찬가지임을 알 수 있습니다.

# Regex 

Subexpression Matching과 lookahead/lookbehind



---

[^a]: 이로 인하여 $$\emptyset$$만을 포함한 singleton set 역시 regular language입니다.
[^b]: 이들을 사용하는 Regular Expression은 Regular Language가 아닙니다. Group Referencing이나 Backreferencing
[^c]: Regular Language의 경우 Full Match를 전제로 하므로, 이가 필요 없습니다.
[^d]: 보통은 알파벳과 공백문자(\s)로 한정되나, 어떤 경우는 문장부호 역시 포함됩니다.
[^e]: hexagonal grid를 사용하기도 합니다만, 편의성을 위해 rectangluar grid를 사용합니다.