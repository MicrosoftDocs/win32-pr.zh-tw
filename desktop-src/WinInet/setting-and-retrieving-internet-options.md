---
title: 設定及抓取網際網路選項
description: 本主題說明如何使用 InternetSetOption 和 InternetQueryOption 函式來設定和捕獲網際網路選項。
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- 設定及抓取網際網路選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842603"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="4e824-104">設定及抓取網際網路選項</span><span class="sxs-lookup"><span data-stu-id="4e824-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="4e824-105">本主題說明如何使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 函式來設定和捕獲網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="4e824-106">您可以在 Microsoft Internet Explorer 的指定 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼或目前的設定中，設定或抓取網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="4e824-107">執行步驟</span><span class="sxs-lookup"><span data-stu-id="4e824-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="4e824-108">選擇網際網路選項</span><span class="sxs-lookup"><span data-stu-id="4e824-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="4e824-109">選擇 HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="4e824-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="4e824-110">設定或取出選項</span><span class="sxs-lookup"><span data-stu-id="4e824-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="4e824-111">HINTERNET 控制碼的範圍</span><span class="sxs-lookup"><span data-stu-id="4e824-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="4e824-112">設定個別選項</span><span class="sxs-lookup"><span data-stu-id="4e824-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="4e824-113">正在抓取個別選項</span><span class="sxs-lookup"><span data-stu-id="4e824-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="4e824-114">完整範例</span><span class="sxs-lookup"><span data-stu-id="4e824-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="4e824-115">設定連接選項</span><span class="sxs-lookup"><span data-stu-id="4e824-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="4e824-116">正在抓取連接選項</span><span class="sxs-lookup"><span data-stu-id="4e824-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="4e824-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e824-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="4e824-118">執行步驟</span><span class="sxs-lookup"><span data-stu-id="4e824-118">Implementation Steps</span></span>

<span data-ttu-id="4e824-119">若要設定或取得網際網路選項，請完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="4e824-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="4e824-120">選擇網際網路選項</span><span class="sxs-lookup"><span data-stu-id="4e824-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="4e824-121">選擇 HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="4e824-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="4e824-122">設定或取出選項</span><span class="sxs-lookup"><span data-stu-id="4e824-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="4e824-123">選擇網際網路選項</span><span class="sxs-lookup"><span data-stu-id="4e824-123">Choosing Internet Options</span></span>

<span data-ttu-id="4e824-124">由於有這麼多的網際網路選項，選擇正確的選項相當重要。</span><span class="sxs-lookup"><span data-stu-id="4e824-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="4e824-125">許多網際網路選項都會影響 WinINet 函式和 Internet Explorer 的行為：</span><span class="sxs-lookup"><span data-stu-id="4e824-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="4e824-126">例如，您可以：</span><span class="sxs-lookup"><span data-stu-id="4e824-126">For example, you can:</span></span>

-   <span data-ttu-id="4e824-127">藉由設定使用者名稱和密碼來處理基本伺服器和 proxy 驗證。</span><span class="sxs-lookup"><span data-stu-id="4e824-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="4e824-128">設定或取出伺服器用來識別用戶端應用程式或瀏覽器功能的使用者代理程式字串。</span><span class="sxs-lookup"><span data-stu-id="4e824-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="4e824-129">取得指定之 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="4e824-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="4e824-130">如需詳細資訊和網際網路選項的清單，請參閱 [**選項旗標**](option-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="4e824-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="4e824-131">在 Internet Explorer 5 和更新版本中，您可以使用 [ [**依據連接選項的網際網路] \_ \_ \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 和 [網際網路] 的 [連結] [**\_ \_ \_ 選項**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) 結構，從特定網際網路連線設定或抓取某些選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="4e824-132">如需詳細資訊以及可從特定網際網路連線設定或抓取的選項清單，請參閱網際網路的 **>dwoptions** 成員（ [**\_ 每個連接 \_ \_ 選項**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) 結構）。</span><span class="sxs-lookup"><span data-stu-id="4e824-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="4e824-133">選擇 HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="4e824-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="4e824-134">用來設定或抓取網際網路選項的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，會決定作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="4e824-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="4e824-135">所有透過這個控制碼建立的控制碼都會繼承這個控制碼上設定的選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="4e824-136">例如，需要驗證 proxy 的用戶端應用程式，在每次應用程式嘗試存取網際網路資源時，可能不需要設定 proxy 使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="4e824-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="4e824-137">如果指定連接上的所有要求都是由相同的 proxy 處理，則在連線類型 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼上設定 proxy 使用者名稱和密碼（也就是由呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼），會允許任何衍生自這個 **HINTERNET** 控制碼的呼叫使用相同的 proxy 使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="4e824-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="4e824-138">每次 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)建立 **HINTERNET** 控制碼時，設定 proxy 使用者名稱和密碼需要額外且不必要的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="4e824-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="4e824-139">請注意，如果應用程式使用需要驗證的 proxy，則應該在每個新連接上設定 proxy 認證。</span><span class="sxs-lookup"><span data-stu-id="4e824-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="4e824-140">設定或取出選項</span><span class="sxs-lookup"><span data-stu-id="4e824-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="4e824-141">當您決定要使用的網際網路選項和 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼時，請取出這些網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="4e824-142">若要設定或取出選項，請呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 或 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)。</span><span class="sxs-lookup"><span data-stu-id="4e824-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="4e824-143">HINTERNET 控制碼的範圍</span><span class="sxs-lookup"><span data-stu-id="4e824-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="4e824-144">用來設定或抓取網際網路選項的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，會決定選項的有效動作。</span><span class="sxs-lookup"><span data-stu-id="4e824-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="4e824-145">這些控制碼有三個層級：</span><span class="sxs-lookup"><span data-stu-id="4e824-145">These handles have three levels:</span></span>

-   <span data-ttu-id="4e824-146">呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) 所建立的根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 (會包含會影響此 WinINet 實例的所有網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="4e824-147">連接至伺服器的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼， (由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)的呼叫所建立) </span><span class="sxs-lookup"><span data-stu-id="4e824-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="4e824-148">與資源相關聯的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼，或特定伺服器上的資源列舉。</span><span class="sxs-lookup"><span data-stu-id="4e824-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="4e824-149">除了各種 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼之外，應用程式也可以使用 **Null** 來設定或抓取 Internet Explorer 和 WinINet 函式所使用之網際網路選項的預設值。</span><span class="sxs-lookup"><span data-stu-id="4e824-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="4e824-150">當使用 **Null** 做為控制碼時，設定網際網路選項會變更目前儲存在登錄中的選項預設值。</span><span class="sxs-lookup"><span data-stu-id="4e824-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="4e824-151">用戶端應用程式不應該使用登錄功能來變更網際網路選項的預設值，因為未來可能會改變選項的儲存方式。</span><span class="sxs-lookup"><span data-stu-id="4e824-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="4e824-152">下表列出 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的類型，以及與其相關聯之網際網路選項的範圍。</span><span class="sxs-lookup"><span data-stu-id="4e824-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e824-153">控制碼類型</span><span class="sxs-lookup"><span data-stu-id="4e824-153">Handle Type</span></span></th>
<th><span data-ttu-id="4e824-154">影響範圍</span><span class="sxs-lookup"><span data-stu-id="4e824-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e824-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="4e824-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="4e824-156">Internet Explorer 的預設選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="4e824-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="4e824-158">FTP 伺服器的這個連接的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="4e824-159">這些選項會影響從此 <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> 控制碼起始的任何作業，例如檔案下載。</span><span class="sxs-lookup"><span data-stu-id="4e824-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="4e824-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="4e824-161">此連接到 Gopher 伺服器的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="4e824-162">這些選項會影響從此 <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> 控制碼起始的任何作業，例如檔案下載。</span><span class="sxs-lookup"><span data-stu-id="4e824-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e824-163">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="4e824-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="4e824-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="4e824-165">此連接至 HTTP 伺服器的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="4e824-166">這些選項會影響從此 <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> 控制碼起始的任何作業，例如檔案下載。</span><span class="sxs-lookup"><span data-stu-id="4e824-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="4e824-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="4e824-168">與此檔案要求相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="4e824-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="4e824-170">與此 FTP 資源下載相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="4e824-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="4e824-172">與此 FTP 資源下載相關聯的選項設定會以 HTML 格式格式化。</span><span class="sxs-lookup"><span data-stu-id="4e824-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="4e824-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="4e824-174">與此搜尋 FTP 伺服器上的檔案相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="4e824-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="4e824-176">在以 HTML 格式格式化的 FTP 伺服器上，與這個檔案搜尋相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="4e824-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="4e824-178">與此 Gopher 資源下載相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e824-179">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="4e824-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="4e824-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="4e824-181">與此 Gopher 資源下載相關聯的選項設定會以 HTML 格式格式化。</span><span class="sxs-lookup"><span data-stu-id="4e824-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e824-182">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="4e824-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="4e824-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="4e824-184">與此在 Gopher 伺服器上搜尋檔案相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e824-185">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="4e824-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="4e824-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="4e824-187">在以 HTML 格式格式化的 Gopher 伺服器上，與此搜尋檔案相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e824-188">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="4e824-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e824-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="4e824-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="4e824-190">與此 HTTP 要求相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e824-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="4e824-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="4e824-192">與此 WinINet 函數實例相關聯的選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="4e824-193">設定個別選項</span><span class="sxs-lookup"><span data-stu-id="4e824-193">Setting Individual Options</span></span>

<span data-ttu-id="4e824-194">決定您想要設定的網際網路選項以及這些選項所要影響的範圍之後，設定 [網際網路選項] 並不複雜。</span><span class="sxs-lookup"><span data-stu-id="4e824-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="4e824-195">您只需要使用所需的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼、網際網路選項旗標，以及包含您想要設定之資訊的緩衝區來呼叫 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)函式。</span><span class="sxs-lookup"><span data-stu-id="4e824-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="4e824-196">下列範例顯示如何在指定的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼上設定 proxy 使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="4e824-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a><span data-ttu-id="4e824-197">正在抓取個別選項</span><span class="sxs-lookup"><span data-stu-id="4e824-197">Retrieving Individual Options</span></span>

<span data-ttu-id="4e824-198">您可以使用 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 函式來取出網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="4e824-199">若要取得網際網路選項：</span><span class="sxs-lookup"><span data-stu-id="4e824-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="4e824-200">判斷取出網際網路選項資訊所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="4e824-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="4e824-201">緩衝區大小可透過使用 **Null** 作為緩衝區位址，並以零的緩衝區大小傳遞給緩衝區大小來決定。</span><span class="sxs-lookup"><span data-stu-id="4e824-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="4e824-202">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所傳回的值是取得資訊所需的記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4e824-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="4e824-203">配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e824-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="4e824-204">取得資料。</span><span class="sxs-lookup"><span data-stu-id="4e824-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="4e824-205">釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e824-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="4e824-206">完整範例</span><span class="sxs-lookup"><span data-stu-id="4e824-206">Complete Sample</span></span>

<span data-ttu-id="4e824-207">以下是前一節中使用的完整範例。</span><span class="sxs-lookup"><span data-stu-id="4e824-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="4e824-208">這個範例會示範如何取出預設的使用者代理程式字串。</span><span class="sxs-lookup"><span data-stu-id="4e824-208">This sample shows how to retrieve the default user agent string.</span></span>


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a><span data-ttu-id="4e824-209">設定連接選項</span><span class="sxs-lookup"><span data-stu-id="4e824-209">Setting Connection Options</span></span>

<span data-ttu-id="4e824-210">在 Internet Explorer 5 和更新版本中，可以針對特定連接設定網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="4e824-211">先前，所有連線都共用相同的網際網路選項設定。</span><span class="sxs-lookup"><span data-stu-id="4e824-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="4e824-212">若要設定特定連接的選項：</span><span class="sxs-lookup"><span data-stu-id="4e824-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="4e824-213">建立 [**\_ 每個 \_ CONN \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 結構的網際網路。</span><span class="sxs-lookup"><span data-stu-id="4e824-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="4e824-214">針對您想要為連線設定的個別網際網路選項配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e824-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="4e824-215">設定 [網際網路] [**中 \_ 每 \_ 個 \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) [連接] 選項結構的選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="4e824-216">使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)設定選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="4e824-217">下列程式碼範例顯示如何設定 LAN 連接的 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="4e824-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a><span data-ttu-id="4e824-218">正在抓取連接選項</span><span class="sxs-lookup"><span data-stu-id="4e824-218">Retrieving Connection Options</span></span>

<span data-ttu-id="4e824-219">在 Internet Explorer 5 和更新版本中，可以從特定連線中取出網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="4e824-220">從特定連接取出選項：</span><span class="sxs-lookup"><span data-stu-id="4e824-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="4e824-221">建立 [**\_ 每個 \_ CONN \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 結構的網際網路。</span><span class="sxs-lookup"><span data-stu-id="4e824-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="4e824-222">配置個別網際網路選項的記憶體，以從連接中取出。</span><span class="sxs-lookup"><span data-stu-id="4e824-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="4e824-223">使用 [網際網路] [**\_ \_ \_ 選項**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) 結構來指定選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="4e824-224">使用 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)取出選項。</span><span class="sxs-lookup"><span data-stu-id="4e824-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="4e824-225">利用選項資料。</span><span class="sxs-lookup"><span data-stu-id="4e824-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="4e824-226">使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式釋放配置用來保存選項資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e824-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="4e824-227">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="4e824-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="4e824-228">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="4e824-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="4e824-229">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="4e824-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4e824-230">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e824-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e824-231">處理驗證</span><span class="sxs-lookup"><span data-stu-id="4e824-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="4e824-232">HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="4e824-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

