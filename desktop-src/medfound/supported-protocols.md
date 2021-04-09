---
description: 支援的通訊協定
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: 支援的通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691596"
---
# <a name="supported-protocols"></a><span data-ttu-id="b74d1-103">支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="b74d1-103">Supported Protocols</span></span>

<span data-ttu-id="b74d1-104">媒體基礎支援下列通訊協定：</span><span class="sxs-lookup"><span data-stu-id="b74d1-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="b74d1-105">即時串流通訊協定 (RTSP) </span><span class="sxs-lookup"><span data-stu-id="b74d1-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="b74d1-106">RTSP 主要用於串流處理媒體內容。</span><span class="sxs-lookup"><span data-stu-id="b74d1-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="b74d1-107">它可以使用 UDP 或 TCP 作為傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="b74d1-108">UDP 是內容傳遞最有效率的方式，因為頻寬額外負荷低於 TCP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="b74d1-109">雖然 TCP 通訊協定可確保可靠的封包傳遞，但 TCP 並不適用于數位媒體串流，但有效使用頻寬比偶爾遺失的封包來得重要。</span><span class="sxs-lookup"><span data-stu-id="b74d1-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="b74d1-110">超文字傳輸通訊協定 (HTTP)</span><span class="sxs-lookup"><span data-stu-id="b74d1-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="b74d1-111">HTTP 使用 TCP，並由 web 伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="b74d1-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="b74d1-112">"Httpd://" 配置表示來源可從 web 伺服器下載。</span><span class="sxs-lookup"><span data-stu-id="b74d1-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="b74d1-113">HTTP 也適用于防火牆，其通常設定為接受 HTTP 要求，且通常會拒絕其他串流通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="b74d1-114">應用程式可以使用 [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) 介面取得媒體基礎所支援的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="b74d1-115">若要這樣做，應用程式必須先藉由呼叫 [**IMFNetSchemeHandlerConfig：： GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) 來取得通訊協定的數目，然後藉由呼叫 [**IMFNetSchemeHandlerConfig：： GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype)取得以索引為基礎的通訊協定類型。</span><span class="sxs-lookup"><span data-stu-id="b74d1-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="b74d1-116">這個方法會傳回 [**MFNETSOURCE \_ 通訊協定 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) 列舉中所定義的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b74d1-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="b74d1-117">應用程式也可以藉由呼叫 [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) 函數來取得來源解析程式所支援的配置。</span><span class="sxs-lookup"><span data-stu-id="b74d1-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="b74d1-118">通訊協定變換</span><span class="sxs-lookup"><span data-stu-id="b74d1-118">Protocol Rollover</span></span>

<span data-ttu-id="b74d1-119">當應用程式將 "mms://" 指定為 URL 配置時，來源解析程式會執行 *通訊協定變換* 操作。</span><span class="sxs-lookup"><span data-stu-id="b74d1-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="b74d1-120">在此程式中，來源解析程式會決定網路來源用來取得內容的最佳通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="b74d1-121">一般來說，針對媒體串流，具有 UDP (RTSPU) 的 RTSP 比 HTTP 更有效率。</span><span class="sxs-lookup"><span data-stu-id="b74d1-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="b74d1-122">但是，如果內容是裝載在 web 伺服器上，則 HTTP 是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="b74d1-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="b74d1-123">當嘗試使用 URL 配置中指定的通訊協定失敗時，也會發生通訊協定變換。</span><span class="sxs-lookup"><span data-stu-id="b74d1-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="b74d1-124">例如，當防火牆封鎖 UDP 封包時，通訊協定可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="b74d1-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="b74d1-125">在此情況下，來源解析程式會切換至 HTTP。</span><span class="sxs-lookup"><span data-stu-id="b74d1-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="b74d1-126">如果 URL 配置包含特定的通訊協定（例如 "rtspu://"），則不適用通訊協定變換。</span><span class="sxs-lookup"><span data-stu-id="b74d1-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="b74d1-127">此外，如果驗證失敗，或伺服器已達到用戶端連線的限制，就不會執行變換。</span><span class="sxs-lookup"><span data-stu-id="b74d1-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="b74d1-128">建議應用程式指定 "mms://" 配置，並允許來源解析程式為案例選取最佳的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="b74d1-129">下表列出變換順序。</span><span class="sxs-lookup"><span data-stu-id="b74d1-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b74d1-130">允許的架構</span><span class="sxs-lookup"><span data-stu-id="b74d1-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="b74d1-131">通訊協定變換順序</span><span class="sxs-lookup"><span data-stu-id="b74d1-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b74d1-132">mms://或 rtsp://</span><span class="sxs-lookup"><span data-stu-id="b74d1-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="b74d1-133">快速快取已啟用：</span><span class="sxs-lookup"><span data-stu-id="b74d1-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="b74d1-134">使用 TCP 的 RTSP (RTSPT) </span><span class="sxs-lookup"><span data-stu-id="b74d1-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="b74d1-135">使用 UDP (RTSPU) 的 RTSP</span><span class="sxs-lookup"><span data-stu-id="b74d1-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="b74d1-136">HTTP 串流</span><span class="sxs-lookup"><span data-stu-id="b74d1-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="b74d1-137"> (HTTPD) 的 HTTP 下載</span><span class="sxs-lookup"><span data-stu-id="b74d1-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="b74d1-138">快取已停用：</span><span class="sxs-lookup"><span data-stu-id="b74d1-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="b74d1-139">RTSPU</span><span class="sxs-lookup"><span data-stu-id="b74d1-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="b74d1-140">RTSPT</span><span class="sxs-lookup"><span data-stu-id="b74d1-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="b74d1-141">HTTP 串流</span><span class="sxs-lookup"><span data-stu-id="b74d1-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="b74d1-142">HTTP 下載</span><span class="sxs-lookup"><span data-stu-id="b74d1-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b74d1-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="b74d1-143">rtspu://</span></span></td>
<td><span data-ttu-id="b74d1-144">RTSPU</span><span class="sxs-lookup"><span data-stu-id="b74d1-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b74d1-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="b74d1-145">rtspt://</span></span></td>
<td><span data-ttu-id="b74d1-146">RTSPT</span><span class="sxs-lookup"><span data-stu-id="b74d1-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b74d1-147"> https://</span><span class="sxs-lookup"><span data-stu-id="b74d1-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="b74d1-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="b74d1-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="b74d1-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="b74d1-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b74d1-150">HTTPd://</span><span class="sxs-lookup"><span data-stu-id="b74d1-150">httpd://</span></span></td>
<td><span data-ttu-id="b74d1-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="b74d1-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="b74d1-152">正在抓取目前的通訊協定</span><span class="sxs-lookup"><span data-stu-id="b74d1-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="b74d1-153">在通訊協定變換作業之後，網路來源可能會使用應用程式在 URL 配置中所指定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="b74d1-154">在網路來源建立與媒體伺服器的連線之後，應用程式就可以使用通訊協定變換結果。</span><span class="sxs-lookup"><span data-stu-id="b74d1-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="b74d1-155">為了取得用來取得內容的通訊協定和傳輸，應用程式可以從網路來源抓取 [MFNETSOURCE \_ 通訊協定](mfnetsource-protocol-property.md)屬性的屬性值，以及 **IPropertyStore** 物件的 [MFNETSOURCE \_ 傳輸](mfnetsource-transport-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="b74d1-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="b74d1-156">下列程式碼顯示如何取得這些值。</span><span class="sxs-lookup"><span data-stu-id="b74d1-156">The following code shows how to get these values.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



<span data-ttu-id="b74d1-157">在上述的範例程式碼中， **IPropertyStore：： GetValue** 會抓取 MFNETSOURCE \_ 通訊協定值，這是 [**MFNETSOURCE \_ 通訊協定 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="b74d1-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="b74d1-158">針對 MFNETSOURCE \_ 傳輸，此值是 [**MFNETSOURCE \_ 傳輸 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="b74d1-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="b74d1-159">或者，應用程式可以使用 MFNETSOURCE \_ STATISTICS service 服務來取得相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b74d1-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="b74d1-160">若要使用這種服務，應用程式可以呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函數，從網路來源取得屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="b74d1-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="b74d1-161">這個屬性存放區包含 [MFNETSOURCE \_ statistics](mfnetsource-statistics-property.md) 屬性中的網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="b74d1-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="b74d1-162">您可以藉由指定 MFNETSOURCE \_ 通訊協定 \_ 識別碼和 MFNETSOURCE \_ 傳輸 \_ 識別碼（定義于 [**MFNETSOURCE \_ 統計資料 \_ 識別碼**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) 列舉中）來抓取通訊協定和傳輸值。</span><span class="sxs-lookup"><span data-stu-id="b74d1-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="b74d1-163">下列程式碼顯示如何使用 MFNETSOURCE \_ STATISTICS service 服務來取得通訊協定和傳輸值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b74d1-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="b74d1-164">啟用和停用通訊協定</span><span class="sxs-lookup"><span data-stu-id="b74d1-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="b74d1-165">應用程式可以設定網路來源，以便在變換程式期間略過特定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="b74d1-166">若要這樣做，會使用網路來源屬性來停用特定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="b74d1-167">下表顯示其所控制的屬性和通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b74d1-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="b74d1-168">屬性</span><span class="sxs-lookup"><span data-stu-id="b74d1-168">Property</span></span>                                                                    | <span data-ttu-id="b74d1-169">描述</span><span class="sxs-lookup"><span data-stu-id="b74d1-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="b74d1-170">MFNETSOURCE \_ 啟用 \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="b74d1-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="b74d1-171">啟用或停用 HTTP 和 HTTPD。</span><span class="sxs-lookup"><span data-stu-id="b74d1-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="b74d1-172">MFNETSOURCE \_ 啟用 \_ RTSP</span><span class="sxs-lookup"><span data-stu-id="b74d1-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="b74d1-173">啟用或停用 RTSPU 和 RTSPT。</span><span class="sxs-lookup"><span data-stu-id="b74d1-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="b74d1-174">MFNETSOURCE \_ 啟用 \_ TCP</span><span class="sxs-lookup"><span data-stu-id="b74d1-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="b74d1-175">啟用或停用 RTSPT。</span><span class="sxs-lookup"><span data-stu-id="b74d1-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="b74d1-176">MFNETSOURCE \_ 啟用 \_ UDP</span><span class="sxs-lookup"><span data-stu-id="b74d1-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="b74d1-177">啟用或停用 RTSPU。</span><span class="sxs-lookup"><span data-stu-id="b74d1-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="b74d1-178">MFNETSOURCE \_ 啟用 \_ 下載</span><span class="sxs-lookup"><span data-stu-id="b74d1-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="b74d1-179">啟用或停用 HTTPD。</span><span class="sxs-lookup"><span data-stu-id="b74d1-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="b74d1-180">MFNETSOURCE \_ 啟用 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="b74d1-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="b74d1-181">啟用或停用 RTSPU、RTSPT 和 HTTP。</span><span class="sxs-lookup"><span data-stu-id="b74d1-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b74d1-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="b74d1-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b74d1-183">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="b74d1-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




