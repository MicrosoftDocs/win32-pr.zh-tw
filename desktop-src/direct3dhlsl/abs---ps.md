---
title: abs-ps
description: 計算絕對值。 |abs-ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 070a513aaa0d336d5ac404b1748fdd162edfd532
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321839"
---
# <a name="abs---ps"></a>abs-ps

計算絕對值。

## <a name="syntax"></a>Syntax



|              |
|--------------|
| abs dst、src |



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



|                       |      |      |      |      |      |      |       |      |       |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
| abs                   |      |      |      |      | x    | x    | x     | x    | x     |



 

此指示的運作方式如下所示。


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a>指示資訊



|                          |            |
|--------------------------|------------|
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




