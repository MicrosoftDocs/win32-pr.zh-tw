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
# <a name="creating-a-notification-sink"></a>建立通知接收

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

若要透過 Microsoft Agent 收到事件通知，您必須執行 [**IAgentNotifySink**](events.md)或 [**IAgentNotifySinkEx**](iagentnotifysinkex.md) 介面，並依照 COM 慣例，建立並註冊該型別的物件：


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



當您的應用程式關閉並釋放 Microsoft 代理程式的介面時，請記得取消註冊您的通知接收。

 

 




