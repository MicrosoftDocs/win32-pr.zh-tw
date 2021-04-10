---
description: 用戶端記錄
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: '用戶端記錄 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191082"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="9ecaa-103">用戶端記錄 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="9ecaa-103">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="9ecaa-104">網路來源支援用戶端記錄，可讓媒體伺服器追蹤連接到該用戶端的用戶端活動。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-104">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="9ecaa-105">用戶端記錄檔可讓伺服器記錄連接、轉譯和串流處理統計資料。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-105">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="9ecaa-106">這些記錄可供各種案例中的內容提供者使用，例如，用來追蹤媒體伺服器使用量和產生帳單，或根據用戶端網路的速度傳遞適當品質的內容。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-106">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="9ecaa-107">記錄檔包含數個用戶端事件專案。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-107">A log file contains several client event entries.</span></span> <span data-ttu-id="9ecaa-108">每個記錄專案都包含一些以空格分隔的欄位。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-108">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="9ecaa-109">用戶端記錄有兩種 *類型：轉譯* (播放) ，以及接收) 的 *串流* (。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-109">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="9ecaa-110">由於內容可以同時播放和串流，因此用戶端可以同時傳送這兩種記錄資料類型的組合。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-110">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="9ecaa-111">在某些情況下，相同的會話可以有兩個記錄專案。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-111">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="9ecaa-112">例如，啟用 [快速快取] 時，用戶端可以在完成轉譯後，先完成接收資料流程處理的內容。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-112">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="9ecaa-113">在此情況下，會在轉譯記錄資料之前傳送串流記錄資料。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-113">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="9ecaa-114">用戶端會在用戶端從任何播放狀態變更時，傳送轉譯記錄資料到伺服器 (播放、向前快轉或倒轉) 至非播放狀態 (停止、暫停、串流結束，以及串流) 開頭。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-114">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="9ecaa-115">提交轉譯記錄檔的資料時，會直接連接到媒體伺服器或設定的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-115">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="9ecaa-116">如果內容儲存在執行用戶端之電腦上的暫存本機快取檔案中，則用戶端可以從其本機快取讀取檔案，並提交轉譯記錄資料，以指出它已播放內容。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-116">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="9ecaa-117">在此情況下，用戶端會從其本機快取讀取檔案、轉譯記錄專案不包含任何網路統計資料，且通訊協定設定為快取。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-117">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="9ecaa-118">用戶端會將串流記錄資料傳送到伺服器，以指出用戶端如何接收內容，但不會呈現其轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-118">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="9ecaa-119">用戶端可以在用戶端完成轉譯內容之前，傳送串流記錄的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-119">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="9ecaa-120">本主題不提供所有記錄欄位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-120">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="9ecaa-121">如需完整的參考，請參閱 [Windows Media 記錄資料結構](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84)。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-121">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="9ecaa-122">設定記錄欄位</span><span class="sxs-lookup"><span data-stu-id="9ecaa-122">Configuring Log Fields</span></span>

<span data-ttu-id="9ecaa-123">媒體基礎可讓用戶端使用屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-123">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="9ecaa-124">應用程式必須在屬性存放區中設定適當的屬性，並將其傳遞給其中一個來源解析程式方法。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-124">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="9ecaa-125">來源解析程式會依要求建立網路來源，並開啟與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-125">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="9ecaa-126">如果連接成功，用戶端會傳送本身的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-126">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="9ecaa-127">下表描述的是應用程式可以透過來源解析程式設定的記錄欄位和對應的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-127">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="9ecaa-128">此資訊不會在會話期間變更。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-128">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ecaa-129">記錄欄位</span><span class="sxs-lookup"><span data-stu-id="9ecaa-129">Logging field</span></span></th>
<th><span data-ttu-id="9ecaa-130">Description</span><span class="sxs-lookup"><span data-stu-id="9ecaa-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ecaa-131">c-playerid</span><span class="sxs-lookup"><span data-stu-id="9ecaa-131">c-playerid</span></span></td>
<td><span data-ttu-id="9ecaa-132">播放程式的唯一識別。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-132">Unique identification of the player.</span></span> <span data-ttu-id="9ecaa-133">這項資訊會在連接開始時傳送。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-133">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="9ecaa-134">一般來說，這是用戶端的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-134">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="9ecaa-135">用戶端可以將此資訊傳送到 <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> 屬性中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-135">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-136">用戶端會在連線開始時將此資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-136">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="9ecaa-137">範例值： &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="9ecaa-137">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ecaa-138">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="9ecaa-138">c-playerversion</span></span></td>
<td><span data-ttu-id="9ecaa-139">在連接開始時傳送的播放程式版本號碼。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-139">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="9ecaa-140">用戶端可以將此資訊傳送到 <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> 屬性中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-140">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-141">用戶端會在連線開始時將此資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-141">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ecaa-142">cs (使用者代理程式) </span><span class="sxs-lookup"><span data-stu-id="9ecaa-142">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="9ecaa-143">當播放程式內嵌在瀏覽器中時，所使用的瀏覽器類型。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-143">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="9ecaa-144">用戶端可以在 <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> 屬性中設定這個值。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-144">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-145">如果播放程式未內嵌，此欄位會參考產生記錄之用戶端的使用者代理程式。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-145">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="9ecaa-146">在此情況下，用戶端必須設定 <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> 屬性。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-146">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-147">用戶端會在連線開始時將此資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-147">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="9ecaa-148">範例值： &quot; Mozilla/4.0 _ (相容; _MSIE_4 01; _Windows_98) &quot;</span><span class="sxs-lookup"><span data-stu-id="9ecaa-148">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ecaa-149">cs (推薦者) </span><span class="sxs-lookup"><span data-stu-id="9ecaa-149">cs(Referer)</span></span></td>
<td><span data-ttu-id="9ecaa-150">內嵌播放程式之網頁的 URL (如果內嵌) 。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-150">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="9ecaa-151">用戶端可以將此資訊傳送到 <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> 屬性中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-151">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-152">用戶端會在連接結束時將此資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-152">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="9ecaa-153">範例值： &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="9ecaa-153">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ecaa-154">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="9ecaa-154">c-hostexe</span></span></td>
<td><span data-ttu-id="9ecaa-155">若為播放程式記錄檔專案，則為執行的主機程式 ( .exe) 。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-155">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="9ecaa-156">例如，瀏覽器中的網頁、Microsoft Visual Basic 小程式或獨立播放機。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-156">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="9ecaa-157">用戶端可以將此資訊傳送到 <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> 屬性中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-157">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-158">用戶端會在連接結束時將此資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-158">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="9ecaa-159">範例值：</span><span class="sxs-lookup"><span data-stu-id="9ecaa-159">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="9ecaa-160">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="9ecaa-160">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="9ecaa-161">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="9ecaa-161">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ecaa-162">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="9ecaa-162">c-hostexever</span></span></td>
<td><span data-ttu-id="9ecaa-163">主機程式 ( .exe) 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-163">Host program (.exe) version number.</span></span> <span data-ttu-id="9ecaa-164">用戶端可以將此資訊傳送到 <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> 屬性中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-164">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="9ecaa-165">用戶端會在連接結束時將此資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-165">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9ecaa-166">下列程式碼範例顯示用戶端應用程式如何設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-166">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="9ecaa-167">此範例會設定 "hostexe" 記錄欄位。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-167">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="9ecaa-168">正在抓取網路統計資料</span><span class="sxs-lookup"><span data-stu-id="9ecaa-168">Retrieving Network Statistics</span></span>

<span data-ttu-id="9ecaa-169">當應用程式呼叫其中一個來源解析程式方法時，它會建立網路來源、設定屬性存放區中指定的屬性，以及開啟媒體伺服器的會話。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-169">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="9ecaa-170">除了上一節所述的可設定資訊之外，還會在會話開始、串流期間以及會話關閉時，在伺服器與用戶端之間傳送額外的資料。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-170">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="9ecaa-171">應用程式可以使用 **MFNETSOURCE \_ statistics \_ service** 服務識別碼來取得網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-171">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="9ecaa-172">若要使用這項服務，應用程式可以呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函數，以取得在 [**MFNETSOURCE \_ statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) 屬性中包含網路統計資料的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-172">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="9ecaa-173">藉由提供 **MFNETSOURCE \_ STATISTICS \_ id** 列舉中所定義的對應識別碼，即可抓取特定的值。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-173">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="9ecaa-174">下列程式碼範例示範如何使用服務來取得用戶端收到的封包數目。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-174">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="9ecaa-175">下列清單描述 [**MFNETSOURCE \_ 統計資料 \_**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)識別碼中所定義的部分網路統計資料識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-175">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="9ecaa-176">網路統計資料識別碼</span><span class="sxs-lookup"><span data-stu-id="9ecaa-176">Network statistics identifier</span></span>              | <span data-ttu-id="9ecaa-177">Description</span><span class="sxs-lookup"><span data-stu-id="9ecaa-177">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecaa-178">**MFNETSOURCE \_ AVGBANDWIDTHBPS \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-178">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="9ecaa-179">用戶端連接到伺服器的平均每秒頻寬 (單位) 。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-179">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="9ecaa-180">此值會在連接的整個持續時間內計算。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-180">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="9ecaa-181">**MFNETSOURCE \_ BUFFERINGCOUNT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-181">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="9ecaa-182">用戶端播放資料流程時緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-182">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9ecaa-183">**MFNETSOURCE \_ BYTESRECEIVED \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-183">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="9ecaa-184">用戶端從伺服器接收的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-184">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="9ecaa-185">此值不包含網路堆疊所新增的任何額外負荷。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-185">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="9ecaa-186">使用不同通訊協定來串流處理的相同內容，可能會產生不同的值。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-186">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="9ecaa-187">**MFNETSOURCE \_ LINKBANDWIDTH \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-187">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="9ecaa-188">用戶端的最大可用頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-188">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9ecaa-189">**MFNETSOURCE \_ LOSTPACKETS \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-189">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="9ecaa-190">伺服器傳送的封包數，但在傳輸期間遺失，用戶端永遠不會播放。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-190">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="9ecaa-191">此值不包含 TCP 或 UDP 封包。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-191">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="9ecaa-192">**MFNETSOURCE \_ RECVPACKETS \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-192">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="9ecaa-193">從伺服器收到的封包數，其值不包括 TCP 或 UDP 封包。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-193">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="9ecaa-194">**MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-194">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="9ecaa-195">網路中的封包會在用戶端層修復和復原。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-195">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="9ecaa-196">此值不包含 TCP 或 UDP 封包。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-196">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="9ecaa-197">**MFNETSOURCE \_ RESENDSREQUESTED \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-197">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="9ecaa-198">用戶端接收新封包所提出的要求數目。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-198">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="9ecaa-199">此值不包含 TCP 或 UDP 封包。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-199">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="9ecaa-200">**MFNETSOURCE \_ RECOVEREDPACKETS \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-200">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="9ecaa-201">已復原的封包數，因為它們是透過 UDP 重新傳送。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-201">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="9ecaa-202">此值不包含 TCP 或 UDP 封包。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-202">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="9ecaa-203">此欄位包含零，除非用戶端使用 UDP 重新傳送。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-203">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="9ecaa-204">**MFNETSOURCE \_ BUFFERPROGRESS \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-204">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="9ecaa-205">在緩衝處理期間填滿的播放緩衝區百分比。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-205">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9ecaa-206">**MFNETSOURCE \_ 通訊協定 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-206">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="9ecaa-207">用來存取資料流程的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-207">Protocol used to access the stream.</span></span> <span data-ttu-id="9ecaa-208">這可能與用戶端所要求的通訊協定不同。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-208">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="9ecaa-209">**MFNETSOURCE \_ 傳輸 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9ecaa-209">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="9ecaa-210">用來傳遞資料流程的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-210">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="9ecaa-211">這必須是 UDP 或 TCP。</span><span class="sxs-lookup"><span data-stu-id="9ecaa-211">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="9ecaa-212">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ecaa-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ecaa-213">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="9ecaa-213">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="9ecaa-214">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="9ecaa-214">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

