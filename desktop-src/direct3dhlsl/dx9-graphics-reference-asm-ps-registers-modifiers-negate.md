---
title: 來源註冊否定
description: 在所有的暫存器元件上執行 (y x) 的否定。
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94898dbbf193254165850ee696d2fea72d6d446908021dfbb5fd32f1920b7010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512949"
---
# <a name="source-register-negate"></a>來源註冊否定

在所有的暫存器元件上執行 (y =-x) 的否定。

## <a name="syntax"></a>Syntax


```
- register
```



## <a name="registers"></a>暫存器

來源註冊。 如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="remarks"></a>備註

註冊的內容不會變更。 修飾詞只會套用至從註冊讀取的資料。 「否定」作業會套用至所有四色通道 (RGBA) 。

這項作業會在相同引數上出現的任何其他修飾詞之後執行。

此修飾詞與 [來源](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) 暫存器有互斥，因此無法套用至相同的暫存器。

此修飾詞僅用於算術指令。

## <a name="example"></a>範例

下列範例會示範如何使用這個修飾詞。


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




