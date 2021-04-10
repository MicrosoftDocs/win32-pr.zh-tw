---
title: HTTP 會話
description: 您可以使用 HTTP 來存取 WWW 上的資源。
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092844"
---
# <a name="http-sessions"></a><span data-ttu-id="10d5d-103">HTTP 會話</span><span class="sxs-lookup"><span data-stu-id="10d5d-103">HTTP Sessions</span></span>

<span data-ttu-id="10d5d-104">WinINet 可讓您存取 World Wide Web (WWW) 上的資源。</span><span class="sxs-lookup"><span data-stu-id="10d5d-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="10d5d-105">您可以使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (直接存取這些資源。如需詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)) 。</span><span class="sxs-lookup"><span data-stu-id="10d5d-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="10d5d-106">您可以使用 HTTP 來存取 WWW 上的資源。</span><span class="sxs-lookup"><span data-stu-id="10d5d-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="10d5d-107">HTTP 函式會處理基礎通訊協定，同時允許您的應用程式存取 WWW 上的資訊。</span><span class="sxs-lookup"><span data-stu-id="10d5d-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="10d5d-108">當 HTTP 通訊協定演進時，會更新基礎通訊協定以維護函式行為。</span><span class="sxs-lookup"><span data-stu-id="10d5d-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="10d5d-109">下圖顯示與 HTTP 通訊協定搭配使用之函數的關聯性。</span><span class="sxs-lookup"><span data-stu-id="10d5d-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="10d5d-110">陰影方塊代表會傳回 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![用於 HTTP 的 wininet 函數](images/ax-wnt05.png)

<span data-ttu-id="10d5d-112">如需詳細資訊，請參閱 [HINTERNET 控制碼](appendix-a-hinternet-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="10d5d-113">使用 WinINet 函數存取 WWW</span><span class="sxs-lookup"><span data-stu-id="10d5d-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="10d5d-114">起始與 WWW 的連接</span><span class="sxs-lookup"><span data-stu-id="10d5d-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="10d5d-115">開啟要求</span><span class="sxs-lookup"><span data-stu-id="10d5d-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="10d5d-116">新增要求標頭</span><span class="sxs-lookup"><span data-stu-id="10d5d-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="10d5d-117">傳送要求</span><span class="sxs-lookup"><span data-stu-id="10d5d-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="10d5d-118">將資料張貼到伺服器</span><span class="sxs-lookup"><span data-stu-id="10d5d-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="10d5d-119">取得要求的相關資訊</span><span class="sxs-lookup"><span data-stu-id="10d5d-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="10d5d-120">從 WWW 下載資源</span><span class="sxs-lookup"><span data-stu-id="10d5d-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="10d5d-121">下列函式會在 HTTP 會話期間用來存取 WWW。</span><span class="sxs-lookup"><span data-stu-id="10d5d-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="10d5d-122">函式</span><span class="sxs-lookup"><span data-stu-id="10d5d-122">Function</span></span>                                               | <span data-ttu-id="10d5d-123">描述</span><span class="sxs-lookup"><span data-stu-id="10d5d-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10d5d-124">**HttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="10d5d-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="10d5d-125">將 HTTP 要求標頭新增至 HTTP 要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="10d5d-126">此函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="10d5d-127">**HttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="10d5d-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="10d5d-128">開啟 HTTP 要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="10d5d-129">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="10d5d-130">**HttpQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="10d5d-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="10d5d-131">查詢 HTTP 要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="10d5d-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="10d5d-132">此函式需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="10d5d-133">**HttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="10d5d-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="10d5d-134">將指定的 HTTP 要求傳送至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="10d5d-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="10d5d-135">此函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="10d5d-136">**InternetErrorDlg**</span><span class="sxs-lookup"><span data-stu-id="10d5d-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="10d5d-137">針對常見的網際網路錯誤情況，顯示預先定義的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="10d5d-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="10d5d-138">此函式需要 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)呼叫中使用的控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="10d5d-139">起始與 WWW 的連接</span><span class="sxs-lookup"><span data-stu-id="10d5d-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="10d5d-140">若要啟動與 WWW 的連接，應用程式必須在 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所傳回的根 [**HINTERNET**](appendix-a-hinternet-handles.md)上呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式。</span><span class="sxs-lookup"><span data-stu-id="10d5d-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="10d5d-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 必須宣告網際網路 \_ 服務 \_ HTTP 服務類型，以建立 HTTP 會話。</span><span class="sxs-lookup"><span data-stu-id="10d5d-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="10d5d-142">如需使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)的詳細資訊，請參閱 [使用 InternetConnect](enabling-internet-functionality.md)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="10d5d-143">開啟要求</span><span class="sxs-lookup"><span data-stu-id="10d5d-143">Opening a Request</span></span>

<span data-ttu-id="10d5d-144">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函式會開啟 HTTP 要求，並傳回其他 HTTP 函數可使用的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="10d5d-145">不同于其他開啟的函式 (例如 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 和 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)) ， [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 不會在呼叫時將要求傳送至網際網路。</span><span class="sxs-lookup"><span data-stu-id="10d5d-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="10d5d-146">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)函式會傳送要求，並透過網路建立連接。</span><span class="sxs-lookup"><span data-stu-id="10d5d-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="10d5d-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 會採用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 和 HTTP 動詞命令、物件名稱、版本字串、查閱者、接受類型、旗標和內容值所建立的 HTTP 會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="10d5d-148">HTTP 動詞命令是要在要求中使用的字串。</span><span class="sxs-lookup"><span data-stu-id="10d5d-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="10d5d-149">要求中使用的常見 HTTP 動詞命令包括 GET、PUT 和 POST。</span><span class="sxs-lookup"><span data-stu-id="10d5d-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="10d5d-150">如果這個值設定為 **Null**， [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 會使用預設值 GET。</span><span class="sxs-lookup"><span data-stu-id="10d5d-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="10d5d-151">物件名稱是一個字串，其中包含指定之 HTTP 動詞命令的目標物件名稱。</span><span class="sxs-lookup"><span data-stu-id="10d5d-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="10d5d-152">這通常是檔案名、可執行模組或搜尋規範。</span><span class="sxs-lookup"><span data-stu-id="10d5d-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="10d5d-153">如果提供的物件名稱是空字串，則 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 會尋找預設頁面。</span><span class="sxs-lookup"><span data-stu-id="10d5d-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="10d5d-154">版本字串應包含 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="10d5d-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="10d5d-155">如果此參數為 **Null**，則函數會使用 "" HTTP/1.1 ""。</span><span class="sxs-lookup"><span data-stu-id="10d5d-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="10d5d-156">訪客會指定取得物件名稱的檔位址。</span><span class="sxs-lookup"><span data-stu-id="10d5d-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="10d5d-157">如果此參數為 **Null**，則不會指定任何訪客。</span><span class="sxs-lookup"><span data-stu-id="10d5d-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="10d5d-158">以 **null** 終止的字串，包含接受類型表示應用程式接受的內容類型。</span><span class="sxs-lookup"><span data-stu-id="10d5d-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="10d5d-159">將此參數設定為 **Null** ，表示應用程式不接受任何內容類型。</span><span class="sxs-lookup"><span data-stu-id="10d5d-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="10d5d-160">如果提供空字串，應用程式表示它只接受 "" text/"" 類型的檔 \* 。</span><span class="sxs-lookup"><span data-stu-id="10d5d-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="10d5d-161">值 "" text/ \* "" 表示純文字檔，而不是圖片或其他二進位檔。</span><span class="sxs-lookup"><span data-stu-id="10d5d-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="10d5d-162">旗標值會控制快取、cookie 和安全性問題。</span><span class="sxs-lookup"><span data-stu-id="10d5d-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="10d5d-163">若為 Microsoft Network (MSN) 、NTLM 和其他類型的驗證，請設定 [網際網路 \_ 旗 \_ 標 \_ 保持連線](api-flags.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="10d5d-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="10d5d-164">如果在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)時設定了 [INTERNET \_ 旗標 \_ ASYNC](api-flags.md)旗標，則應該針對適當的非同步作業設定非零的內容值。</span><span class="sxs-lookup"><span data-stu-id="10d5d-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="10d5d-165">下列範例是 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)的範例呼叫。</span><span class="sxs-lookup"><span data-stu-id="10d5d-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="10d5d-166">新增要求標頭</span><span class="sxs-lookup"><span data-stu-id="10d5d-166">Adding Request Headers</span></span>

<span data-ttu-id="10d5d-167">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa)函式可讓應用程式將一個或多個要求標頭加入至初始要求。</span><span class="sxs-lookup"><span data-stu-id="10d5d-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="10d5d-168">此函式可讓應用程式將額外的自由格式標頭附加至 HTTP 要求控制碼;它適用于需要精確控制傳送至 HTTP 伺服器之要求的精密應用程式。</span><span class="sxs-lookup"><span data-stu-id="10d5d-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="10d5d-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) 需要由 [**HTTPOPENREQUEST**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立的 HTTP 要求控制碼、包含標頭的字串、標頭的長度，以及修飾詞。</span><span class="sxs-lookup"><span data-stu-id="10d5d-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="10d5d-170">傳送要求</span><span class="sxs-lookup"><span data-stu-id="10d5d-170">Sending a Request</span></span>

<span data-ttu-id="10d5d-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 會建立與網際網路的連線，並將要求傳送至指定的網站。</span><span class="sxs-lookup"><span data-stu-id="10d5d-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="10d5d-172">此函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="10d5d-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 也可以傳送額外的標頭或選擇性資訊。</span><span class="sxs-lookup"><span data-stu-id="10d5d-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="10d5d-174">選用資訊通常用於將資訊寫入伺服器的作業，例如 PUT 和 POST。</span><span class="sxs-lookup"><span data-stu-id="10d5d-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="10d5d-175">在 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)傳送要求之後，應用程式可以在 [**HINTERNET**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的 [**HttpOpenRequest**](appendix-a-hinternet-handles.md)控制碼上，使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)函數來下載伺服器的資源。</span><span class="sxs-lookup"><span data-stu-id="10d5d-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="10d5d-176">將資料張貼到伺服器</span><span class="sxs-lookup"><span data-stu-id="10d5d-176">Posting Data to the Server</span></span>

<span data-ttu-id="10d5d-177">若要將資料張貼至伺服器，呼叫 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 的 HTTP 動詞命令必須是 POST 或 PUT。</span><span class="sxs-lookup"><span data-stu-id="10d5d-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="10d5d-178">接著，必須將包含 POST 資料的緩衝區位址傳遞至 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)中的 *lpOptional* 參數。</span><span class="sxs-lookup"><span data-stu-id="10d5d-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="10d5d-179">*DwOptionalLength* 參數應該設定為數據的大小。</span><span class="sxs-lookup"><span data-stu-id="10d5d-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="10d5d-180">您也可以使用 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)函數，在使用 [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)傳送的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼上張貼資料。</span><span class="sxs-lookup"><span data-stu-id="10d5d-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="10d5d-181">取得要求的相關資訊</span><span class="sxs-lookup"><span data-stu-id="10d5d-181">Getting Information About a Request</span></span>

<span data-ttu-id="10d5d-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 可讓應用程式取得 HTTP 要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="10d5d-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="10d5d-183">函數需要 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)所建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼、資訊層級值，以及緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="10d5d-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="10d5d-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 也接受緩衝區來儲存資訊和以零為基底的標頭索引，以列舉具有相同名稱的多個標頭。</span><span class="sxs-lookup"><span data-stu-id="10d5d-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="10d5d-185">從 WWW 下載資源</span><span class="sxs-lookup"><span data-stu-id="10d5d-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="10d5d-186">使用 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 開啟要求，並使用 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)將其傳送至伺服器之後，應用程式可以使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**INTERNETQUERYDATAAVAILABLE**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) 函式，從 HTTP 伺服器下載資源。</span><span class="sxs-lookup"><span data-stu-id="10d5d-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="10d5d-187">下列範例會下載資源。</span><span class="sxs-lookup"><span data-stu-id="10d5d-187">The following example downloads a resource.</span></span> <span data-ttu-id="10d5d-188">函數會接受目前視窗的控制碼、編輯方塊的識別碼，以及由 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立並由 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)傳送的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="10d5d-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="10d5d-189">它會使用 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) 來判斷資源的大小，然後使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)進行下載。</span><span class="sxs-lookup"><span data-stu-id="10d5d-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="10d5d-190">然後，內容會顯示在編輯方塊中。</span><span class="sxs-lookup"><span data-stu-id="10d5d-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="10d5d-191">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="10d5d-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="10d5d-192">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="10d5d-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="10d5d-193">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="10d5d-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 