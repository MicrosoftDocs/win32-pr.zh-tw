---
title: 處理要求
description: 處理要求包含四個步驟。
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "103853231"
---
# <a name="processing-requests"></a><span data-ttu-id="680b4-103">處理要求</span><span class="sxs-lookup"><span data-stu-id="680b4-103">Processing Requests</span></span>

<span data-ttu-id="680b4-104">處理要求包含四個步驟：</span><span class="sxs-lookup"><span data-stu-id="680b4-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="680b4-105">接收要求</span><span class="sxs-lookup"><span data-stu-id="680b4-105">Receiving a request</span></span>
-   <span data-ttu-id="680b4-106">處理要求</span><span class="sxs-lookup"><span data-stu-id="680b4-106">Handling the request</span></span>
-   <span data-ttu-id="680b4-107">傳送回應</span><span class="sxs-lookup"><span data-stu-id="680b4-107">Sending the response</span></span>
-   <span data-ttu-id="680b4-108">正在取消無法處理的要求</span><span class="sxs-lookup"><span data-stu-id="680b4-108">Canceling requests that cannot be processed</span></span>

![顯示進程要求迴圈的圖表。](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="680b4-110">接收要求</span><span class="sxs-lookup"><span data-stu-id="680b4-110">Receiving a Request</span></span>

<span data-ttu-id="680b4-111">HTTP 伺服器 API 會提供一個要求結構來儲存剖析的連入要求。</span><span class="sxs-lookup"><span data-stu-id="680b4-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="680b4-112">此結構是由應用程式所配置，並在收到傳入要求時初始化。</span><span class="sxs-lookup"><span data-stu-id="680b4-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="680b4-113">應用程式會呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 函數來接收要求。</span><span class="sxs-lookup"><span data-stu-id="680b4-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="680b4-114">如果要求緩衝區太小而無法接收要求，應用程式可以增加緩衝區大小，然後再次呼叫 **HttpReceiveHttpRequest** ，以接收整個要求。</span><span class="sxs-lookup"><span data-stu-id="680b4-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="680b4-115">如果要求包含要接收的實體主體資料，則應用程式會在呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)期間以 *pRequestBuffer* 參數傳回的要求識別碼來呼叫 [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) 。</span><span class="sxs-lookup"><span data-stu-id="680b4-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="680b4-116">處理要求</span><span class="sxs-lookup"><span data-stu-id="680b4-116">Handling the Request</span></span>

<span data-ttu-id="680b4-117">應用程式會執行要求的應用程式特定處理，並會構成回應。</span><span class="sxs-lookup"><span data-stu-id="680b4-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="680b4-118">HTTP 伺服器 API 不會在此程式上強加任何時間。</span><span class="sxs-lookup"><span data-stu-id="680b4-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="680b4-119">傳送回應</span><span class="sxs-lookup"><span data-stu-id="680b4-119">Sending the Response</span></span>

<span data-ttu-id="680b4-120">當應用程式完成處理要求並編寫回應時，它會呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 函式來傳送回應。</span><span class="sxs-lookup"><span data-stu-id="680b4-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="680b4-121">如果回應包含要傳送的實體主體資料，則應用程式也會呼叫 [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)。</span><span class="sxs-lookup"><span data-stu-id="680b4-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="680b4-122">取消要求</span><span class="sxs-lookup"><span data-stu-id="680b4-122">Canceling Requests</span></span>

<span data-ttu-id="680b4-123">應用程式從呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)收到要求識別碼之後，就可以在任何時候呼叫 [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)來取消要求。</span><span class="sxs-lookup"><span data-stu-id="680b4-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




