---
description: Microsoft Windows HTTP Services (WinHTTP) 會公開一組 C/c + + 函式，可讓您的應用程式存取 Web 上的 HTTP 資源。 本主題概要說明如何使用這些函數來與 HTTP 伺服器互動。
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: WinHTTP 會話總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113141"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="d13a6-104">WinHTTP 會話總覽</span><span class="sxs-lookup"><span data-stu-id="d13a6-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="d13a6-105">Microsoft Windows HTTP Services (WinHTTP) 會公開一組 C/c + + 函式，可讓您的應用程式存取 Web 上的 HTTP 資源。</span><span class="sxs-lookup"><span data-stu-id="d13a6-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="d13a6-106">本主題概要說明如何使用這些函數來與 HTTP 伺服器互動。</span><span class="sxs-lookup"><span data-stu-id="d13a6-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="d13a6-107">使用 WinHTTP API 來存取 Web</span><span class="sxs-lookup"><span data-stu-id="d13a6-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="d13a6-108">正在初始化 WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d13a6-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="d13a6-109">開啟要求</span><span class="sxs-lookup"><span data-stu-id="d13a6-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="d13a6-110">新增要求標頭</span><span class="sxs-lookup"><span data-stu-id="d13a6-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="d13a6-111">傳送要求</span><span class="sxs-lookup"><span data-stu-id="d13a6-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="d13a6-112">將資料張貼到伺服器</span><span class="sxs-lookup"><span data-stu-id="d13a6-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="d13a6-113">取得要求的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d13a6-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="d13a6-114">從 Web 下載資源</span><span class="sxs-lookup"><span data-stu-id="d13a6-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="d13a6-115">使用 WinHTTP API 來存取 Web</span><span class="sxs-lookup"><span data-stu-id="d13a6-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="d13a6-116">下圖顯示當與 HTTP 伺服器互動時，通常會呼叫 WinHTTP 函數的順序。</span><span class="sxs-lookup"><span data-stu-id="d13a6-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="d13a6-117">陰影方塊表示產生 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼的函式，而一般方塊代表使用這些控制碼的函式。</span><span class="sxs-lookup"><span data-stu-id="d13a6-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![建立控制碼的函式](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="d13a6-119">正在初始化 WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d13a6-119">Initializing WinHTTP</span></span>

<span data-ttu-id="d13a6-120">在與伺服器互動之前，必須先呼叫 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)來初始化 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="d13a6-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="d13a6-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 會建立會話內容來維護 HTTP 會話的詳細資料，並傳回會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="d13a6-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="d13a6-122">[**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)函式會使用此控制碼，指定目標 HTTP 或安全超文字傳輸通訊協定 (HTTPS) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d13a6-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="d13a6-123">在對特定資源提出要求之前，對 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) 的呼叫不會產生與 HTTP 伺服器的實際連接。</span><span class="sxs-lookup"><span data-stu-id="d13a6-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="d13a6-124">開啟要求</span><span class="sxs-lookup"><span data-stu-id="d13a6-124">Opening a Request</span></span>

<span data-ttu-id="d13a6-125">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)函式會開啟特定資源的 HTTP 要求，並傳回其他 HTTP 函數可使用的 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="d13a6-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="d13a6-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 不會在呼叫時將要求傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="d13a6-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="d13a6-127">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式會透過網路實際建立連線，並傳送要求。</span><span class="sxs-lookup"><span data-stu-id="d13a6-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="d13a6-128">下列範例顯示使用預設選項之 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 的範例呼叫。</span><span class="sxs-lookup"><span data-stu-id="d13a6-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="d13a6-129">新增要求標頭</span><span class="sxs-lookup"><span data-stu-id="d13a6-129">Adding Request Headers</span></span>

<span data-ttu-id="d13a6-130">[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)函式可讓應用程式將額外的自由格式要求標頭附加至 HTTP 要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="d13a6-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="d13a6-131">它適用于需要精確控制傳送至 HTTP 伺服器之要求的精密應用程式。</span><span class="sxs-lookup"><span data-stu-id="d13a6-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="d13a6-132">[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)函式需要 [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立的 HTTP 要求控制碼、包含標頭的字串、標頭的長度，以及任何修飾詞。</span><span class="sxs-lookup"><span data-stu-id="d13a6-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="d13a6-133">下列修飾詞可以搭配 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)使用。</span><span class="sxs-lookup"><span data-stu-id="d13a6-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="d13a6-134">修飾詞</span><span class="sxs-lookup"><span data-stu-id="d13a6-134">Modifier</span></span>                                                                                         | <span data-ttu-id="d13a6-135">Description</span><span class="sxs-lookup"><span data-stu-id="d13a6-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d13a6-136">**WINHTTP \_ ADDREQ \_ 旗標 \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="d13a6-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="d13a6-137">如果標頭不存在，則加入標頭。</span><span class="sxs-lookup"><span data-stu-id="d13a6-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="d13a6-138">使用於 [**WINHTTP \_ ADDREQ \_ 旗標 \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)。</span><span class="sxs-lookup"><span data-stu-id="d13a6-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="d13a6-139">**新的 WINHTTP \_ ADDREQ \_ 旗標 \_ \_ \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="d13a6-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="d13a6-140">只有當標頭不存在時，才新增標頭;否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d13a6-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="d13a6-141">**WINHTTP \_ ADDREQ \_ 旗標 \_ 聯合**</span><span class="sxs-lookup"><span data-stu-id="d13a6-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="d13a6-142">合併相同名稱的標頭。</span><span class="sxs-lookup"><span data-stu-id="d13a6-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="d13a6-143">**WINHTTP \_ ADDREQ \_ 旗 \_ 標 \_ 與 \_ 逗號聯合**</span><span class="sxs-lookup"><span data-stu-id="d13a6-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="d13a6-144">使用逗號合併相同名稱的標頭。</span><span class="sxs-lookup"><span data-stu-id="d13a6-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="d13a6-145">例如，新增 "Accept： text/ \* "，後面接著 "accept： audio/ \* " 且此旗標會形成單一標頭 "Accept： text/ \* ，audio/ \* "，導致第一個找到的標頭合併。</span><span class="sxs-lookup"><span data-stu-id="d13a6-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="d13a6-146">它是由呼叫應用程式所組成，以確保與合併/分開的標頭相關的配置一致。</span><span class="sxs-lookup"><span data-stu-id="d13a6-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="d13a6-147">**WINHTTP \_ ADDREQ \_ 旗 \_ 標 \_ 與 \_ 分號合併**</span><span class="sxs-lookup"><span data-stu-id="d13a6-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="d13a6-148">使用分號合併相同名稱的標頭。</span><span class="sxs-lookup"><span data-stu-id="d13a6-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="d13a6-149">**WINHTTP \_ ADDREQ \_ 旗標 \_ 取代**</span><span class="sxs-lookup"><span data-stu-id="d13a6-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="d13a6-150">取代或移除標頭。</span><span class="sxs-lookup"><span data-stu-id="d13a6-150">Replaces or removes a header.</span></span> <span data-ttu-id="d13a6-151">如果標頭值是空的，而且找到標頭，則會將它移除。</span><span class="sxs-lookup"><span data-stu-id="d13a6-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="d13a6-152">如果標頭值不是空的，則會取代標頭值。</span><span class="sxs-lookup"><span data-stu-id="d13a6-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="d13a6-153">傳送要求</span><span class="sxs-lookup"><span data-stu-id="d13a6-153">Sending a Request</span></span>

<span data-ttu-id="d13a6-154">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式會建立與伺服器的連接，並將要求傳送至指定的網站。</span><span class="sxs-lookup"><span data-stu-id="d13a6-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="d13a6-155">此函數需要 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立的 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="d13a6-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="d13a6-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 也可以傳送額外的標頭或選擇性資訊。</span><span class="sxs-lookup"><span data-stu-id="d13a6-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="d13a6-157">選用資訊通常用於將資訊寫入伺服器的作業，例如 PUT 和 POST。</span><span class="sxs-lookup"><span data-stu-id="d13a6-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="d13a6-158">在 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式傳送要求之後，應用程式可以使用 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼上的 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)和 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)函數來下載伺服器的資源。</span><span class="sxs-lookup"><span data-stu-id="d13a6-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="d13a6-159">將資料張貼到伺服器</span><span class="sxs-lookup"><span data-stu-id="d13a6-159">Posting Data to the Server</span></span>

<span data-ttu-id="d13a6-160">若要將資料張貼至伺服器，呼叫 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)的 [*HTTP 動詞*](glossary.md)命令必須是 post 或 PUT。</span><span class="sxs-lookup"><span data-stu-id="d13a6-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="d13a6-161">當呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 時， *dwTotalLength* 參數應該設定為數據的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d13a6-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="d13a6-162">然後使用 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) 將資料張貼至伺服器。</span><span class="sxs-lookup"><span data-stu-id="d13a6-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="d13a6-163">或者，將 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)的 *lpOptional* 參數設定為包含要張貼至伺服器之資料的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="d13a6-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="d13a6-164">使用這項技術時，您必須將 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)的 *dwOptionalLength* 和 *dwTotalLength* 參數設定為要張貼之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="d13a6-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="d13a6-165">以這種方式呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ，就不需要呼叫 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)。</span><span class="sxs-lookup"><span data-stu-id="d13a6-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="d13a6-166">取得要求的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d13a6-166">Getting Information About a Request</span></span>

<span data-ttu-id="d13a6-167">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)函式可讓應用程式取得 HTTP 要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d13a6-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="d13a6-168">函數需要 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立的 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼、資訊層級值，以及緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="d13a6-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="d13a6-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) 也接受緩衝區來儲存資訊和以零為基底的標頭索引，以列舉具有相同名稱的多個標頭。</span><span class="sxs-lookup"><span data-stu-id="d13a6-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="d13a6-170">使用在 [[**查詢資訊旗標**](query-info-flags.md)] 頁面上找到的任何資訊層級值，並以修飾詞來控制資訊儲存在 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)的 *lpvBuffer* 參數中的格式。</span><span class="sxs-lookup"><span data-stu-id="d13a6-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="d13a6-171">從 Web 下載資源</span><span class="sxs-lookup"><span data-stu-id="d13a6-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="d13a6-172">使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 函式開啟要求，並使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)將其傳送至伺服器，並準備要求控制碼以接收 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)的回應之後，應用程式就可以使用 [**WINHTTPREADDATA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) 和 [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) 函式，從 HTTP 伺服器下載資源。</span><span class="sxs-lookup"><span data-stu-id="d13a6-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="d13a6-173">下列範例程式碼示範如何下載具有安全交易語義的資源。</span><span class="sxs-lookup"><span data-stu-id="d13a6-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="d13a6-174">範例程式碼會初始化 (API) 的 WinHTTP 應用程式開發介面、選取目標 HTTPS 伺服器，然後開啟並傳送此安全資源的要求。</span><span class="sxs-lookup"><span data-stu-id="d13a6-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="d13a6-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) 可搭配要求控制碼使用，以判斷可供下載的資料量，然後使用 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) 來讀取該資料。</span><span class="sxs-lookup"><span data-stu-id="d13a6-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="d13a6-176">此程式會重複執行，直到整份檔被抓取並顯示為止。</span><span class="sxs-lookup"><span data-stu-id="d13a6-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



