---
title: DirectShow 中的 DRM 支援
description: DirectShow 中的 DRM 支援
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK，DirectShow 中的 DRM 支援
- Windows Media Format SDK、DirectShow
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- 先進的系統格式 (ASF) 、DirectShow 中的 DRM 支援
- ASF (Advanced Systems Format) 、DirectShow 中的 DRM 支援
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'Advanced Systems Format (ASF) 、數位版權管理 (DRM) '
- 'ASF (Advanced Systems Format) 、數位版權管理 (DRM) '
- DirectShow，DRM 支援
- 數位版權管理 (DRM) 、DirectShow
- DRM (數位版權管理) 、DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932919"
---
# <a name="drm-support-in-directshow"></a><span data-ttu-id="23fdd-115">DirectShow 中的 DRM 支援</span><span class="sxs-lookup"><span data-stu-id="23fdd-115">DRM Support in DirectShow</span></span>

<span data-ttu-id="23fdd-116">在 DirectShow 中讀取和寫入受 DRM 保護的檔案的完成方式基本上與您直接使用 Windows Media Format SDK 的方式相同。</span><span class="sxs-lookup"><span data-stu-id="23fdd-116">Reading and writing DRM-protected files in DirectShow is done in basically the same way as when you use the Windows Media Format SDK directly.</span></span> <span data-ttu-id="23fdd-117">首先，您需要 wmstubdrm 靜態程式庫，它是與 Microsoft 分開取得的。</span><span class="sxs-lookup"><span data-stu-id="23fdd-117">To begin with, you need the wmstubdrm static library, which is obtained separately from Microsoft.</span></span> <span data-ttu-id="23fdd-118">此外，您必須執行 **IKeyProvider** 介面，讓您的應用程式在啟用 DRM 時存取 Windows MEDIA Format SDK 執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="23fdd-118">In addition, you must implement the **IKeyProvider** interface to enable your application to access the Windows Media Format SDK run-time objects when DRM is enabled.</span></span>

<span data-ttu-id="23fdd-119">套用 DRM 第1版保護時，請使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面，如在 [DIRECTSHOW 中讀取 ASF](reading-asf-files-in-directshow.md)檔案所述。</span><span class="sxs-lookup"><span data-stu-id="23fdd-119">When applying DRM version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which is obtained as described in [Reading ASF Files in DirectShow](reading-asf-files-in-directshow.md).</span></span> <span data-ttu-id="23fdd-120">套用 DRM 版本7保護時，請在 [WM ASF 寫入](wm-asf-writer-filter.md)器篩選器上呼叫 **QueryService** 來取得 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)介面，如本主題稍後的程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="23fdd-120">When applying DRM version 7 protection, obtain the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface by calling **QueryService** on the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the code snippet later in this topic.</span></span>

<span data-ttu-id="23fdd-121">所有其他 DRM 專屬設定都與 [啟用 DRM 支援](enabling-drm-support.md)中所述的設定完全相同。</span><span class="sxs-lookup"><span data-stu-id="23fdd-121">All other DRM-specific configuration is exactly the same as described in [Enabling DRM Support](enabling-drm-support.md).</span></span> <span data-ttu-id="23fdd-122">使用 **QueryService** 從 [WM ASF 讀取](wm-asf-reader-filter.md)器篩選器取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)介面。</span><span class="sxs-lookup"><span data-stu-id="23fdd-122">Use **QueryService** to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

<span data-ttu-id="23fdd-123">DirectX 9.0 包含一個範例 PlayWndASF，此為啟用 DRM 的 DirectShow 播放機應用程式，示範 DRM 第1版和第7版授權取得。</span><span class="sxs-lookup"><span data-stu-id="23fdd-123">DirectX 9.0 contains a sample, PlayWndASF, a DRM-enabled DirectShow player application that demonstrates DRM version 1 and version 7 license acquisition.</span></span> <span data-ttu-id="23fdd-124">這個範例也包含 **CKeyProvider** 類別的實作為支援 **IKeyProvider** 介面的。</span><span class="sxs-lookup"><span data-stu-id="23fdd-124">This sample also includes an implementation of the **CKeyProvider** class, which supports the **IKeyProvider** interface.</span></span>

 

 




