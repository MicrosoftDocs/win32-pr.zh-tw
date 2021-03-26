---
title: 來源登錄反轉
description: 針對指定之註冊的每個通道，執行 (1 值) 計算。
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971456"
---
# <a name="source-register-invert"></a>來源登錄反轉

針對指定之註冊的每個通道，執行 (1 值) 計算。

## <a name="syntax"></a>Syntax


```
1 - register
```



## <a name="registers"></a>暫存器

來源註冊。 如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="remarks"></a>備註

註冊的內容不會變更。 修飾詞只會套用至從註冊讀取的資料。  (RGBA) 的所有四色通道都會套用反向運算。

此修飾詞只能搭配算術指令使用。 此外，此修飾詞不能與其他 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)合併。

## <a name="example"></a>範例

此範例會使用反轉來產生 register r1 的補數。


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




