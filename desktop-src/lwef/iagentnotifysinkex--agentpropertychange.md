---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932225"
---
# <a name="iagentnotifysinkexagentpropertychange"></a><span data-ttu-id="b2f08-103">IAgentNotifySinkEx::AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="b2f08-103">IAgentNotifySinkEx::AgentPropertyChange</span></span>

<span data-ttu-id="b2f08-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b2f08-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AgentPropertyChange(
);
```

<span data-ttu-id="b2f08-105">當使用者變更 Microsoft Agent 屬性設定時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="b2f08-105">Notifies a client application when the user changes a Microsoft Agent property setting.</span></span>

-   <span data-ttu-id="b2f08-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b2f08-106">No return value.</span></span>

<span data-ttu-id="b2f08-107">當使用者變更 Microsoft Agent 屬性工作表中的 Microsoft Agent 內容設定時，除非伺服器目前已暫停，否則伺服器會將此事件傳送給所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="b2f08-107">When the user changes a Microsoft Agent property setting in the Microsoft Agent property sheet, the server sends this event to all clients unless the server is currently suspended.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2f08-108">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2f08-108">See Also</span></span>

[<span data-ttu-id="b2f08-109">**IAgentNotifySinkEx：:D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="b2f08-109">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 




