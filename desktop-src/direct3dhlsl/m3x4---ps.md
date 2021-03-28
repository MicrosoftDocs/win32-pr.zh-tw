---
title: m3x4-ps
description: 將3個元件向量乘以3x4 圓矩陣。 |m3x4-ps
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974352"
---
# <a name="m3x4---ps"></a>m3x4-ps

將3個元件向量乘以3x4 圓矩陣。

## <a name="syntax"></a>Syntax



| m3x4 dst、src0、src1 |
|----------------------|



 

其中

-   dst 是目的地註冊。 結果是4個元件的向量。
-   src0 是代表3個元件向量的來源暫存器。
-   src1 是代表3x4 圓矩陣的來源暫存器，它會對應至4個連續暫存器中的第一個。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

目的地註冊需要 xyzw (預設) 遮罩。 Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。

下列程式碼片段會顯示已執行的作業。


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



輸入向量位於 register src0 中。 輸入3x4 圓矩陣位於 register src1 和接下來的兩個較高的暫存器中，如下列擴充所示。

這項作業通常用來透過具有 projective 效果但未套用轉譯的矩陣來轉換位置向量。 此指示會實作為一對點產品，如下所示。


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




