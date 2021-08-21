---
title: mov-vs
description: 移動暫存器之間的浮點數據。
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dd3e476c871bf2c8d1e48075a3f43576283efff1df285f900c6d0194cf4bbbfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906729"
---
# <a name="mov---vs"></a>mov-vs

移動暫存器之間的浮點數據。

## <a name="syntax"></a>Syntax



| mov dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 平均線                    | x    | x    | x    | x     | x    | x     |



 

可以用於浮點數據。 針對版本與 \_ 1 \_ 1，也可以使用它來寫入位址註冊。 當用來更新位址暫存器時，會使用四捨五入到最接近的位置，從浮點數轉換值。

下列程式碼片段會顯示已執行的作業。


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




