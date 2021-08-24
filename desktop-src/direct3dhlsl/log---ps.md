---
title: 記錄-ps
description: Full precision log ₂ (x) 。 |記錄-ps
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4be7061b6e2e0bfa4fd86ffaeef1651cd114996bb9252192582f4c447aac09ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854148"
---
# <a name="log---ps"></a>記錄-ps

Full precision log ₂ (x) 。

## <a name="syntax"></a>Syntax



| 記錄 dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。 來源註冊需要明確使用複寫 swizzle;也就是，您必須指定一個. x、. y、z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| log                   |      |      |      |      | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示已執行的作業。


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



此指示會接受已忽略其正負號位的純量來源。 結果會複寫到所有的四個通道。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




