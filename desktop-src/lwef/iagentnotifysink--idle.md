---
title: IAgentNotifySink 閒置
description: IAgentNotifySink 閒置
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968663"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="cf531-103">IAgentNotifySink：：閒置</span><span class="sxs-lookup"><span data-stu-id="cf531-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="cf531-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="cf531-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="cf531-105">當字元的 **閒置** 狀態變更時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf531-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="cf531-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf531-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cf531-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="cf531-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="cf531-108">啟動之要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf531-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="cf531-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span><span class="sxs-lookup"><span data-stu-id="cf531-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="cf531-110">開始旗標。</span><span class="sxs-lookup"><span data-stu-id="cf531-110">Start flag.</span></span> <span data-ttu-id="cf531-111">當字元開始閒置時，這個布林值是 **True** ，而當字元停止閒置時，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="cf531-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="cf531-112">此事件可讓您追蹤 Microsoft 代理程式伺服器啟動或停止閒置處理某個字元的時間。</span><span class="sxs-lookup"><span data-stu-id="cf531-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf531-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf531-113">See Also</span></span>

<span data-ttu-id="cf531-114">[**IAgentCharacter：： GetIdleOn**](iagentcharacter--getidleon.md)、 [ **IAgentCharacter：： SetIdleOn**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="cf531-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 




