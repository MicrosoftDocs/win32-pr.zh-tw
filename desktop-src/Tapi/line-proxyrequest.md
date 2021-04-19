---
description: TAPI 線路 \_ PROXYREQUEST 訊息會將要求傳遞給已註冊的 proxy 函式處理常式。
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: 'LINE_PROXYREQUEST 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992920"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="a1300-103">行 \_ PROXYREQUEST 訊息</span><span class="sxs-lookup"><span data-stu-id="a1300-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="a1300-104">TAPI **線路 \_ PROXYREQUEST** 訊息會將要求傳遞給已註冊的 proxy 函式處理常式。</span><span class="sxs-lookup"><span data-stu-id="a1300-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a1300-105">參數</span><span class="sxs-lookup"><span data-stu-id="a1300-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1300-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a1300-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a1300-107">應用程式狀態已變更之線路裝置的應用程式控制碼。</span><span class="sxs-lookup"><span data-stu-id="a1300-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="a1300-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a1300-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a1300-109">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="a1300-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="a1300-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a1300-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a1300-111">[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)結構的指標，其中包含 proxy 處理常式應用程式要處理的要求。</span><span class="sxs-lookup"><span data-stu-id="a1300-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="a1300-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a1300-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a1300-113">保留的。</span><span class="sxs-lookup"><span data-stu-id="a1300-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1300-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a1300-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a1300-115">保留的。</span><span class="sxs-lookup"><span data-stu-id="a1300-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1300-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1300-116">Return value</span></span>

<span data-ttu-id="a1300-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a1300-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1300-118">備註</span><span class="sxs-lookup"><span data-stu-id="a1300-118">Remarks</span></span>

<span data-ttu-id="a1300-119">**該行 \_ PROXYREQUEST** 訊息只會傳送至第一個註冊的應用程式，以處理傳遞之類型的 proxy 要求。</span><span class="sxs-lookup"><span data-stu-id="a1300-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="a1300-120">應用程式應該處理 proxy 緩衝區中包含的要求，並呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) 來傳回資料或傳遞結果。</span><span class="sxs-lookup"><span data-stu-id="a1300-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="a1300-121">只有在應用程式的 TAPI 回呼函數可以立即執行時，才需要在應用程式的 TAPI 回呼函式內容中處理要求，而不需要等待任何其他實體的回應。</span><span class="sxs-lookup"><span data-stu-id="a1300-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="a1300-122">如果應用程式需要與其他實體通訊 (例如，用來處理 PBX 型 ACD 的服務提供者，或可能導致封鎖) 的任何其他系統服務，則要求應該在應用程式中排入佇列，而且回呼函式會結束，以避免應用程式延遲接收到其他的 TAPI 訊息。</span><span class="sxs-lookup"><span data-stu-id="a1300-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="a1300-123">當 **行 \_ PROXYREQUEST** 傳遞至 proxy 處理常式時，TAPI 已經將正面的 *dwRequestID* 函式結果傳回至原始應用程式，並解除封鎖呼叫執行緒以繼續執行。</span><span class="sxs-lookup"><span data-stu-id="a1300-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="a1300-124">應用程式正在等候 [**行 \_ 回復**](line-reply.md) 訊息，此訊息會在 proxy 處理常式應用程式呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)時自動產生。</span><span class="sxs-lookup"><span data-stu-id="a1300-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="a1300-125">應用程式不應釋放 *lpProxyRequest* 所指向的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a1300-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="a1300-126">TAPI 會在執行 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)期間釋出記憶體。</span><span class="sxs-lookup"><span data-stu-id="a1300-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="a1300-127">應用程式可以針對每 **一行 \_ PROXYREQUEST** 訊息只呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)一次。</span><span class="sxs-lookup"><span data-stu-id="a1300-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="a1300-128">如果應用程式在有擱置的 proxy 要求時收到 [**行 \_ 關閉**](line-close.md) 訊息，則應該為每個擱置中的要求呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) ，並傳入適當的 *dwResult* 值 (例如 LINEERR \_ OPERATIONFAILED) 。</span><span class="sxs-lookup"><span data-stu-id="a1300-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1300-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1300-129">Requirements</span></span>



| <span data-ttu-id="a1300-130">需求</span><span class="sxs-lookup"><span data-stu-id="a1300-130">Requirement</span></span> | <span data-ttu-id="a1300-131">值</span><span class="sxs-lookup"><span data-stu-id="a1300-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a1300-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a1300-132">TAPI version</span></span><br/> | <span data-ttu-id="a1300-133">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a1300-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a1300-134">標頭</span><span class="sxs-lookup"><span data-stu-id="a1300-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a1300-135"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="a1300-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1300-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1300-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1300-137">**行 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="a1300-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="a1300-138">**行 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="a1300-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="a1300-139">**LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="a1300-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="a1300-140">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="a1300-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




