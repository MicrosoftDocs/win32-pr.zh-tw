---
title: cmp-ps
description: 如果 src0 為0，請選擇 [src1]。 否則，請選擇 [src2 收取]。 每個通道都會進行比較。
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022815"
---
# <a name="cmp---ps"></a>cmp-ps

如果 src0 >= 0，請選擇 [src1]。 否則，請選擇 [src2 收取]。 每個通道都會進行比較。

## <a name="syntax"></a>Syntax



| cmp dst、src0、src1、src2 收取 |
|---------------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。
-   src2 收取是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Cmp                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

版本 1 \_ 2 和 1 3 有幾個額外的限制 \_ ：

-   每個著色器最多可以使用三個 cmp 指令。
-   目的地暫存器不能與任何來源暫存器相同。

此範例會進行四個通道的比較。


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




