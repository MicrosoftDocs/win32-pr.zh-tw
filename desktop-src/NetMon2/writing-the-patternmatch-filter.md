---
description: 模式比對篩選準則會通知驅動程式，接受特定位移具有特定模式的框架。
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: 撰寫 PATTERNMATCH 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993084"
---
# <a name="writing-the-patternmatch-filter"></a>撰寫 PATTERNMATCH 篩選

模式比對篩選準則會通知驅動程式，接受特定位移具有特定模式的框架。 您可以指定最多四個詳細的模式比對，可以在網路監視器驅動程式評估的邏輯 AND 或語句中結合。

若要執行模式比對，請使用下列網路監視器結構：

-   [**表達**](expression.md)
-   [**ANDEXP**](andexp.md)
-   [**PATTERNMATCH**](patternmatch.md)

若要評估 **或** 語句，請結合二到四種模式，以符合 [**ANDEXP**](andexp.md)結構 (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3) 。 若要評估和語句，請將一到四個 **ANDEXP** 結構和 [**運算式**](expression.md) 結構結合 (AndExp1 && AndExp2) 。

## <a name="pattern-match-definitions"></a>模式比對定義

單一模式比對是由 [**PATTERNMATCH**](patternmatch.md) 結構所定義。 個別的相符可以用兩種方式之一來運作。

一般來說，驅動程式會採用位移基礎 (可以是相對於框架的位移、相對於有效通訊協定的位移基準、相對於 IPX 的相對於 IPX 的位移，或是相對於 IP) 的位移基礎， \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 然後開始計算。 驅動程式將會從該處計算位移位元組，然後比對所找到的資料與 **PatternToMatch** 中的第一個長度位元組。 如果兩者相同，且 \_ \_ 未設定模式比對旗標 \_ not 旗標，則此模式會通過。 如果兩者不同，且未設定模式比對 \_ \_ 旗標 \_ ，則模式會通過。 否則，此模式將會失敗。

或：

如果 \_ \_ 已設定模式符合旗標 \_ 埠指定的旗標 \_ ，且基礎設定為相對於 IPX 的相對於 \_ IPX 或相對於 \_ \_ \_ \_ \_ \_ \_ IP 的位移，則比較會比較複雜。 首先，驅動程式會確認位移基礎通訊協定，然後驅動程式會驗證指定的埠是否符合框架中的埠。 最後，驅動程式會確保 **PatternToMatch** 成員與之前相符，但位移是來自 IP 或 IPX 的結尾。 請注意，如果基礎不是這兩種類型的其中一種，則會忽略模式比對 \_ \_ 旗標 \_ 埠 \_ 指定的旗標，且會依照上述方式評估模式。

若要評估單一模式比對， [**運算式**](expression.md) 結構必須有一個包含單一模式相符的 **AndExp** 成員。

建立模式比對篩選牽涉到建立 [**PATTERNMATCH**](patternmatch.md) 結構，並以邏輯方式將它們與 [**運算式**](expression.md) 和 [**ANDEXP**](andexp.md) 結構結合在一起。

**撰寫 PATTERNMATCH 篩選**

1.  在 [**ANDEXP**](andexp.md) 結構中，使用模式比對來填入陣列。
2.  以 **AndExp** 成員的陣列填入 [**運算式**](expression.md)結構。
3.  針對 capture 篩選器，請勿超過四個模式相符專案的總和。
4.  在 [**PATTERNMATCH**](patternmatch.md) 結構中，選取旗標類型。
5.  選取位移。
6.  列舉埠值。
7.  定義位移值。
8.  定義模式長度。
9.  列舉模式值。

## <a name="patternmatch-examples"></a>PATTERNMATCH 範例

此框架表示標準位移。

![標準位移框架](images/offs-pat.png)

程式碼片段會實作為：

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

此框架描述對 IPX)  (埠指定的位移。

![埠指定的位移框架](images/stan-pat.png)

範例程式碼會實作為：

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



