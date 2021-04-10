---
title: HTTP 伺服器工作
description: HTTP 伺服器工作通常會以特定循序執行;也就是說，必須完成一項工作，並在下一個工作開始之前取得輸出。
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- HTTP 伺服器工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22455dbda21aca32b26f586eed6e51cef7509af2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675923"
---
# <a name="http-server-tasks"></a><span data-ttu-id="e000e-104">HTTP 伺服器工作</span><span class="sxs-lookup"><span data-stu-id="e000e-104">HTTP Server Tasks</span></span>

<span data-ttu-id="e000e-105">HTTP 伺服器工作通常會以特定循序執行;也就是說，必須完成一項工作，並在下一個工作開始之前取得輸出。</span><span class="sxs-lookup"><span data-stu-id="e000e-105">Typically, HTTP server tasks are performed in a specific order; that is, one task must be completed and the output obtained before the next task begins.</span></span>

<span data-ttu-id="e000e-106">系統會建立工作頁面，以顯示有關 HTTP 伺服器應用程式所執行之特定工作的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="e000e-106">A task page is created to present sample code about specific tasks that an HTTP Server application performs.</span></span> <span data-ttu-id="e000e-107">工作頁面會連結至 HTTP 伺服器範例的 C 擴充檔。</span><span class="sxs-lookup"><span data-stu-id="e000e-107">A task page links to the C extension file of the HTTP server sample.</span></span> <span data-ttu-id="e000e-108">當您在本機電腦的 C：磁片磁碟機上安裝 PSDK 時 \\ ，會在 c： \\ Program FILES \\ Microsoft SDK \\ 範例 \\ netds \\ HTTP \\ 伺服器上安裝完整的伺服器範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="e000e-108">When you install the PSDK on drive C:\\ of a local computer, the complete server sample application is installed at C:\\Program Files\\Microsoft SDK\\Samples\\netds\\http\\server.</span></span>

<span data-ttu-id="e000e-109">下列清單會識別 HTTP 伺服器工作：</span><span class="sxs-lookup"><span data-stu-id="e000e-109">The following list identifies the HTTP Server tasks:</span></span>

-   [<span data-ttu-id="e000e-110">初始化 HTTP 服務</span><span class="sxs-lookup"><span data-stu-id="e000e-110">Initialize the HTTP Service</span></span>](#initialize-the-http-service)
-   [<span data-ttu-id="e000e-111">註冊要接聽的 Url</span><span class="sxs-lookup"><span data-stu-id="e000e-111">Register the URLs to Listen On</span></span>](#register-the-urls-to-listen-on)
-   [<span data-ttu-id="e000e-112">呼叫常式以接收要求</span><span class="sxs-lookup"><span data-stu-id="e000e-112">Call the Routine to Receive a Request</span></span>](#call-the-routine-to-receive-a-request)
-   [<span data-ttu-id="e000e-113">接收要求</span><span class="sxs-lookup"><span data-stu-id="e000e-113">Receive the Request</span></span>](#receive-the-request)
-   [<span data-ttu-id="e000e-114">處理 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="e000e-114">Handle the HTTP Request</span></span>](#handle-the-http-request)
-   [<span data-ttu-id="e000e-115">傳送 HTTP 回應</span><span class="sxs-lookup"><span data-stu-id="e000e-115">Send the HTTP Response</span></span>](#send-the-http-response)
-   [<span data-ttu-id="e000e-116">傳送 HTTP POST 回應</span><span class="sxs-lookup"><span data-stu-id="e000e-116">Send the HTTP POST Response</span></span>](#send-the-http-post-response)
-   [<span data-ttu-id="e000e-117">清除 HTTP 伺服器 API</span><span class="sxs-lookup"><span data-stu-id="e000e-117">Clean Up the HTTP Server API</span></span>](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a><span data-ttu-id="e000e-118">初始化 HTTP 服務</span><span class="sxs-lookup"><span data-stu-id="e000e-118">Initialize the HTTP Service</span></span>

<span data-ttu-id="e000e-119">HTTP 服務是使用 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) 函式來初始化，而要求佇列的控制碼則是使用 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)所建立。</span><span class="sxs-lookup"><span data-stu-id="e000e-119">The HTTP service is initialized by using the [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) function, and the handle to the request queue is created by using [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle).</span></span> <span data-ttu-id="e000e-120">伺服器必須先初始化，才能呼叫任何其他伺服器函數。</span><span class="sxs-lookup"><span data-stu-id="e000e-120">The server must be initialized before any other server functions can be called.</span></span> <span data-ttu-id="e000e-121">必須先建立要求佇列，服務才能註冊 Url 來接聽傳入的 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="e000e-121">The request queue must be created before the service can register URLs to listen for incoming HTTP requests.</span></span>

<span data-ttu-id="e000e-122">如需詳細資訊和程式碼範例，請參閱 [初始化 HTTP 服務](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-122">For more information and a code example, see [Initialize the HTTP Service](http-server-sample-application.md).</span></span>

## <a name="register-the-urls-to-listen-on"></a><span data-ttu-id="e000e-123">註冊要接聽的 Url</span><span class="sxs-lookup"><span data-stu-id="e000e-123">Register the URLs to Listen On</span></span>

<span data-ttu-id="e000e-124">為了讓 HTTP 伺服器 API 接聽傳入的要求，會藉由呼叫 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式，向 API 註冊特定的 url。</span><span class="sxs-lookup"><span data-stu-id="e000e-124">For the HTTP Server API to listen for incoming requests, specific URLs are registered with the API by calling the [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) function.</span></span> <span data-ttu-id="e000e-125">符合這些 Url 的連入要求會路由傳送到此呼叫中指定的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="e000e-125">Incoming requests that match these URLs are routed to the request queue specified in this call.</span></span>

<span data-ttu-id="e000e-126">如需詳細資訊和程式碼範例，請參閱 [註冊要接聽的 url](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-126">For more information and a code example, see [Register the URLs to Listen On](http-server-sample-application.md).</span></span>

## <a name="call-the-routine-to-receive-a-request"></a><span data-ttu-id="e000e-127">呼叫常式以接收要求</span><span class="sxs-lookup"><span data-stu-id="e000e-127">Call the Routine to Receive a Request</span></span>

<span data-ttu-id="e000e-128">DoReceiveRequest 函式會配置要求緩衝區、初始化要求識別碼，並啟動迴圈來接收要求。</span><span class="sxs-lookup"><span data-stu-id="e000e-128">The DoReceiveRequest function allocates the request buffer, initializes the request ID, and starts the loop to receive requests.</span></span>

<span data-ttu-id="e000e-129">如需詳細資訊和程式碼範例，請參閱 [呼叫常式以接收要求](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-129">For more information and a code example, see [Call the Routine to Receive a Request](http-server-sample-application.md).</span></span>

## <a name="receive-the-request"></a><span data-ttu-id="e000e-130">接收要求</span><span class="sxs-lookup"><span data-stu-id="e000e-130">Receive the Request</span></span>

<span data-ttu-id="e000e-131">HTTP 伺服器 API 會提供一個要求結構來儲存剖析的連入要求。</span><span class="sxs-lookup"><span data-stu-id="e000e-131">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="e000e-132">此結構是由應用程式所配置，並在收到傳入要求時初始化。</span><span class="sxs-lookup"><span data-stu-id="e000e-132">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="e000e-133">應用程式會呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 函數來接收要求。</span><span class="sxs-lookup"><span data-stu-id="e000e-133">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="e000e-134">如果要求緩衝區太小而無法接收要求，應用程式可以增加緩衝區大小，然後再次呼叫 **HttpReceiveHttpRequest** ，以接收整個要求。</span><span class="sxs-lookup"><span data-stu-id="e000e-134">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="e000e-135">如需詳細資訊和程式碼範例，請參閱 [接收要求](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-135">For more information and a code example, see [Receive a Request](http-server-sample-application.md).</span></span>

## <a name="handle-the-http-request"></a><span data-ttu-id="e000e-136">處理 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="e000e-136">Handle the HTTP Request</span></span>

<span data-ttu-id="e000e-137">範例應用程式會示範如何處理 HTTP GET 和 POST 要求動詞。</span><span class="sxs-lookup"><span data-stu-id="e000e-137">The sample application shows how to handle the HTTP GET and POST request verbs.</span></span> <span data-ttu-id="e000e-138">如果應用程式未處理的要求中出現動詞命令，則應用程式會傳送 503 (**未 \_ 執行**) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="e000e-138">The application sends a 503 (**NOT\_IMPLEMENTED**) error if verbs are present in the request that the application does not handle.</span></span>

<span data-ttu-id="e000e-139">請注意，用來處理要求的 URL 是已處理的 URL，其包含在 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1)結構的 **CookedUrl** 成員中。</span><span class="sxs-lookup"><span data-stu-id="e000e-139">Note that the URL to be used in handling requests is the processed URL contained in the **CookedUrl** member of the [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span> <span data-ttu-id="e000e-140">請勿在 **pRawUrl** 成員中使用未處理的 URL，這僅適用于追蹤和統計用途。</span><span class="sxs-lookup"><span data-stu-id="e000e-140">Do not the unprocessed URL in the **pRawUrl** member, which is solely for tracking and statistical purposes.</span></span>

<span data-ttu-id="e000e-141">如需詳細資訊和程式碼範例，請參閱 [處理 HTTP 要求](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-141">For more information and a code example, see [Handle the HTTP Request](http-server-sample-application.md).</span></span>

## <a name="send-the-http-response"></a><span data-ttu-id="e000e-142">傳送 HTTP 回應</span><span class="sxs-lookup"><span data-stu-id="e000e-142">Send the HTTP Response</span></span>

<span data-ttu-id="e000e-143">回應結構會以狀態碼和 INITIALIZE \_ HTTP 回應宏中的原因片語進行配置和初始化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e000e-143">The response structure is allocated and initialized with the status code and a reason phrase in the INITIALIZE\_HTTP\_RESPONSE macro.</span></span> <span data-ttu-id="e000e-144">已知的 HTTP 標頭會新增至「加入已知標頭」宏的回應結構中 \_ \_ ，而實體主體會加入至來自記憶體之資料區塊的回應。</span><span class="sxs-lookup"><span data-stu-id="e000e-144">A known HTTP header is added into the response structure in the ADD\_KNOWN\_HEADER macro, and the entity body is added to the response from a data block from memory.</span></span> <span data-ttu-id="e000e-145">呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 函數以傳送回應。</span><span class="sxs-lookup"><span data-stu-id="e000e-145">The [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function is called to send the response.</span></span> <span data-ttu-id="e000e-146">在此範例中，應用程式會將簡單的200正常回應傳送給 GET 要求。</span><span class="sxs-lookup"><span data-stu-id="e000e-146">In this example, the application sends a simple 200 OK response to the GET request.</span></span>

<span data-ttu-id="e000e-147">如需詳細資訊和程式碼範例，請參閱 [傳送 HTTP 回應](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-147">For more information and a code example, see [Send an HTTP Response](http-server-sample-application.md).</span></span>

## <a name="send-the-http-post-response"></a><span data-ttu-id="e000e-148">傳送 HTTP POST 回應</span><span class="sxs-lookup"><span data-stu-id="e000e-148">Send the HTTP POST Response</span></span>

<span data-ttu-id="e000e-149">POST 要求需要比 GET 要求更多的處理。</span><span class="sxs-lookup"><span data-stu-id="e000e-149">The POST request requires more processing than the GET request.</span></span> <span data-ttu-id="e000e-150">藉由呼叫 [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) 函數來接收要求實體主體。</span><span class="sxs-lookup"><span data-stu-id="e000e-150">The request entity body is received by calling the [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) function.</span></span> <span data-ttu-id="e000e-151">應用程式會在 HTTP 伺服器 API 的個別呼叫中傳送回應和回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="e000e-151">The application sends the response and the response entity body in separate calls to the HTTP Server API.</span></span> <span data-ttu-id="e000e-152">回應標頭會與 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)一起傳送。</span><span class="sxs-lookup"><span data-stu-id="e000e-152">The response headers are sent with the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span> <span data-ttu-id="e000e-153">實體主體會使用 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) 函式，從檔案控制代碼傳送到資料區塊中。</span><span class="sxs-lookup"><span data-stu-id="e000e-153">The entity body is sent in a data block from a file handle with the [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) function.</span></span>

<span data-ttu-id="e000e-154">如需詳細資訊和程式碼範例，請參閱 [傳送 HTTP POST 回應](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-154">For more information and a code example, see [Send an HTTP POST Response](http-server-sample-application.md).</span></span>

## <a name="clean-up-the-http-server-api"></a><span data-ttu-id="e000e-155">清除 HTTP 伺服器 API</span><span class="sxs-lookup"><span data-stu-id="e000e-155">Clean Up the HTTP Server API</span></span>

<span data-ttu-id="e000e-156">HTTP 伺服器 API 的清除作業包括：</span><span class="sxs-lookup"><span data-stu-id="e000e-156">The cleanup operations for the HTTP Server API include:</span></span>

-   <span data-ttu-id="e000e-157">正在移除所有已註冊的 Url。</span><span class="sxs-lookup"><span data-stu-id="e000e-157">Removing all registered URLs.</span></span>
-   <span data-ttu-id="e000e-158">關閉要求佇列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e000e-158">Closing the handle to the request queue.</span></span>
-   <span data-ttu-id="e000e-159">終止 HTTP 伺服器 API 所建立的資源。</span><span class="sxs-lookup"><span data-stu-id="e000e-159">Terminating the resources created by the HTTP Server API.</span></span>

<span data-ttu-id="e000e-160">應用程式會呼叫 [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) 函式，將初始 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式所註冊的 url 取消註冊。</span><span class="sxs-lookup"><span data-stu-id="e000e-160">The application calls the [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) function to deregister URLs registered by the initial [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) function.</span></span> <span data-ttu-id="e000e-161">應用程式也會針對具有相符旗標設定的每個 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)呼叫呼叫 [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) 。</span><span class="sxs-lookup"><span data-stu-id="e000e-161">The application also calls [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) for each call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) with matching flag settings.</span></span> <span data-ttu-id="e000e-162">此呼叫會結束通話 **HttpInitialize** 所建立的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e000e-162">This call terminates all resources created by the call to **HttpInitialize**.</span></span>

<span data-ttu-id="e000e-163">如需詳細資訊和程式碼範例，請參閱 [清除 HTTP 伺服器 API](http-server-sample-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e000e-163">For more information and a code example, see [Cleanup the HTTP Server API](http-server-sample-application.md).</span></span>

 

 




