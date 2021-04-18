---
title: IAgentCharacter 啟用
description: IAgentCharacter 啟用
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507472"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="3822a-103">IAgentCharacter：： Activate</span><span class="sxs-lookup"><span data-stu-id="3822a-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="3822a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3822a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="3822a-105">設定用戶端是否為使用中或字元是否最上層。</span><span class="sxs-lookup"><span data-stu-id="3822a-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="3822a-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="3822a-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="3822a-107">傳回 \_ FALSE，表示作業不成功。</span><span class="sxs-lookup"><span data-stu-id="3822a-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="3822a-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span><span class="sxs-lookup"><span data-stu-id="3822a-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="3822a-109">您可以為此參數指定下列值：</span><span class="sxs-lookup"><span data-stu-id="3822a-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="3822a-110">值</span><span class="sxs-lookup"><span data-stu-id="3822a-110">Value</span></span> | <span data-ttu-id="3822a-111">描述</span><span class="sxs-lookup"><span data-stu-id="3822a-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="3822a-112">0</span><span class="sxs-lookup"><span data-stu-id="3822a-112">0</span></span>     | <span data-ttu-id="3822a-113">設定為非作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-113">Set as not the active client.</span></span> |
| <span data-ttu-id="3822a-114">1</span><span class="sxs-lookup"><span data-stu-id="3822a-114">1</span></span>     | <span data-ttu-id="3822a-115">設定為使用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-115">Set as the active client.</span></span>     |
| <span data-ttu-id="3822a-116">2</span><span class="sxs-lookup"><span data-stu-id="3822a-116">2</span></span>     | <span data-ttu-id="3822a-117">將最上層的字元設為最上層。</span><span class="sxs-lookup"><span data-stu-id="3822a-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="3822a-118">當有多個字元可見時，一次只能有一個字元接收語音輸入。</span><span class="sxs-lookup"><span data-stu-id="3822a-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="3822a-119">同樣地，當多個用戶端應用程式共用相同的字元時，只有其中一個用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 一次。</span><span class="sxs-lookup"><span data-stu-id="3822a-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="3822a-120">用來接收滑鼠和語音輸入的字元集是最上層的字元，而接收輸入的用戶端是字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="3822a-121"> (最頂端的字元視窗也會出現在字元視窗的迭置順序頂端。 ) 一般是由使用者明確選取時，判斷哪一個字元最上層。</span><span class="sxs-lookup"><span data-stu-id="3822a-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="3822a-122">不過，當字元顯示或隱藏 (字元變成或不再是最上層時，最上層啟用也會變更。 ) </span><span class="sxs-lookup"><span data-stu-id="3822a-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="3822a-123">您也可以使用這個方法，在用戶端收到導向字元的輸入時明確管理，例如當您的應用程式本身變成作用中時。</span><span class="sxs-lookup"><span data-stu-id="3822a-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="3822a-124">例如，將 [ **狀態** ] 設定為 [2] 會將字元設為最上層，而您的用戶端會接收使用者與該字元互動所產生的所有滑鼠和語音輸入事件。</span><span class="sxs-lookup"><span data-stu-id="3822a-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="3822a-125">因此，它也會讓您的用戶端成為字元的輸入主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="3822a-126">不過，您也可以將 [ **狀態** ] 設定為 [1]，為字元設定使用中用戶端，而不讓字元最上層。</span><span class="sxs-lookup"><span data-stu-id="3822a-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="3822a-127">這可讓您的用戶端在字元變成最上層時，接收導向該字元的輸入。</span><span class="sxs-lookup"><span data-stu-id="3822a-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="3822a-128">同樣地，您可以將用戶端設定為非作用中的用戶端 (不會在字元變成最上層時，藉由將 **狀態** 設為0來接收輸入) 。</span><span class="sxs-lookup"><span data-stu-id="3822a-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="3822a-129">您可以使用 [**IAgentCharacter：： HasOtherClients**](iagentcharacter--hasotherclients.md)來判斷某個字元是否有其他目前的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="3822a-130">避免直接在 [**Show**](iagentcharacter--show.md) 方法之後呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="3822a-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="3822a-131">**顯示** 自動設定輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="3822a-132">隱藏字元時，如果在 **Show** 方法完成之前處理，**啟動** 呼叫可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="3822a-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="3822a-133">當指定的字元隱藏時，嘗試以 **State** 參數設定為 2 () 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3822a-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="3822a-134">同樣地，如果您將 **狀態** 設定為0，而您的應用程式是唯一的用戶端，則此呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="3822a-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="3822a-135">字元必須一律具有最上層的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3822a-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="3822a-136">除非沒有載入任何其他字元，或您的應用程式已經輸入-主動，否則以將 **狀態** 設定為1的方法呼叫此方法通常不會產生 [**AgentNotifySink：： ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) 事件。</span><span class="sxs-lookup"><span data-stu-id="3822a-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="3822a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3822a-137">See Also</span></span>

[<span data-ttu-id="3822a-138">**IAgentCharacter::HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="3822a-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 




