---
title: lrp-ps
description: 在第二個和第三個來源暫存器之間，以第一個來源登錄中指定的比例，以線性方式插補 |lrp-ps
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 716cbdd5492f768885b8dd91dca5a17f72c4ba50897274c2d6e11f340f563394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906868"
---
# <a name="lrp---ps"></a>lrp-ps

在第二個和第三個來源暫存器之間，以第一個來源登錄中指定的比例，以線性方式插補

## <a name="syntax"></a>Syntax



| lrp dst、src0、src1、src2 收取 |
|---------------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。
-   src2 收取是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Lrp                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

此指示會根據下列公式來執行線性插補。


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




