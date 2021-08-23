---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e4f3fe070a944ecd9800a6712e8ae4db8d333913e5cfe85c027565cf1cf77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609378"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::GetHotKey

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

抓取語音輸入接聽按鍵的目前鍵盤指派。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

接收目前用來開啟語音輸入音訊頻道之熱鍵設定的 BSTR 位址。

</dd> </dl>

如果 [**GetEnabled**](iagentspeechinputproperties--getenabled.md) 傳回 **False**，則查詢此設定會引發錯誤。

## <a name="see-also"></a>另請參閱

[**IAgentSpeechInputProperties：： GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




