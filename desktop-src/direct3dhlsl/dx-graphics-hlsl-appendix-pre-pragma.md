---
title: " pragma 指示詞"
description: 預處理器指示詞，提供電腦特定或作業系統特有的功能，同時保留與 C 和 c + + 語言的整體相容性。
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022472"
---
# <a name="pragma-directive"></a>\#pragma 指示詞

預處理器指示詞，提供電腦特定或作業系統特有的功能，同時保留與 C 和 c + + 語言的整體相容性。



| \#pragma *token-字串* |
|-------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                    | 描述                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*<br/> | 提供特定編譯器指令和引數的字元系列。 此參數受限於宏展開。 <br/> |



 

## <a name="remarks"></a>備註

如果編譯器發現無法辨識的 pragma，則會發出警告，但編譯會繼續進行。

HLSL 編譯器會辨識下列 pragma：

-   [Def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [套件 \_ 矩陣](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





