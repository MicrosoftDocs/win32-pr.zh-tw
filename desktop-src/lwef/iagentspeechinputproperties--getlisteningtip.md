---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966775"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

抓取值，指出是否啟用接聽提示來顯示。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

如果已啟用接聽提示以顯示，則為 **True** 的變數位址; 如果停用接聽提示，則為 **False** 。

</dd> </dl>

如果 [**GetEnabled**](iagentspeechinputproperties--getenabled.md) 傳回 **False**，則查詢其他任何語音輸入屬性會傳回錯誤。

## <a name="see-also"></a>另請參閱

[**IAgentSpeechInputProperties：： GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




