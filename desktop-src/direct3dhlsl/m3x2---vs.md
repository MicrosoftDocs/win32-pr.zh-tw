---
title: m3x2-vs
description: 將3個元件向量乘以3x2 矩陣。 |m3x2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195937"
---
# <a name="m3x2---vs"></a>m3x2-vs

將3個元件向量乘以3x2 矩陣。

## <a name="syntax"></a>Syntax



| m3x2 dst、src0、src1 |
|----------------------|



 

其中

-   dst 是目的地註冊。 結果是2個元件的向量。
-   src0 是代表3個元件向量的來源暫存器。
-   src1 是代表3x2 矩陣的來源暫存器，它會對應到2個連續暫存器中的第一個。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x2                   | x    | x    | x    | x     | x    | x     |



 

目的地註冊需要 xy 遮罩。 Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。

下列方會顯示指令的運作方式：


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



輸入向量位於 register src0 中。 輸入3x2 矩陣位於登錄 src1 和下一個較高的註冊檔中，如下列擴充所示。 會產生2D 結果，而將目的地暫存器的其他元素 (的 destination 和 dest) 不會受到影響。

這項作業通常用於2D 轉換。 此指示會實作為一對點產品，如下所示。


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Swizzle 和否定修飾詞對 src1 暫存器而言是不正確。 目的地和 src0 暫存器，或任何 src1 + i 暫存器都不能相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




