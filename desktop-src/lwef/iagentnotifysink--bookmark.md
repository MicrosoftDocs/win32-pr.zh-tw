---
title: IAgentNotifySink 書簽
description: IAgentNotifySink 書簽
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477094"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink：： Bookmark

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

當用戶端應用程式的書簽完成時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

導致觸發事件的書簽識別碼。

</dd> </dl>

當您在「 [**說話**](speak-method.md) 」方法中包含書簽標記時，您可以追蹤這些標記何時發生此事件。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：：說**](iagentcharacter--speak.md)， [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md)


 

 




