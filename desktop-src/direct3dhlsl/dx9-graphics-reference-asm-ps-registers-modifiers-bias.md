---
title: 來源註冊偏差
description: 從所有元件減去0.5。
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932585"
---
# <a name="source-register-bias"></a>來源註冊偏差

從所有元件減去0.5。

## <a name="registers"></a>暫存器

來源註冊。 如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="remarks"></a>備註

註冊的內容不會變更。 修飾詞只會套用至從註冊讀取的資料。 偏差會套用至所有四色通道 (RGBA) 如下所示：


```
output = (input - 0.5)
```



效果是修改範圍介於0到1之間的資料，範圍從-0.5 到0.5。 將偏差套用到此範圍以外的資料可能會產生未定義的結果。

> [!Note]  
> 此修飾詞與來源登錄 [反轉](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)互斥，因此無法套用至相同的暫存器。

 

此修飾詞用於算術指令。

## <a name="example"></a>範例

此範例會執行與 \_ DirectX 6.0 和7.0 多重紋理語法中的 D3DTOP ADDSIGNED 相同的作業。


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




