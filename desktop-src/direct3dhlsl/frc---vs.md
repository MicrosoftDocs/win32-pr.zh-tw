---
title: frc-vs
description: 傳回每個輸入元件的小數部分。 |frc-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2ecc6a1c903f78fb7c03442809f792e3ddb984d04975d3f5ecb0b5c918f7ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907641"
---
# <a name="frc---vs"></a>frc-vs

傳回每個輸入元件的小數部分。

## <a name="syntax"></a>Syntax



| frc dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Frc                    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會以概念方式顯示指令的運作方式。


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



Floor 函數會將傳入的引數轉換成小於 (或等於) 引數的最大整數。 這會轉換成浮點數，然後將原始值減去從。 產生的小數值範圍從0.0 到1.0。

在第1版 \_ 中，允許的寫入遮罩是. y 和 xy (. x 不允許) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




