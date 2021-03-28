---
title: dp4-ps
description: 計算來源註冊的四個元件點乘積。 |dp4-ps
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035268"
---
# <a name="dp4---ps"></a>dp4-ps

計算來源註冊的四個元件點乘積。

## <a name="syntax"></a>Syntax



| dp4 dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp4                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示執行的作業：


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



Ps \_ 1 \_ 2 和 ps \_ 1 3 的限制 \_ ：

-   每個著色器最多可以使用四個 dp4 指令。
-   每個 dp4 指令都會計算為兩個算術指令。

1 \_ X 版本的限制：

-   因為 dp4 是在向量和 Alpha 管線中執行，所以無法共同發出此指令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




