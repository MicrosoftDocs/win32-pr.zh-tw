---
title: m4x4-vs
description: 將4個元件向量乘以4x4 矩陣。 |m4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195934"
---
# <a name="m4x4---vs"></a>m4x4-vs

將4個元件向量乘以4x4 矩陣。

## <a name="syntax"></a>Syntax



| m4x4 dst、src0、src1 |
|----------------------|



 

其中

-   dst 是目的地註冊。 結果是4個元件的向量。
-   src0 是代表4元件向量的來源暫存器。
-   src1 是代表4x4 矩陣的來源暫存器，它會對應至4個連續暫存器中的第一個。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m4x4                   | x    | x    | x    | x     | x    | x     |



 

目的地註冊需要 xyzw (預設) 遮罩。 Src0 允許否定和 swizzle 修飾詞，但不允許 src1。

Swizzle 和否定修飾詞對 src0 暫存器而言是不正確。 目的地和 src0 暫存器不可以相同。

下列程式碼片段會顯示已執行的作業。


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



輸入向量位於 register src0 中。 輸入4x4 矩陣位於 register src1 和後續三個較高的暫存器中，如下列擴充所示。

這項作業通常用來將位置轉換成投射矩陣。 此指示會實作為一系列的點乘積，如下所示。


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




