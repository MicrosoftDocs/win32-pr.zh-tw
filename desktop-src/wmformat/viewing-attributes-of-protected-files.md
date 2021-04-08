---
title: 查看受保護檔案的屬性
description: 查看受保護檔案的屬性
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK，查看受保護檔案的屬性
- Windows Media Format SDK，受保護檔案的屬性
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，查看受保護檔案的屬性
- ASF (Advanced Systems Format) ，查看受保護檔案的屬性
- Advanced Systems Format (ASF) 、受保護檔案的屬性
- ASF (Advanced Systems Format) ，受保護檔案的屬性
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- 數位版權管理 (DRM) ，查看受保護檔案的屬性
- DRM (數位版權管理) ，查看受保護檔案的屬性
- 數位版權管理 (DRM) ，受保護檔案的屬性
- DRM (數位版權管理) ，受保護檔案的屬性
- 數位版權管理 (DRM) 、受保護的檔案
- DRM (數位版權管理) 、受保護的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681383"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="df127-118">查看受保護檔案的屬性</span><span class="sxs-lookup"><span data-stu-id="df127-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="df127-119">在某些情況下，您可能需要在檔案中取出某些 DRM 屬性，而不需要實際存取檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="df127-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="df127-120">這項功能很有用，例如，應用程式會根據檔案標頭中的資訊，以不同的方式處理批次的檔案。</span><span class="sxs-lookup"><span data-stu-id="df127-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="df127-121">在舊版的 Windows Media Format SDK 中，應用程式必須連結到 DRM 靜態程式庫，才能開啟任何受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="df127-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="df127-122">沒有 DRM 程式庫的應用程式可以使用中繼資料編輯器物件上的 [**IWMDRMEditor：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) 介面來檢查特定的 DRM 屬性。</span><span class="sxs-lookup"><span data-stu-id="df127-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="df127-123">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="df127-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="df127-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="df127-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df127-125">**DRM 屬性清單**</span><span class="sxs-lookup"><span data-stu-id="df127-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="df127-126">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="df127-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="df127-127">**IWMDRMEditor 介面**</span><span class="sxs-lookup"><span data-stu-id="df127-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




