---
title: m3x2-ps
description: 將3個元件向量乘以3x2 矩陣。 |m3x2-ps
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59bf908a2858e46f9c1e339db32d3e6e57062bc280b8223a9fcb66a527380773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672638"
---
# <a name="m3x2---ps"></a>m3x2-ps

將3個元件向量乘以3x2 矩陣。

## <a name="syntax"></a>Syntax



| m3x2 dst、src0、src1 |
|----------------------|



 

其中

-   dst 是目的地註冊。 結果是2個元件的向量。
-   src0 是代表3個元件向量的來源暫存器。
-   src1 是代表3x2 矩陣的來源暫存器，它會對應到2個連續暫存器中的第一個。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

目的地註冊需要 xy 遮罩。 Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。

下列方會顯示指令的運作方式：


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



輸入向量位於 register src0 中。 輸入3x2 矩陣位於登錄 src1 和下一個較高的註冊檔中，如下列擴充所示。 會產生2D 結果，而將目的地暫存器的其他元素 (的 destination 和 dest) 不會受到影響。

這項作業通常用於2D 轉換。 此指示會實作為一對點產品，如下所示。


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Swizzle 和否定修飾詞對 src1 暫存器而言是不正確。 Dst 和 src0 暫存器或 src1 + i 註冊的任何一個都不能相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




