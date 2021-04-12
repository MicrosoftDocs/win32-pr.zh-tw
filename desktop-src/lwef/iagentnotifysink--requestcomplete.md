---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301879"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="48517-103">IAgentNotifySink::RequestComplete</span><span class="sxs-lookup"><span data-stu-id="48517-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="48517-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="48517-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="48517-105">當要求完成時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="48517-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="48517-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="48517-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="48517-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="48517-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="48517-108">啟動之要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="48517-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="48517-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span><span class="sxs-lookup"><span data-stu-id="48517-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="48517-110">狀態碼。</span><span class="sxs-lookup"><span data-stu-id="48517-110">Status code.</span></span> <span data-ttu-id="48517-111">此參數會傳回要求的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="48517-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="48517-112">此事件可讓您使用其要求識別碼來追蹤佇列方法完成的時間。</span><span class="sxs-lookup"><span data-stu-id="48517-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="48517-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48517-113">See Also</span></span>

<span data-ttu-id="48517-114">[**IAgentNotifySink：： RequestStart**](iagentnotifysink--requeststart.md)、 [**IAgent：： Load**](iagent--load.md)、 [**IAgentCharacter：： GestureAt**](iagentcharacter--gestureat.md)、 [**IAgentCharacter：： Hide**](iagentcharacter--hide.md)、 [**IAgentCharacter：：中斷**](iagentcharacter--interrupt.md)、 [**IAgentCharacter：： MoveTo**](iagentcharacter--moveto.md)、 [**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)、 [**IAgentCharacter：:P**](iagentcharacter--play.md)配置、 [**IAgentCharacter：： Show**](iagentcharacter--show.md)、 [**IAgentCharacter：：說話**](iagentcharacter--speak.md)、 [**IAgentCharacter：： Wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="48517-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




