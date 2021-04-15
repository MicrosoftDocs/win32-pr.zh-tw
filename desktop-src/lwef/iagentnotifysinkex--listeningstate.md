---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507276"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="cb9a0-103">IAgentNotifySinkEx::ListeningState</span><span class="sxs-lookup"><span data-stu-id="cb9a0-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="cb9a0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="cb9a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="cb9a0-105">在接聽模式變更時通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="cb9a0-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cb9a0-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span><span class="sxs-lookup"><span data-stu-id="cb9a0-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="cb9a0-108">接聽狀態變更的字元。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a0-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span><span class="sxs-lookup"><span data-stu-id="cb9a0-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="cb9a0-110">接聽模式的狀態。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-110">The Listening mode state.</span></span> <span data-ttu-id="cb9a0-111">**True** 表示接聽模式已啟動; **False**，表示接聽模式已結束。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a0-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="cb9a0-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="cb9a0-113">事件的原因，可能是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="cb9a0-114">值</span><span class="sxs-lookup"><span data-stu-id="cb9a0-114">Value</span></span>                                                                             | <span data-ttu-id="cb9a0-115">描述</span><span class="sxs-lookup"><span data-stu-id="cb9a0-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cb9a0-116">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ PROGRAMDISABLED = 1;**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="cb9a0-117">程式碼已關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="cb9a0-118">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ PROGRAMTIMEDOUT = 2;**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="cb9a0-119">程式碼 (開啟接聽模式) 超時。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="cb9a0-120">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERTIMEDOUT = 3;**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="cb9a0-121">接聽 (開啟接聽模式) 超時。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="cb9a0-122">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERRELEASEDKEY = 4;**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="cb9a0-123">因為使用者放開接聽金鑰，所以已關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="cb9a0-124">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERUTTERANCEENDED = 5;**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="cb9a0-125">因為使用者已完成說話，所以已關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="cb9a0-126">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ CLIENTDEACTI加值稅ED = 6;**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="cb9a0-127">因為已停用輸入作用中用戶端，所以已關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="cb9a0-128">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ DEFAULTCHARCHANGE = 7**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="cb9a0-129">因為預設字元已變更，所以已關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="cb9a0-130">**const 不帶正負號的 long** **LSCOMPLETE \_ 導致 \_ USERDISABLED = 8**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="cb9a0-131">因為使用者停用語音輸入，所以已關閉接聽模式。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="cb9a0-132">當使用者按下接聽鍵或其超時時間結束時，或當輸入-主動用戶端使用 **True** 或 **False** 呼叫 [**IAgentCharacterEx：：接聽**](iagentcharacterex--listen.md)方法時，就會將此事件傳送至所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="cb9a0-133">此事件會將值傳回給目前已載入此字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="cb9a0-134">所有其他用戶端都會收到 null 字元， (空的字串) 。</span><span class="sxs-lookup"><span data-stu-id="cb9a0-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="cb9a0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb9a0-135">See Also</span></span>

[<span data-ttu-id="cb9a0-136">**IAgentCharacterEx：：接聽**</span><span class="sxs-lookup"><span data-stu-id="cb9a0-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 





