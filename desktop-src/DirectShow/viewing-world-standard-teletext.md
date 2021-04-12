---
description: 觀賞全球標準 Teletext
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: 觀賞全球標準 Teletext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318727"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="03e58-103">觀賞全球標準 Teletext</span><span class="sxs-lookup"><span data-stu-id="03e58-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="03e58-104">Windows Vista 和更新版本的作業系統已移除此功能。</span><span class="sxs-lookup"><span data-stu-id="03e58-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="03e58-105">它可在 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="03e58-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="03e58-106">全球標準 Teletext (WST) 會以垂直空白間隔編碼， (VBI) 的類比電視信號。</span><span class="sxs-lookup"><span data-stu-id="03e58-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="03e58-107">預覽 teletext 的篩選圖形類似于用來查看隱藏式輔助字幕的圖形。</span><span class="sxs-lookup"><span data-stu-id="03e58-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="03e58-108">下圖說明此圖形。</span><span class="sxs-lookup"><span data-stu-id="03e58-108">The following diagram illustrates this graph.</span></span>

![wst 預覽圖形](images/vidcap10.png)

<span data-ttu-id="03e58-110">此圖表會使用下列篩選器來顯示 WST：</span><span class="sxs-lookup"><span data-stu-id="03e58-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="03e58-111">[T/接收到接收的轉換器](tee-sink-to-sink-converter.md)。</span><span class="sxs-lookup"><span data-stu-id="03e58-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="03e58-112">接受 capture 篩選器中的 VBI 資訊，並將其分割為信號上的每個資料服務的個別資料流程。</span><span class="sxs-lookup"><span data-stu-id="03e58-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="03e58-113">[WST 編解碼器](wst-codec-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="03e58-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="03e58-114">解碼 VBI 範例中的 Teletext 資料。</span><span class="sxs-lookup"><span data-stu-id="03e58-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="03e58-115">[WST 解碼器](wst-decoder-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="03e58-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="03e58-116">轉譯 teletext 的資料，並將文字繪製到點陣圖上。</span><span class="sxs-lookup"><span data-stu-id="03e58-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="03e58-117">下游篩選 (在此案例中，重迭混音器) 將點陣圖重迭到影片。</span><span class="sxs-lookup"><span data-stu-id="03e58-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="03e58-118">「捕獲圖形產生器」的 **RenderStream** 方法不會直接支援 WST 篩選，因此您的應用程式必須執行一些額外的工作。</span><span class="sxs-lookup"><span data-stu-id="03e58-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="03e58-119">將覆迭混音器篩選器新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="03e58-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="03e58-120">下列程式碼會使用 [依 CLSID 加入篩選器](add-a-filter-by-clsid.md)中所述的 AddFilterByCLSID 函數。</span><span class="sxs-lookup"><span data-stu-id="03e58-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="03e58-121"> (AddFilterByCLSID 不是 DirectShow API。 ) </span><span class="sxs-lookup"><span data-stu-id="03e58-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="03e58-122">透過重迭混音器，將預覽釘選到影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="03e58-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="03e58-123">您可以使用 **RenderStream** 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="03e58-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="03e58-124">將端對端/接收到接收轉換器篩選加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="03e58-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="03e58-125">下列程式碼使用 [建立 Kernel-Mode 篩選準則](creating-kernel-mode-filters.md)中所述的 CreateKernelFilter 函數。</span><span class="sxs-lookup"><span data-stu-id="03e58-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="03e58-126"> (CreateKernelFilter 不是 DirectShow API。 ) </span><span class="sxs-lookup"><span data-stu-id="03e58-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="03e58-127">將 WST 編解碼器篩選器新增至篩選圖形：</span><span class="sxs-lookup"><span data-stu-id="03e58-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="03e58-128">呼叫 **RenderStream** 以將捕獲篩選器的 VBI 釘選到「t/接收」和「接收端對接收」轉換器，並將 T-sql 編解碼器篩選準則的 t/接收到接收轉換器：</span><span class="sxs-lookup"><span data-stu-id="03e58-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="03e58-129">再次呼叫 **RenderStream** ，以將 WST 編解碼器篩選器連線到重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="03e58-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="03e58-130">WST 解碼器篩選器會自動帶入圖形中。</span><span class="sxs-lookup"><span data-stu-id="03e58-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="03e58-131">請記得釋放所有篩選介面。</span><span class="sxs-lookup"><span data-stu-id="03e58-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="03e58-132">目前，WST 解碼器篩選器不支援連接到 (VMR) 篩選器的視頻混合轉譯器。</span><span class="sxs-lookup"><span data-stu-id="03e58-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="03e58-133">因此，您必須使用舊版影片轉譯器篩選器來查看 teletext。</span><span class="sxs-lookup"><span data-stu-id="03e58-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="03e58-134">如果捕捉篩選器有影片埠 VBI pin (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI) ，請將它連線到 [VBI Surface](vbi-surface-allocator.md) 配置器篩選器。</span><span class="sxs-lookup"><span data-stu-id="03e58-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="03e58-135">否則，圖形將無法正確執行。</span><span class="sxs-lookup"><span data-stu-id="03e58-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="03e58-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span><span class="sxs-lookup"><span data-stu-id="03e58-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="03e58-137"> (兩個函式都不是 DirectShow API。 ) </span><span class="sxs-lookup"><span data-stu-id="03e58-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="03e58-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="03e58-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03e58-139">隱藏式輔助字幕和 Teletext</span><span class="sxs-lookup"><span data-stu-id="03e58-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



