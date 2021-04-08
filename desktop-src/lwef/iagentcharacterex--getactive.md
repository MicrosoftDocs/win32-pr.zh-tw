---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840540"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="f2653-103">IAgentCharacterEx::GetActive</span><span class="sxs-lookup"><span data-stu-id="f2653-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="f2653-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f2653-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="f2653-105">抓取用戶端應用程式是否為字元的作用中用戶端，以及字元是否最上層。</span><span class="sxs-lookup"><span data-stu-id="f2653-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="f2653-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f2653-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f2653-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span><span class="sxs-lookup"><span data-stu-id="f2653-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="f2653-108">變數的位址，此變數會接收狀態設定的下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f2653-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="f2653-109">值</span><span class="sxs-lookup"><span data-stu-id="f2653-109">Value</span></span>                                                              | <span data-ttu-id="f2653-110">描述</span><span class="sxs-lookup"><span data-stu-id="f2653-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f2653-111">**const 不帶正負號的 short** **ACTI加值稅E \_ NOTACTIVE = 0;**</span><span class="sxs-lookup"><span data-stu-id="f2653-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="f2653-112">您的用戶端不是字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="f2653-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="f2653-113">**const 不帶正負號短\*\*\*\*啟用使用中 \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="f2653-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="f2653-114">您的用戶端是字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="f2653-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="f2653-115">**const 不帶正負號的 short** **ACTI加值稅E \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="f2653-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="f2653-116">您的用戶端是輸入-主動 (最上層字元) 的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="f2653-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="f2653-117">這項設定可讓您知道您是字元的作用中用戶端，還是您的字元是否為輸入使用中的字元。</span><span class="sxs-lookup"><span data-stu-id="f2653-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="f2653-118">當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。</span><span class="sxs-lookup"><span data-stu-id="f2653-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="f2653-119">同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f2653-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="f2653-120">您可以使用 [**啟動**](iagentcharacter--activate.md) 方法來設定您的應用程式是字元的作用中用戶端，還是讓您的應用程式成為輸入使用中的用戶端 (也會讓字元) 最上層。</span><span class="sxs-lookup"><span data-stu-id="f2653-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="f2653-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2653-121">See Also</span></span>

<span data-ttu-id="f2653-122">[**IAgentCharacter：： Activate**](iagentcharacter--activate.md)、 [ **IAgentNotifySinkEx：： ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="f2653-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 





