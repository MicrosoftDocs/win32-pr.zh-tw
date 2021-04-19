---
title: 取消方法呼叫
description: 隨著分散式和 Web 應用程式的推出，某些方法呼叫可能會花費很長的時間才能傳回。
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966891"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="4e938-103">取消方法呼叫</span><span class="sxs-lookup"><span data-stu-id="4e938-103">Canceling Method Calls</span></span>

<span data-ttu-id="4e938-104">隨著分散式和 Web 應用程式的推出，某些方法呼叫可能會花費很長的時間才能傳回。</span><span class="sxs-lookup"><span data-stu-id="4e938-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="4e938-105">網路連線的延遲可能很高，伺服器電腦可能會服務許多用戶端，或者伺服器元件可能傳遞大量資料，例如多媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="4e938-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="4e938-106">使用者應該能夠取消花費太長時間的要求，而且應用程式應該能夠處理取消要求，並繼續執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="4e938-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="4e938-107">在 COM 中，您可以使用 [**imessagefilter.prefiltermessage**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) 介面來取消源自單一執行緒單元的暫止呼叫。</span><span class="sxs-lookup"><span data-stu-id="4e938-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="4e938-108">當呼叫被封送處理時，proxy 會建立一個可實 [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) 介面的 cancel 物件。</span><span class="sxs-lookup"><span data-stu-id="4e938-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="4e938-109">Cancel 物件與呼叫暫止的呼叫和執行緒相關聯。</span><span class="sxs-lookup"><span data-stu-id="4e938-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="4e938-110">若要解除擱置中的呼叫，用戶端會透過 cancel 物件傳遞取消要求，此物件會處理通知伺服器物件已取消呼叫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4e938-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="4e938-111">如果所呼叫的方法尚未傳回，伺服器物件在偵測取消要求時，會清除它已配置的任何程式資源，並藉由傳回適當的 **HRESULT** 值來通知其用戶端，以取消執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="4e938-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="4e938-112">如果已傳回呼叫的方法，cancel 物件會通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="4e938-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="4e938-113">無論是哪一種情況，用戶端執行緒都會解除封鎖，並可繼續處理。</span><span class="sxs-lookup"><span data-stu-id="4e938-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="4e938-114">伺服器物件對取消要求的回應是由伺服器實施者自行決定，但是用戶端上的呼叫執行緒一律會解除封鎖，並忽略伺服器嘗試傳遞給它的任何結果。</span><span class="sxs-lookup"><span data-stu-id="4e938-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="4e938-115">Cancel 物件提供一種方法來要求取消目前正在執行的方法，但是無法保證伺服器物件將停止處理呼叫。</span><span class="sxs-lookup"><span data-stu-id="4e938-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="4e938-116">例如，呼叫可能已經傳回，或伺服器物件可能不支援取消物件。</span><span class="sxs-lookup"><span data-stu-id="4e938-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="4e938-117">COM 會針對使用標準封送處理的用戶端物件和介面，自動提供取消物件的標準執行。</span><span class="sxs-lookup"><span data-stu-id="4e938-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="4e938-118">若為使用自訂封送處理的物件和介面，您將必須執行您自己的 cancel 物件。</span><span class="sxs-lookup"><span data-stu-id="4e938-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="4e938-119">現在，cancel 物件只會處理同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="4e938-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e938-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e938-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e938-121">取消非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="4e938-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="4e938-122">**CoGetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="4e938-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="4e938-123">**CoSetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="4e938-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="4e938-124">**CoTestCancel**</span><span class="sxs-lookup"><span data-stu-id="4e938-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 