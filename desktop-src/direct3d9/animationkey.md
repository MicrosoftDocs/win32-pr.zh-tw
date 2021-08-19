---
description: 定義一組動畫索引鍵。 矩陣索引鍵適用于需要以轉換矩陣表示的動畫資料集。
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bad23a6cc519b0b0525cd0dac1b488184b3bf91e99359e252f44dca435ace529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806403"
---
# <a name="animationkey"></a>AnimationKey

定義一組動畫索引鍵。 矩陣索引鍵適用于需要以轉換矩陣表示的動畫資料集。

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

其中：

-   keyType-使用整數0、1、2或3分別) ，指定索引鍵為旋轉、縮放、位置或矩陣鍵 (。
-   nKeys-索引鍵數目。
-   索引鍵-索引鍵的陣列。 請參閱 [**TimedFloatKeys**](timedfloatkeys.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



