---
title: m4x3-vs
description: 將4個元件向量乘以4x3 矩陣。 |m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974024"
---
# <a name="m4x3---vs"></a>m4x3-vs

將4個元件向量乘以4x3 矩陣。

## <a name="syntax"></a>Syntax



| m4x3 dst、src0、src1 |
|----------------------|



 

其中

-   dst 是目的地註冊。 結果是3個元件的向量。
-   src0 是代表4元件向量的來源暫存器。
-   src1 是代表4x3 矩陣的來源暫存器，它會對應至3個連續暫存器中的第一個。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m4x3                   | x    | x    | x    | x     | x    | x     |



 

目的地註冊需要 xyz mask。 Src0 允許否定和 swizzle 修飾詞，但不允許 src1。

下列程式碼片段會顯示已執行的作業。


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



輸入向量位於 register src0 中。 輸入4x3 矩陣位於 register src1 和接下來的兩個較高的暫存器中，如下列擴充所示。 產生3D 結果，讓目的地登錄的另一個元素 (的) 不會受到影響。

這項作業通常用來將位置向量轉換為沒有 projective 效果的矩陣，例如模型空間轉換時。 此指示會實作為一對點產品，如下所示。


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Swizzle 和否定修飾詞對 src1 暫存器而言是不正確。 Dst 和 src0 暫存器不能相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




