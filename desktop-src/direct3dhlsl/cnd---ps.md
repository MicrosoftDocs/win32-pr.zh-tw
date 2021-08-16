---
title: cnd-ps
description: 根據 src0 0.5 的比較，有條件地選擇 src1 和 src2 收取。
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb31c873bf3a4e38048f57d75a30cec70021716d2aab43b683cb29aef25f7f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726958"
---
# <a name="cnd---ps"></a>cnd-ps

根據 > 0.5 的比較 src0，有條件地選擇 src1 和 src2 收取。

## <a name="syntax"></a>Syntax



| cnd dst、src0、src1、src2 收取 |
|---------------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。
-   src2 收取是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| cnd                   | x    | x    | x    | x    |      |      |       |      |       |



 

若為 1 \_ 1 到 1 \_ 3 的版本，src0 必須是 r0。


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



第1版會 \_ 分別比較每個通道。


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



這些範例示範在第1版著色器中完成的四個通道比較 \_ ，以及第1版著色器中可能的單一通道比較 \_ 。


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



第1版 \_ 到第1版 \_ 只會與 r0 的已複寫 Alpha 通道進行比較。


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



此範例會比較兩個值： A 和 B。此範例假設將載入至 v0，並將 B 載入至 v1。 A 和 B 的範圍必須介於-1 到 + 1 之間，因為色彩暫存器 (vn) 定義為介於0和1之間，所以在此範例中，將會滿足此限制。


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




