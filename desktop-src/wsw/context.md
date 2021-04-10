---
title: 'Windows Web 服務的內容 () '
description: 內容會在服務模型服務作業和回呼中用來將相關的狀態資料傳遞至服務作業或回呼（當叫用時）。
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- 適用于 Windows 的內容 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103932833"
---
# <a name="context-windows-web-services"></a><span data-ttu-id="3d12a-106">Windows Web 服務的內容 () </span><span class="sxs-lookup"><span data-stu-id="3d12a-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="3d12a-107">內容會在服務模型 [服務作業](service-operation.md) 和回呼中用來將相關的狀態資料傳遞至服務作業或回呼（當叫用時）。</span><span class="sxs-lookup"><span data-stu-id="3d12a-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="3d12a-108">內容是由 [WS \_ 操作 \_ 內容](ws-operation-context.md) 結構所參考。</span><span class="sxs-lookup"><span data-stu-id="3d12a-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="3d12a-109">您可以使用 [**WsGetOperationCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) 函數來抓取內容的屬性，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="3d12a-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="3d12a-110">並非所有內容屬性都可在任何指定時間使用。</span><span class="sxs-lookup"><span data-stu-id="3d12a-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="3d12a-111">請參閱有關回呼或 [服務](service-operation.md)作業中特定屬性可用性的內容屬性檔。</span><span class="sxs-lookup"><span data-stu-id="3d12a-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="3d12a-112">如需如何維護作業內容存留期和執行緒的詳細資訊，請參閱 [操作內容存留期和執行緒](operation-context-lifetime-and-threading.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="3d12a-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="3d12a-113">下列列舉是內容的一部分：</span><span class="sxs-lookup"><span data-stu-id="3d12a-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="3d12a-114">**WS \_ 操作 \_ 上下文 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="3d12a-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="3d12a-115">下列函數是內容的一部分：</span><span class="sxs-lookup"><span data-stu-id="3d12a-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="3d12a-116">**WsGetOperationCoNtextProperty**</span><span class="sxs-lookup"><span data-stu-id="3d12a-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="3d12a-117">下列控制碼是內容的一部分：</span><span class="sxs-lookup"><span data-stu-id="3d12a-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="3d12a-118">WS \_ 操作 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="3d12a-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




