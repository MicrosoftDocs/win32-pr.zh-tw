---
title: '\_ \_ 適用于 texld、texcrd 的 ps 1 4 來源登錄修飾詞'
description: 雙圖元著色器第1版 \_ 的材質位址指示（texld-ps \_ 1 \_ 4 和 texcrd-ps）有自訂語法。
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104092483"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>\_ \_ 適用于 texld、texcrd 的 ps 1 4 來源登錄修飾詞

雙圖元著色器第1版 \_ 的材質位址指示（ [texld-ps \_ 1 \_ 4](texld---ps-1-4.md) 和 [texcrd-ps](texcrd---ps.md)）有自訂語法。 這些指示支援自己的一組來源登錄修飾詞、來源登錄選取器，以及目的地登錄寫入遮罩，如下所示。

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Texld 和 texcrd 的來源登錄修飾詞

這些修飾詞會將 x 和 y 值除以 z 或 w 值，以提供 projective 分割功能。



| 來源暫存器修飾符 | 描述                | 語法       |
|---------------------------|----------------------------|--------------|
| \_Dz                      | 以 z 分隔 x、y 元件 | 註冊 \_ dz |
| \_db                      | 以 z 分隔 x、y 元件 | 註冊 \_ db |
| \_dw                      | 將 x、y 元件除以 w | 註冊 \_ dw |
| \_大                      | 將 x、y 元件除以 w | 註冊 \_ da |



 

### <a name="remarks"></a>備註

\_Dz 或 \_ db 修飾詞會執行下列動作：


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



\_Dw 或 \_ da 修飾詞會執行下列動作：


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




