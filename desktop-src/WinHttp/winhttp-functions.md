---
description: 本主題將識別 WinHTTP 提供的函式。
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972858"
---
# <a name="winhttp-functions"></a><span data-ttu-id="db70f-103">WinHTTP 函數</span><span class="sxs-lookup"><span data-stu-id="db70f-103">WinHTTP Functions</span></span>

<span data-ttu-id="db70f-104">WinHTTP 提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="db70f-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="db70f-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="db70f-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="db70f-106">將一或多個 HTTP 要求標頭新增至 HTTP 要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="db70f-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="db70f-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="db70f-108">判斷 WinHTTP 是否支援目前的平臺。</span><span class="sxs-lookup"><span data-stu-id="db70f-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="db70f-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="db70f-110">關閉單一 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="db70f-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="db70f-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="db70f-112">指定 HTTP 要求的初始目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="db70f-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="db70f-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="db70f-114">將 URL 分隔成其元件部分，例如，主機名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="db70f-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="db70f-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="db70f-116">建立 [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)所使用的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db70f-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="db70f-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="db70f-118">從元件部分建立 URL，例如主機名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="db70f-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="db70f-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="db70f-120">尋找 Proxy 自動設定 (PAC) 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="db70f-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="db70f-121">此函數會報告 PAC 檔案的 URL，但不會下載檔案。</span><span class="sxs-lookup"><span data-stu-id="db70f-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="db70f-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="db70f-123">釋出從先前的 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)呼叫取出的資料。</span><span class="sxs-lookup"><span data-stu-id="db70f-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-124">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="db70f-124">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="db70f-125">從登錄抓取預設的 WinHTTP proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="db70f-125">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="db70f-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="db70f-127">取得目前使用者的 Internet Explorer (IE) proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="db70f-127">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-128">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="db70f-128">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="db70f-129">抓取指定之 URL 的 proxy 資訊。</span><span class="sxs-lookup"><span data-stu-id="db70f-129">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-130">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="db70f-130">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="db70f-131">抓取指定之 URL 的 proxy 資訊。</span><span class="sxs-lookup"><span data-stu-id="db70f-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-132">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="db70f-132">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="db70f-133">抓取 [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="db70f-133">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-134">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="db70f-134">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="db70f-135">初始化應用程式對 WinHTTP 函式的使用。</span><span class="sxs-lookup"><span data-stu-id="db70f-135">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-136">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="db70f-136">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="db70f-137">建立 HTTP 要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="db70f-137">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-138">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="db70f-138">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="db70f-139">傳回伺服器支援的授權配置。</span><span class="sxs-lookup"><span data-stu-id="db70f-139">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-140">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="db70f-140">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="db70f-141">傳回可立即使用 [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)讀取的資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="db70f-141">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-142">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="db70f-142">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="db70f-143">抓取與 HTTP 要求相關聯的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="db70f-143">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-144">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="db70f-144">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="db70f-145">在指定的控制碼上查詢網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="db70f-145">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-146">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="db70f-146">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="db70f-147">從 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 函數所開啟的控制碼讀取資料。</span><span class="sxs-lookup"><span data-stu-id="db70f-147">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-148">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="db70f-148">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="db70f-149">結束由 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)起始的 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="db70f-149">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-150">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="db70f-150">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="db70f-151">重設自動 proxy。</span><span class="sxs-lookup"><span data-stu-id="db70f-151">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-152">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="db70f-152">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="db70f-153">將指定的要求傳送至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="db70f-153">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-154">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="db70f-154">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="db70f-155">將必要的授權認證傳遞給伺服器。</span><span class="sxs-lookup"><span data-stu-id="db70f-155">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-156">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="db70f-156">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="db70f-157">在登錄中設定預設的 WinHTTP proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="db70f-157">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-158">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="db70f-158">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="db70f-159">設定網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="db70f-159">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-160">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="db70f-160">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="db70f-161">設定 WinHTTP 可以在作業期間進行的呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="db70f-161">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-162">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="db70f-162">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="db70f-163">設定與 HTTP 交易相關的各種超時時間。</span><span class="sxs-lookup"><span data-stu-id="db70f-163">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-164">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="db70f-164">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="db70f-165">根據 HTTP 版本1.0 規格來格式化日期和時間。</span><span class="sxs-lookup"><span data-stu-id="db70f-165">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-166">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="db70f-166">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="db70f-167">取得 HTTP 時間/日期字串，並將它轉換成 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構。</span><span class="sxs-lookup"><span data-stu-id="db70f-167">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-168">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="db70f-168">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="db70f-169">將要求資料寫入至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="db70f-169">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-170">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="db70f-170">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="db70f-171">關閉 WebSocket 連接。</span><span class="sxs-lookup"><span data-stu-id="db70f-171">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-172">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="db70f-172">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="db70f-173">完成 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)啟動的 WebSocket 交握。</span><span class="sxs-lookup"><span data-stu-id="db70f-173">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-174">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="db70f-174">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="db70f-175">取得伺服器所傳送的關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="db70f-175">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-176">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="db70f-176">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="db70f-177">接收來自 WebSocket 連接的資料。</span><span class="sxs-lookup"><span data-stu-id="db70f-177">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-178">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="db70f-178">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="db70f-179">透過 WebSocket 連接傳送資料。</span><span class="sxs-lookup"><span data-stu-id="db70f-179">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="db70f-180">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="db70f-180">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="db70f-181">將關閉框架傳送至 WebSocket 連接。</span><span class="sxs-lookup"><span data-stu-id="db70f-181">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
