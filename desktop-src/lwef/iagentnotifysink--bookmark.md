---
title: IAgentNotifySink 書簽
description: IAgentNotifySink 書簽
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672407"
---
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="e600f-103">IAgentNotifySink：： Bookmark</span><span class="sxs-lookup"><span data-stu-id="e600f-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="e600f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e600f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="e600f-105">當用戶端應用程式的書簽完成時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="e600f-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="e600f-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e600f-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="e600f-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span><span class="sxs-lookup"><span data-stu-id="e600f-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="e600f-108">導致觸發事件的書簽識別碼。</span><span class="sxs-lookup"><span data-stu-id="e600f-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="e600f-109">當您在「 [**說話**](speak-method.md) 」方法中包含書簽標記時，您可以追蹤這些標記何時發生此事件。</span><span class="sxs-lookup"><span data-stu-id="e600f-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="e600f-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e600f-110">See Also</span></span>

<span data-ttu-id="e600f-111">[**IAgentCharacter：：說**](iagentcharacter--speak.md)， [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="e600f-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




