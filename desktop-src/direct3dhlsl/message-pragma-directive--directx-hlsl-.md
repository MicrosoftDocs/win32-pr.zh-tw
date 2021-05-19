---
title: message pragma 指示詞
description: 產生編譯器時間訊息的 Pragma 指示詞。
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- message pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153481"
---
# <a name="message-pragma-directive"></a>message pragma 指示詞

產生編譯器時間訊息的 Pragma 指示詞。



| \#pragma message ( "*token-string*" )  |
|-----------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                    | 描述                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*<br/> | 編譯器訊息。<br/> |



 

## <a name="examples"></a>範例

下列範例示範在前置處理期間的訊息處理。


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\# (DirectX HLSL) 的 pragma 指示詞 ](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





