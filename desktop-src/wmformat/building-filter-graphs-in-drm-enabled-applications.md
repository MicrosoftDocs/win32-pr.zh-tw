---
title: 在 DRM-Enabled 應用程式中建立篩選圖形
description: 在 DRM-Enabled 應用程式中建立篩選圖形
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK，建立篩選圖形
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，啟用 DRM 的應用程式
- Advanced Systems Format (ASF) ，建立篩選圖形
- ASF (Advanced Systems Format) ，建立篩選圖形
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、已啟用 DRM 的應用程式
- ASF (Advanced Systems Format) 、已啟用 DRM 的應用程式
- DirectShow，建立篩選圖形
- DirectShow、啟用 DRM 的應用程式
- 數位版權管理 (DRM) 、DirectShow
- DRM (數位版權管理) 、DirectShow
- 數位版權管理 (DRM) ，建立篩選圖形
- DRM (數位版權管理) ，建立篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314331"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="9bd57-118">在 DRM-Enabled 應用程式中建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="9bd57-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="9bd57-119">如果您的 DirectShow 應用程式支援播放受 DRM 保護的檔案，您通常不應該使用 **RenderFile** 來建立篩選圖形，因為在檔案開啟之前，沒有任何方法可指定您要要求的 DRM 許可權。</span><span class="sxs-lookup"><span data-stu-id="9bd57-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="9bd57-120">依預設，WM ASF 讀取器只會要求播放許可權。</span><span class="sxs-lookup"><span data-stu-id="9bd57-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="9bd57-121">篩選不會加入至圖形，因此應用程式無法探索到檔案，直到檔案成功開啟為止。</span><span class="sxs-lookup"><span data-stu-id="9bd57-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="9bd57-122">若要使用 [WM ASF 讀取](wm-asf-reader-filter.md)器建立啟用 DRM 的播放圖形，您必須使用 **CoCreateInstance** 將篩選具現化、使用 **IGraphBuilder：： AddFilter** 將它新增至篩選圖形、加以設定，然後轉譯其輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="9bd57-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="9bd57-123">這項技術會在 PlayWndASF 範例中示範。</span><span class="sxs-lookup"><span data-stu-id="9bd57-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="9bd57-124">當您以這種方式建立圖形時，您已經擁有可用來呼叫 **QueryService** 以取得 **IWMDRMWriter** 的 **IBaseFilter** 指標。</span><span class="sxs-lookup"><span data-stu-id="9bd57-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="9bd57-125">不過，在由 WM ASF 讀取器內部建立 Windows Media Format SDK 讀取器物件之前，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="9bd57-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="9bd57-126">應用程式必須設定 DRM 許可權的第一個機會，是在其 WMT \_ 沒有許可權的範例 \_ \_ 事件處理常式中，如下列程式碼片段所示：</span><span class="sxs-lookup"><span data-stu-id="9bd57-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="9bd57-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bd57-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bd57-128">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="9bd57-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="9bd57-129">**DRM 屬性清單**</span><span class="sxs-lookup"><span data-stu-id="9bd57-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="9bd57-130">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="9bd57-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="9bd57-131">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="9bd57-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="9bd57-132">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="9bd57-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="9bd57-133">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="9bd57-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




