---
title: rsq-vs
description: 將交互平方根 (計算來源純量的) 。 |rsq-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974272"
---
# <a name="rsq---vs"></a>rsq-vs

將交互平方根 (計算來源純量的) 。

## <a name="syntax"></a>Syntax



| rsq dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| rsq                    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示已執行的作業。


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



在處理之前，會先取得絕對值。

精確度至少應該是 1.0/ (2 ²²) 範圍 (1.0，4.0) 的絕對錯誤，因為常見的實作為會分隔尾數和指數。

如果來源沒有下標，則會使用 x 元件。 如果輸入正好是1.0，則輸出必須正好為1.0。 0.0 的來源會產生無限大。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




