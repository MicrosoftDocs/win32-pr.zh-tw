---
description: 本主題說明如何使用 DirectShow 播放以 Windows Media 數位 Rights Management (DRM) 保護的媒體檔案。
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: 在 DirectShow 中讀取 DRM-Protected 的 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997319"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="731ff-103">在 DirectShow 中讀取 DRM-Protected 的 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="731ff-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="731ff-104">本主題說明如何使用 DirectShow 播放以 Windows Media 數位 Rights Management (DRM) 保護的媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="731ff-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="731ff-105">DRM 概念</span><span class="sxs-lookup"><span data-stu-id="731ff-105">DRM Concepts</span></span>

<span data-ttu-id="731ff-106">使用 Windows Media DRM 保護媒體檔案牽涉到兩個不同的步驟：</span><span class="sxs-lookup"><span data-stu-id="731ff-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="731ff-107">內容提供者會封裝檔案，也就是加密檔案並將授權資訊附加至 ASF 檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="731ff-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="731ff-108">授權資訊包括用戶端可以取得授權的 URL。</span><span class="sxs-lookup"><span data-stu-id="731ff-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="731ff-109">用戶端應用程式會取得內容的授權。</span><span class="sxs-lookup"><span data-stu-id="731ff-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="731ff-110">封裝會在散發檔案之前進行。</span><span class="sxs-lookup"><span data-stu-id="731ff-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="731ff-111">當使用者嘗試播放或複製檔案時，就會取得授權。</span><span class="sxs-lookup"><span data-stu-id="731ff-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="731ff-112">授權取得可能是 *無* 訊息或 *非無* 訊息。</span><span class="sxs-lookup"><span data-stu-id="731ff-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="731ff-113">無訊息捕獲不需要與使用者進行任何互動。</span><span class="sxs-lookup"><span data-stu-id="731ff-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="731ff-114">非無訊息取得需要應用程式開啟瀏覽器視窗，並向使用者顯示網頁。</span><span class="sxs-lookup"><span data-stu-id="731ff-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="731ff-115">屆時，使用者可能需要為內容提供者提供一種資訊。</span><span class="sxs-lookup"><span data-stu-id="731ff-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="731ff-116">不過，這兩種授權類型都需要用戶端向授權伺服器提交 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="731ff-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="731ff-117">DRM 版本</span><span class="sxs-lookup"><span data-stu-id="731ff-117">DRM Versions</span></span>

<span data-ttu-id="731ff-118">有數種版本的 Windows Media DRM 存在。</span><span class="sxs-lookup"><span data-stu-id="731ff-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="731ff-119">從用戶端應用程式的觀點來看，它們可以分為兩類： DRM 第1版，以及 DRM 7 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="731ff-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="731ff-120"> (第二個類別包含 DRM 9 和10版，以及第7版。 ) 以這種方式分類 DRM 版本的原因，是因為第1版的授權處理方式與7版或更新版本的授權稍有不同。</span><span class="sxs-lookup"><span data-stu-id="731ff-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="731ff-121">在此檔中， *第7版授權* 表示第7版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="731ff-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="731ff-122">區分 drm 封裝與 DRM 授權也很重要。</span><span class="sxs-lookup"><span data-stu-id="731ff-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="731ff-123">如果是使用 Windows Media Rights Manager 7 版或更新版本來封裝檔案，DRM 標頭除了第7版授權 URL 之外，還可以包含第1版授權 URL。</span><span class="sxs-lookup"><span data-stu-id="731ff-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="731ff-124">第1版授權 URL 可讓不支援第7版的舊版播放程式取得內容的授權。</span><span class="sxs-lookup"><span data-stu-id="731ff-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="731ff-125">不過，反向並不是正確的，因此第1版封裝的檔案不能有第7版授權 URL。</span><span class="sxs-lookup"><span data-stu-id="731ff-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="731ff-126">應用程式安全性層級</span><span class="sxs-lookup"><span data-stu-id="731ff-126">Application Security Level</span></span>

<span data-ttu-id="731ff-127">若要播放受 DRM 保護的檔案，用戶端應用程式必須連結至 Microsoft 以二進位格式提供的靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="731ff-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="731ff-128">此程式庫可唯一識別應用程式，有時稱為存根程式庫。</span><span class="sxs-lookup"><span data-stu-id="731ff-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="731ff-129">存根程式庫具有指派的安全性層級，其值取決於您取得存根程式庫時簽署的授權合約。</span><span class="sxs-lookup"><span data-stu-id="731ff-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="731ff-130">內容提供者會設定取得授權所需的最低安全性層級。</span><span class="sxs-lookup"><span data-stu-id="731ff-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="731ff-131">如果存根程式庫的安全性層級小於授權伺服器所需的最低安全性層級，則應用程式無法取得授權。</span><span class="sxs-lookup"><span data-stu-id="731ff-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="731ff-132">個人化</span><span class="sxs-lookup"><span data-stu-id="731ff-132">Individualization</span></span>

<span data-ttu-id="731ff-133">為了提高安全性，應用程式可能會更新用戶端電腦上的 DRM 元件。</span><span class="sxs-lookup"><span data-stu-id="731ff-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="731ff-134">這個稱為「個人化」的更新，會區分使用者的應用程式複本與相同應用程式的所有其他複本。</span><span class="sxs-lookup"><span data-stu-id="731ff-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="731ff-135">受保護檔案的 DRM 標頭可能會指定最小的個人化層級。</span><span class="sxs-lookup"><span data-stu-id="731ff-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="731ff-136"> (需詳細資訊，請參閱 Windows Media Rights Manager SDK 中的 WMRMHeader IndividualizedVersion 檔。 ) </span><span class="sxs-lookup"><span data-stu-id="731ff-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="731ff-137">由於 Microsoft 個人級服務會處理來自使用者的資訊，因此您必須在應用程式 individualizes 之前，顯示 Microsoft 網站上的 Microsoft 隱私權原則或提供該頁面的連結： <https://go.microsoft.com/fwlink/p/?linkid=10240> 。</span><span class="sxs-lookup"><span data-stu-id="731ff-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="731ff-138">提供軟體憑證</span><span class="sxs-lookup"><span data-stu-id="731ff-138">Provide the Software Certificate</span></span>

<span data-ttu-id="731ff-139">若要讓應用程式使用 DRM 授權，應用程式必須提供軟體憑證或 *金鑰* 給篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="731ff-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="731ff-140">此索引鍵包含在為應用程式個人化的靜態程式庫中。</span><span class="sxs-lookup"><span data-stu-id="731ff-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="731ff-141">如需取得個別程式庫的詳細資訊，請參閱 Windows Media Format SDK 檔中的 [取得必要的 DRM 程式庫](../wmformat/obtaining-the-required-drm-library.md) 。</span><span class="sxs-lookup"><span data-stu-id="731ff-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="731ff-142">若要提供軟體金鑰，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="731ff-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="731ff-143">靜態程式庫的連結。</span><span class="sxs-lookup"><span data-stu-id="731ff-143">Link to the static library.</span></span>
2.  <span data-ttu-id="731ff-144">執行 **IServiceProvider** 介面。</span><span class="sxs-lookup"><span data-stu-id="731ff-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="731ff-145">查詢 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) 介面的篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="731ff-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="731ff-146">使用 **IServiceProvider 的** 指標來呼叫 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 。</span><span class="sxs-lookup"><span data-stu-id="731ff-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="731ff-147">篩選圖形管理員會呼叫 **IServiceProvider：： QueryService**，並為服務識別碼指定 **IID \_ IWMReader** 。</span><span class="sxs-lookup"><span data-stu-id="731ff-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="731ff-148">在 **QueryService** 的執行中，呼叫 [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) 以建立軟體金鑰。</span><span class="sxs-lookup"><span data-stu-id="731ff-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="731ff-149">下列程式碼顯示如何執行 **QueryService** 方法：</span><span class="sxs-lookup"><span data-stu-id="731ff-149">The following code shows how to implement the **QueryService** method:</span></span>


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



<span data-ttu-id="731ff-150">下列程式碼顯示如何在篩選圖形管理員上呼叫 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) ：</span><span class="sxs-lookup"><span data-stu-id="731ff-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a><span data-ttu-id="731ff-151">建立播放圖表</span><span class="sxs-lookup"><span data-stu-id="731ff-151">Building the Playback Graph</span></span>

<span data-ttu-id="731ff-152">若要播放受 DRM 保護的 ASF 檔案，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="731ff-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="731ff-153">建立 [篩選圖形管理員](filter-graph-manager.md) ，並使用 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面註冊圖形事件。</span><span class="sxs-lookup"><span data-stu-id="731ff-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="731ff-154">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器的新實例。</span><span class="sxs-lookup"><span data-stu-id="731ff-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="731ff-155">呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選準則加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="731ff-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="731ff-156">查詢 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) 介面的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="731ff-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="731ff-157">以檔案的 URL 呼叫 [**IFileSourceFilter：： Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) 。</span><span class="sxs-lookup"><span data-stu-id="731ff-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="731ff-158">處理 [**EC \_ WMT \_ 事件**](ec-wmt-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="731ff-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="731ff-159">在第一個 [**EC \_ WMT \_ 事件**](ec-wmt-event.md)事件上，查詢 **IServiceProvider** 介面的 [WM ASF 讀取](wm-asf-reader-filter.md)器篩選器。</span><span class="sxs-lookup"><span data-stu-id="731ff-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="731ff-160">呼叫 **IServiceProvider：： QueryService** 來取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="731ff-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="731ff-161">呼叫 [**IGraphBuilder：： render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 以轉譯 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="731ff-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="731ff-162">開啟受 DRM 保護的檔案時，請勿呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 來建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="731ff-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="731ff-163">在取得 DRM 授權之前，「WM ASF 讀取器」篩選器無法連線到任何其他篩選器。</span><span class="sxs-lookup"><span data-stu-id="731ff-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="731ff-164">此步驟需要應用程式使用 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) 介面（必須從篩選中取得），如步驟7–8所述。</span><span class="sxs-lookup"><span data-stu-id="731ff-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="731ff-165">因此，您必須建立篩選器，並將它新增至圖形</span><span class="sxs-lookup"><span data-stu-id="731ff-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="731ff-166">在將 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器新增至圖形 (步驟 3) 之前，請務必 (步驟 1) 註冊圖形事件，因為應用程式必須處理 [**EC \_ WMT \_ 事件**](ec-wmt-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="731ff-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="731ff-167">呼叫 [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) 時，會傳送事件 (步驟 5) 。</span><span class="sxs-lookup"><span data-stu-id="731ff-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="731ff-168">下列程式碼顯示如何建立圖形：</span><span class="sxs-lookup"><span data-stu-id="731ff-168">The following code shows how to build the graph:</span></span>


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="731ff-169">C++</span><span class="sxs-lookup"><span data-stu-id="731ff-169">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="731ff-170">在先前的程式碼中，此函式會 `RenderOutputPins` 列舉 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器上的輸出圖釘，並針對每個 pin 呼叫 [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 。</span><span class="sxs-lookup"><span data-stu-id="731ff-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



<span data-ttu-id="731ff-171">下列程式碼說明如何從 [WM ASF 讀取器](wm-asf-reader-filter.md)取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)介面的指標：</span><span class="sxs-lookup"><span data-stu-id="731ff-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="731ff-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="731ff-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="731ff-173">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="731ff-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
