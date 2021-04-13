---
title: 建立受保護的檔案
description: 建立受保護的檔案
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK，建立受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，建立受保護的檔案
- ASF (Advanced Systems Format) ，建立受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，建立受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314262"
---
# <a name="creating-protected-files"></a><span data-ttu-id="54b77-115">建立受保護的檔案</span><span class="sxs-lookup"><span data-stu-id="54b77-115">Creating Protected Files</span></span>

<span data-ttu-id="54b77-116">若要使用 DRM 第1版或 DRM 版本7和更新版本來建立受保護的數位媒體檔案，請連結至您從 Microsoft 取得的 WMStubDRM .lib 檔案，然後建立寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="54b77-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="54b77-117">針對第1版保護，請使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面設定您想要套用的 DRM 屬性。</span><span class="sxs-lookup"><span data-stu-id="54b77-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="54b77-118">若為7版和更新版本，請使用 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) 介面方法。</span><span class="sxs-lookup"><span data-stu-id="54b77-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="54b77-119">下列主題將詳細說明如何保護檔案。</span><span class="sxs-lookup"><span data-stu-id="54b77-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="54b77-120">使用 DRM 第1版保護檔案</span><span class="sxs-lookup"><span data-stu-id="54b77-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="54b77-121">使用 DRM 7 版或更新版本保護檔案</span><span class="sxs-lookup"><span data-stu-id="54b77-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="54b77-122">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="54b77-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="54b77-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="54b77-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54b77-124">**DRM 屬性清單**</span><span class="sxs-lookup"><span data-stu-id="54b77-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="54b77-125">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="54b77-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="54b77-126">**DRM 版本**</span><span class="sxs-lookup"><span data-stu-id="54b77-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="54b77-127">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="54b77-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="54b77-128">**取得必要的 DRM 程式庫**</span><span class="sxs-lookup"><span data-stu-id="54b77-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="54b77-129">**讀取受保護的檔案**</span><span class="sxs-lookup"><span data-stu-id="54b77-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




