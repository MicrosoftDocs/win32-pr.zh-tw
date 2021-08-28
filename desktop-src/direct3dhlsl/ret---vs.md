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
ms.openlocfilehash: 6bec0356f2f1542da421a807598707e4857033c13cda2077d9281ac24e4fc3e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853768"
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

 

 




