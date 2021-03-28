---
title: 目的地註冊遮罩
description: 遮罩會指定將會以指示的結果更新目的地登錄的哪些元件。 材質暫存器有一組規則，而 noNtexture 暫存器有另一組規則。
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372401"
---
# <a name="destination-register-masking"></a>目的地註冊遮罩

遮罩會指定將會以指示的結果更新目的地登錄的哪些元件。 材質暫存器有一組規則，而 noNtexture 暫存器有另一組規則。

-   dx9 \_ 圖形 \_ 參考 \_ asm 與登錄修飾詞 \_ \_ \_ \_ 遮罩-本節包含將遮罩套用至目的地暫存器的規則。
-   材質暫存器 \_ \_ 遮罩-材質暫存器有一些獨特的規則。

## <a name="destination-register-masking"></a>目的地註冊遮罩

如下表所示，遮罩 (其中是其中一個有效的頂點著色器 [頂點著色器](dx9-graphics-reference-asm-vs-registers.md) ，) 可以套用至向量資料的個別元件。



| 元件修飾詞 | Description      |
|--------------------|------------------|
| r. {x} {y} {z} {w}     | 目的地遮罩 |



 

-   一般來說，指定目的地登錄寫入遮罩是很好的編碼樣式。 它讓程式碼更容易讀取和維護。
-   您可以指定任何元件組合 (包括 [無]) ，只要 x 在 y 之前、y 在 z 之前、y 到 z 之前，z 就會在 w 之前。
-   選擇和 oFog 輸出暫存器必須只使用一個遮罩。
-   某些指示需要目的地登錄才能使用單一寫入遮罩： exp、expp、log、logp、pow、rcp 和 rsq。
-   在1.0 版中，frc 指令必須有下列其中一個遮罩組合：. x 或. y 或 xy。 2.0 版沒有遮罩限制。
-   sincos 需要下列其中一個遮罩組合：. x 或. y 或 xyz。
-   m3x2 需要 xy 寫入遮罩。
-   m3x3 和 m4x3 需要 xyz 寫入遮罩。
-   m3x4 和 m4x4 需要 .xyz 寫入遮罩或預設寫入遮罩 (xyzw) 。

## <a name="texture-register-masks"></a>材質暫存器遮罩

在紋理座標暫存器上使用修飾詞的驗證規則，比其他暫存器的驗證規則更緊密。

-   如果寫入 oTn，所有先前的暫存器 (oTn-1 ~ oT0) 也必須撰寫。
-   任何 oT 註冊的「合併」寫入遮罩 \# 必須是下列其中一項：
    -   .x
    -   xy
    -   .xyz
    -   xyzw (，這相當於不使用任何元件修飾詞) 

例如，頂點著色器可以個別的指示輸出至材質暫存器。


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



或者，您可以結合指令。


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



這些限制僅適用于材質座標暫存器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器修飾詞](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




