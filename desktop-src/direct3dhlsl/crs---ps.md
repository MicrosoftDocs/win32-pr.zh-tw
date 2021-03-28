---
title: crs-ps
description: 使用右手條規則來計算交叉乘積。 |crs-ps
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322003"
---
# <a name="crs---ps"></a>crs-ps

使用右手條規則來計算交叉乘積。

## <a name="syntax"></a>Syntax



| crs dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Crs                   |      |      |      |      | x    | x    | x     | x    | x     |



 

此指示的運作方式如下所示。


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



使用的一些限制：

-   src0 不可以是與 dest 相同的暫存器。
-   src1 不可以是與 dest 相同的暫存器。
-   src0 不能有預設 swizzle ( xyzw) 以外的任何 swizzle。
-   src1 不能有預設 swizzle ( xyzw) 以外的任何 swizzle。
-   dest 必須剛好有下列其中一個 yz：.. \| z. z. z. z. z. \| z. \| \| \| \|
-   dest 必須是臨時暫存器。
-   目的地不得與 src0 或 src1 相同的註冊

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




