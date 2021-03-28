---
title: ret-vs
description: 從副程式或 main 函數返回。
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313652"
---
# <a name="ret---vs"></a>ret-vs

從副程式或 main 函數返回。

## <a name="syntax"></a>Syntax



| Ret |
|-----|



 

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Ret                    |      | x    | x    | x     | x    | x     |



 

此指令會從傳回位址堆疊取得指示的位址，並繼續執行。 在 main 函式的情況下，此指令會停止著色器的執行。

Ret 指令會使用一個頂點著色器指令位置。

如果著色器未包含任何副程式，則在 main 程式結尾使用 ret 是選擇性的。

Main 程式或任何副程式中不允許有多個 return 語句，第一個 return 語句會被視為 main 程式或副程式的結尾。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




