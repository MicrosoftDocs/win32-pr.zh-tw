---
title: " error 指示詞"
description: 產生編譯器時間錯誤訊息的預處理器指示詞。
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- error 指示詞 HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373034"
---
# <a name="error-directive"></a>\#error 指示詞

產生編譯器時間錯誤訊息的預處理器指示詞。



| \#錯誤 *標記-字串* |
|------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                    | 描述                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*<br/> | 錯誤訊息。 這個參數是由一系列的 token 所組成，例如關鍵字、常數或完整語句。 標記字串受限於宏展開。 <br/> |



 

## <a name="remarks"></a>備註

\#error 指示詞最適合用來偵測程式設計師不一致，並在前置處理期間違反條件約束。 當遇到 error 指示詞時 \# ，編譯就會終止。

## <a name="examples"></a>範例

下列範例示範前置處理期間的錯誤處理。


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





