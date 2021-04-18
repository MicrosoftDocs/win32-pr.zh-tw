---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965374"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="7cc67-103">IAgentNotifySinkEx::ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="7cc67-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="7cc67-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7cc67-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="7cc67-105">如果用戶端應用程式的作用中用戶端不再是字元的作用中用戶端，則會通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="7cc67-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="7cc67-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="7cc67-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="7cc67-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="7cc67-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="7cc67-108">作用中用戶端狀態變更之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7cc67-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="7cc67-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span><span class="sxs-lookup"><span data-stu-id="7cc67-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="7cc67-110">用戶端的作用中狀態變更，可以是下列任何一個值的組合：</span><span class="sxs-lookup"><span data-stu-id="7cc67-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="7cc67-111">值</span><span class="sxs-lookup"><span data-stu-id="7cc67-111">Value</span></span>                                                              | <span data-ttu-id="7cc67-112">描述</span><span class="sxs-lookup"><span data-stu-id="7cc67-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7cc67-113">**const 不帶正負號的 short** **ACTI加值稅E \_ NOTACTIVE = 0;**</span><span class="sxs-lookup"><span data-stu-id="7cc67-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="7cc67-114">您的用戶端不是字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="7cc67-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="7cc67-115">**const 不帶正負號短\*\*\*\*啟用使用中 \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="7cc67-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="7cc67-116">您的用戶端是字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="7cc67-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="7cc67-117">**const 不帶正負號的 short** **ACTI加值稅E \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="7cc67-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="7cc67-118">您的用戶端是輸入-主動 (最上層字元) 的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="7cc67-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="7cc67-119">當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。</span><span class="sxs-lookup"><span data-stu-id="7cc67-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="7cc67-120">同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="7cc67-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="7cc67-121">當使用中用戶端的字元變更時，此事件會傳回該字元的識別碼，如果您的應用程式已成為字元的作用中用戶端， **則為 True** ; 如果不再是字元的作用中用戶端，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="7cc67-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="7cc67-122">當使用者在字元的快顯功能表中選取其他用戶端應用程式的專案，或使用 [語音] 命令、用戶端應用程式變更其作用中狀態，或其他用戶端應用程式結束其與 Microsoft Agent 的連接時，用戶端應用程式可能會收到此事件。</span><span class="sxs-lookup"><span data-stu-id="7cc67-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="7cc67-123">代理程式只會將此事件傳送給直接受影響的用戶端應用程式，這些應用程式會變成作用中用戶端或停止成為作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="7cc67-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="7cc67-124">您可以使用 [**啟動**](iagentcharacter--activate.md) 方法來設定您的應用程式是字元的作用中用戶端，還是讓您的應用程式成為輸入-主動用戶端 (也會讓字元) 最上層。</span><span class="sxs-lookup"><span data-stu-id="7cc67-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc67-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cc67-125">See Also</span></span>

<span data-ttu-id="7cc67-126">[**IAgentCharacter：： Activate**](iagentcharacter--activate.md)、 [**IAgentCharacterEx：： GetActive**](iagentcharacterex--getactive.md)、 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="7cc67-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 





