---
title: m3x3-ps
description: 將三個分量向量乘以3x3 矩陣。 |m3x3-ps
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af5f56f659c547d34a61e8bb65ef6cf2730f7e3b0d43f488454e79fe4e02cd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089284"
---
# <a name="m3x3---ps"></a>m3x3-ps

將三個分量向量乘以3x3 矩陣。

## <a name="syntax"></a>Syntax



| m3x3 dst、src0、src1 |
|----------------------|



 

其中

-   dst 是目的地註冊。 結果是3個元件的向量。
-   src0 是代表3個元件向量的來源暫存器。
-   src1 是代表3x3 矩陣的來源暫存器，它會對應至3個連續暫存器中的第一個。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

目的地註冊需要 xyz mask。 Src0 允許否定和 swizzle 修飾詞，但無法用於 src1。

下列程式碼片段會顯示已執行的作業。


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



輸入向量位於 register src0 中。 輸入3x3 矩陣位於 register src1 和接下來的兩個較高的暫存器中，如下列擴充所示。 產生3D 結果，讓目的地登錄的另一個元素 (的) 不會受到影響。

這項作業通常用於在光源計算期間轉換一般向量。 此指令會實作為一組點乘積，如下所示。


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




