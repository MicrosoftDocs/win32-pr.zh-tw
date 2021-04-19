---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106978566"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="96f28-103">IAgentNotifySink::BalloonVisibleState</span><span class="sxs-lookup"><span data-stu-id="96f28-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="96f28-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="96f28-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="96f28-105">當字元的單字氣球的可見度狀態變更時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="96f28-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="96f28-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="96f28-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="96f28-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="96f28-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="96f28-108">文字提示的可見度狀態已變更之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96f28-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="96f28-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="96f28-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="96f28-110">可見度旗標。</span><span class="sxs-lookup"><span data-stu-id="96f28-110">Visibility flag.</span></span> <span data-ttu-id="96f28-111">當字元的文字氣球變成可見時，此布林值為 **True** 。如果變成隱藏，則 **為 False** 。</span><span class="sxs-lookup"><span data-stu-id="96f28-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="96f28-112">此事件會傳送到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="96f28-112">This event is sent to all clients of the character.</span></span>

 

 




