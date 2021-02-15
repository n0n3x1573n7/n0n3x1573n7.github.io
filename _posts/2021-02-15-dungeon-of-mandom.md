---
title: "Dungeon of Mandom: Risk vs Reward"
date: 2021-02-15 00
categories:
  - game design
tags:
  - 보드게임
---

저는 작은 게임들을 좋아합니다. 특히 크기는 작지만 그 전략적 깊이나 다양성이 높은 작품들을 좋아합니다. [Gamelyn Games사의 Tiny Epic 시리즈](https://www.gamelyngames.com/)를 높게 평가하는 이유이기도 합니다.

맨덤의 던전은 이러한 게임 중 하나로, 친구들에게 제가 [하나비](https://n0n3x1573n7.github.io/study/hanabi-npc-1/)나 [러브 레터](https://n0n3x1573n7.github.io/game%20design/love-letter/) 다음으로 소개하는 보드게임입니다. 하나비로 협력을, 러브 레터로 운[^1]을 보여줬다면, [맨덤의 던전](https://oinkgames.com/en/games/analog/dungeon-of-mandom-eight/), 또는 [Welcome to the Dungeon](https://iellousa.com/products/welcome-to-the-dungeon)/[Welcome Back to the Dungeon](https://iellousa.com/products/welcome-back-to-the-dungeon)으로 전략을 보여주는 거죠. 두 가지 게임은 같은 게임이고, 출판사만 다릅니다.

이 글에서는 맨덤의 던전을 기준으로 한 룰을 설명하고, 그에 따른 전략을 제안합니다.

# 게임 규칙

게임이 시작될 때, 각 플레이어들은 레퍼런스 카드를 한 장씩 받고, 하얀 쪽을 위로 가게 둡니다.

매 라운드가 시작될 때, 다음 몬스터들이 있는 몬스터 덱을 셔플합니다.

| 레벨 | 장수 | 이름     |
| ---- | ---- | -------- |
| 1    | 2    | 고블린   |
| 2    | 2    | 해골전사 |
| 3    | 2    | 오크     |
| 4    | 2    | 뱀파이어 |
| 5    | 2    | 골렘     |
| 6    | 1    | 사신     |
| 7    | 1    | 마왕     |
| 9    | 1    | 드래곤   |

또한, 용사 타일과 6개의 장비들을 늘어놓습니다. 용사는 기본적으로 체력 3을 가지고, 다음 장비들을 사용할 수 있습니다:

| 이름      | 효과                                                         |
| --------- | ------------------------------------------------------------ |
| 방패      | +3HP                                                         |
| 갑옷      | +5HP                                                         |
| 창        | 드래곤을 처치합니다.                                         |
| 용사의 검 | 던전에 들어가기 전에 몬스터 하나를 고릅니다. 해당 몬스터를 처치합니다. |
| 횃불      | 3 이하 레벨의 몬스터를 처치합니다.                           |
| 성배      | 짝수 레벨 몬스터를 처치합니다.                               |

각 라운드는 2개의 페이즈로 구분됩니다.

## 1. 던전 만들기

던전 만들기에서는, 선플레이어부터 돌아가며 둘 중 한가지를 할 수 있습니다:

1. 던전

   몬스터를 한 장 뽑아 봅니다. 플레이어는 다음 중 하나를 선택합니다:

   1. 몬스터를 던전의 가장 위에 뒷면으로 추가합니다.
   2. 몬스터를 던전에서 제거합니다. 단, 이 경우 장비 하나를 같이 제거해야 합니다.

2. 패스

   패스하고, 이후 라운드에 참여하지 않습니다.

한 명을 제외한 모두가 패스하면 패스하지 않은 사람은 반드시 던전에 입장해야 합니다.

첫 번째 몬스터 카드는 항상 던전에 추가해야 한다는, 룰북에서 제안하는 변형룰이 있습니다.

## 2. 던전 입장

던전에 들어가는 플레이어는 제거되지 않은 아이템을 모두 소지하고 들어갑니다. 용사의 검이 제외되지 않았다면, 이 때 몬스터 한 종류를 고릅니다.

이제, 던전에 있는 몬스터를 뒤집습니다.

- 해당 몬스터를 처치할 수 있다면, 아무 피해 없이 제외됩니다.
- 처치할 수 없다면, 용사의 체력이 몬스터의 레벨만큼 깎이고 제외됩니다.

용사의 체력이 0 이하가 되면 사망합니다. 레퍼런스 카드를 빨간 면이 위로 가도록 뒤집습니다. 이미 빨간 면이 위라면, 게임에서 탈락되어 더이상 참여할 수 없습니다. 한 사람을 제외하고 모두가 탈락된다면 탈락되지 않은 사람이 승리합니다!

하지만 던전 덱이 용사의 체력이 0 이하가 되기 전에 떨어진다면, 성공합니다. 성공 토큰 하나를 받습니다. 두 번째 성공 토큰을 받았다면 게임에서 승리합니다!

게임이 종료되지 않았다면, 던전에 들어간 플레이어(아웃되었다면 던전에 들어가게 만든 플레이어)가 선플레이어가 되어 다시 던전 만들기부터 진행합니다.

# 기본 전략

맨덤의 던전의 모든 것은 던전 빌딩에서 옵니다. 용사의 검을 잘 선택함으로서 죽거나 살거나가 결정될수는 있지만, 이는 결국 던전 빌딩에서 얼마나 많은 정보를 얻어냈냐에 따라 달려있습니다.

던전 빌딩 전략은 크게 두 가지로 결정됩니다: "어떤 아이템을 뺄 것인가", 그리고 "언제 빠질 것인가". 몬스터는 일단 기본적으로 넣는것을 가정합니다.

## 장비의 이해

이 전에, 장비에 대한 간단한 분석을 해보겠습니다. 용사의 기본 체력은 3이고, 방패로 +3, 갑옷으로 +5를 하여 최대 11까지 증가시킬 수 있습니다. 즉시 처치 장비들은 용사의 검을 제외하고 다음과 같은 몬스터들을 처치할 수 있습니다:

| 아이템 | 처치 가능                         |
| ------ | --------------------------------- |
| 창     | 드래곤(9)                         |
| 횃불   | 고블린(1), 해골전사(2), 오크(3)   |
| 성배   | 해골전사(2), 뱀파이어(4), 사신(6) |

다시 말해, 골렘(5)과 마왕(7)은 용사의 검이 아니라면 처치할 수 없으며, 용사의 검이 없으며 마왕을 포함하여 두 장 이상이 던전에 들어가 있다면 체력 장비 여부에 상관없이 용사는 _반드시_ 사망합니다.

횃불과 성배의 경우, 성배는 5장에 걸쳐 최대 18피해, 횃불은 6장에 걸쳐 최대 12피해를 막을 수 있습니다 어느쪽이든 상관없이, 체력 아이템을 모두 가지고 있다고 해도 사망합니다.

창은 레벨 9의 드래곤 한 장만을 처치할 수 있지만, 반대로 용사의 검 없이는 드래곤을 처치할 수 있는 _유일한_ 장비입니다. 창이 빠진다면, 용이 존재하고, 골렘(5)과 마왕(7) 중 하나라도 남아있게 되면 용사는 _반드시_ 사망합니다.

## 어떤 아이템을 뺄 것인가?

아이템을 뺄 때에는 *정직하게* 뺄 수도, *블러핑으로* 뺄수도 있습니다. 다만 몬스터를 넣는 것이 기본이 되어야 하며, 이 정보를 효율적으로 활용하는 것이 아이템을 빼는것보다 더 좋다는 것을 항상 기억해야 합니다.

### 체력 아이템

#### 정직

가장 무난합니다. 특히, 방패의 경우 3 이상/갑옷의 경우 5 이상의 몬스터를 함께 제거하면 이득이며, 그 아래라 할지라도 처치 불가능한 몬스터라면 이 차이로 인해 생존 여부가 갈릴 수 있습니다.

#### 블러핑

제거 가능한 낮은 몬스터를 제거한 경우가 블러핑이겠지만, 이는 횃불이나 성배, 또는 해골전사(2)의 경우 둘 다 빠진다면 차이를 만들 수 있습니다.

### 용사의 검

#### 정직

골렘(5) 또는 마왕(7), 내지는 창이 없을 때 용(9)과 함께 뺄 때입니다. 다만, 빼는것보다 넣은 후 이 정보를 이용하는게 나을 수 있단것도 기억하세요.

#### 블러핑

다른 몬스터와 함께 뺄 때입니다. 정보 혼란을 주는 용도로서 사용하기 굉장히 좋습니다.

### 창

#### 정직

용(9)을 뺄 때 입니다.

#### 블러핑

용(9)이 아닌 것과 뺄 때 입니다. 어느쪽이든, 정보 혼란을 줄 수 있습니다. 추가로, 용을 넣은 후, 다음 턴에 창을 빼고 그 다음 턴에 패스하는 것은 해당 라운드의 던전 탐사를 굉장히 어렵게 만들 수 있습니다.

### 횃불/성배

#### 정직

용사의 검 또는 창이 빠진 상태에서 골렘(5), 마왕(7), 용(9)과 함께 제거하는 것입니다.

#### 블러핑

 이 장비의 경우 너무 활용도가 높아, 오히려 정직하게 이 장비들으로 처치할 수 있는 몬스터를 빼는 것이 블러핑이 됩니다.

## 언제 빠질것인가?

저의 경우, 기본적으로 첫 두 라운드 안에 장비가 두 개 이상 빠지지 않는다면, 두 라운드(또는 3명 이하의 경우 세 라운드)까지는 반드시 버텨봅니다. 단, 용을 넣었지만 누군가 블러핑으로 창을 제거한 경우 바로 빠집니다. 그 이후, 내가 넣은 몬스터들로 인해 내가 입을 피해가 (현재 체력)/(플레이어 수+1) 이상이 되면 빠집니다.

또한 빠진 장비에 따라 얼마나 많은 몬스터를 처치할 수 있는가 역시 그 기준이 됩니다. 횃불이나 성배의 경우 사신(6)정도를 자잘한 피해를 막아주는 것으로 볼 수 있지만, 반대로 생각하면 체력이 최대 11이기 때문에, "긁히는" 피해가 얼마나 아픈지를 생각해봐야 합니다. 횃불이나 성배가 제거된다면 거의 바로 빠지는 것을 고려하는 이유입니다.

반대로, 제가 뺀 아이템과 몬스터를 고려했을 때 버텨볼만 하다는 생각이 들면 버티기도 합니다. 예를 들어 마왕과 용사의 검이 빠졌다면, 처치 불가능한 몬스터가 던전에 모두 있다고 하더라도 살아남을 수 있다면 버티는 것이 좋습니다.

물론 이는 제 주관적인 기본 전략으로, 각자의 직관과 경험에 따라 빠지는 것이 좋을 수 있습니다. 많이 해보는게 좋겠죠.

# Welcome [Back] to the Dungeon

맨덤의 던전과 같은 규칙을 공유하는 Welcome to the Dungeon의 경우 위의 용사와 같은 Warrior을 제외하고 세 명의 추가 용사들을 제공합니다. 또한, Welcome Back to the Dungeon은 네 명의 추가 용사와 일곱 마리의 특별 몬스터[^3]를 제공합니다. 나중에 기회가 된다면 각 용사별 전략 등을 더 소개할 수 있다면 좋을 것 같습니다.

---

[^1]: 전략이 존재는 하나, 매 턴 할 수 있는 선택지가 사실상 두 가지로 한정되고, 비공개 정보가 거의 존재하지 않으므로 비교적 운적인 요소에 의존한다고 볼 수 있습니다.
[^2]: 3번째로 나왔다면 레벨 3 Orc가 되는 식입니다. 8레벨 또는 10레벨 이상인 경우, 정체가 없습니다. 하우스 룰로, 정체가 없는 경우 Shapeshifter으로 취급할 수도 있으며, 8이 나오면 Count로 취급할 수도 있습니다.
[^3]: 프로모로 한 마리가 더 존재합니다.