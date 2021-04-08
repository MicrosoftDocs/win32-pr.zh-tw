---
title: IAgent 註冊
description: IAgent 註冊
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840124"
---
# <a name="iagentregister"></a><span data-ttu-id="08617-103">IAgent：： Register</span><span class="sxs-lookup"><span data-stu-id="08617-103">IAgent::Register</span></span>

<span data-ttu-id="08617-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="08617-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="08617-105">註冊用戶端應用程式的通知接收。</span><span class="sxs-lookup"><span data-stu-id="08617-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="08617-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="08617-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="08617-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="08617-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="08617-108">通知接收介面的 [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) 位址。</span><span class="sxs-lookup"><span data-stu-id="08617-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="08617-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span><span class="sxs-lookup"><span data-stu-id="08617-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="08617-110">通知接收識別碼 (用來取消註冊通知接收) 的位址。</span><span class="sxs-lookup"><span data-stu-id="08617-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="08617-111">您必須註冊通知接收 (也稱為通知接收或事件接收) ，才能從 Microsoft 代理程式伺服器接收事件。</span><span class="sxs-lookup"><span data-stu-id="08617-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="08617-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08617-112">See Also</span></span>

[<span data-ttu-id="08617-113">**IAgent：：取消註冊**</span><span class="sxs-lookup"><span data-stu-id="08617-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




