---
description: 定義一組動畫索引鍵。 矩陣索引鍵適用于需要以轉換矩陣表示的動畫資料集。
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972568"
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

 

 



