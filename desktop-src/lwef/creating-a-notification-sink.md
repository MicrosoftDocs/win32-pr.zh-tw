---
title: 建立通知接收
description: 建立通知接收
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372603"
---
# <a name="creating-a-notification-sink"></a><span data-ttu-id="62004-103">建立通知接收</span><span class="sxs-lookup"><span data-stu-id="62004-103">Creating a Notification Sink</span></span>

<span data-ttu-id="62004-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="62004-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="62004-105">若要透過 Microsoft Agent 收到事件通知，您必須執行 [**IAgentNotifySink**](events.md)或 [**IAgentNotifySinkEx**](iagentnotifysinkex.md) 介面，並依照 COM 慣例，建立並註冊該型別的物件：</span><span class="sxs-lookup"><span data-stu-id="62004-105">To be notified of events by Microsoft Agent, you must implement either the [**IAgentNotifySink**](events.md)or the [**IAgentNotifySinkEx**](iagentnotifysinkex.md) interface, and create and register an object of that type following COM conventions:</span></span>


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



<span data-ttu-id="62004-106">當您的應用程式關閉並釋放 Microsoft 代理程式的介面時，請記得取消註冊您的通知接收。</span><span class="sxs-lookup"><span data-stu-id="62004-106">Remember to unregister your notification sink when your application shuts down and releases Microsoft Agent's interfaces.</span></span>

 

 




