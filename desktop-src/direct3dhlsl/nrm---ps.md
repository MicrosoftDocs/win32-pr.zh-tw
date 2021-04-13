---
title: nrm-ps
description: 標準化3D 向量。 |nrm-ps
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322120"
---
# <a name="nrm---ps"></a>nrm-ps

標準化3D 向量。

## <a name="syntax"></a>Syntax



| nrm dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| nrm                   |      |      |      |      | x    | x    | x     | x    | x     |



 

此指示在概念上的運作方式如下所示。

squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z) <sup>1/2</sup>;


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



目的地和 src 暫存器不可以相同。 目的地暫存器必須是臨時暫存器。

此指示會根據下列公式來執行線性插補。


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




