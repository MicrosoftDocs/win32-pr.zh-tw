---
title: 明確授權和包含清單
description: 明確授權和包含清單
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media Format SDK，DRM 匯出
- Windows Media 格式 SDK，匯出
- Windows Media Format SDK、明確授權和包含清單
- Windows Media Format SDK，授權清單
- Windows Media Format SDK，包含清單
- 數位版權管理 (DRM) 、匯出
- DRM (數位版權管理) ，匯出
- 數位版權管理 (DRM) 、明確授權和包含清單
- DRM (數位版權管理) 、明確授權和包含清單
- 數位版權管理 (DRM) 、授權清單
- DRM (數位版權管理) 、授權清單
- 數位版權管理 (DRM) ，包含清單
- DRM (數位版權管理) ，包含清單
- DRM 用戶端擴充 Api、明確授權和包含清單
- 用戶端擴充 Api、明確授權和包含清單
- DRM 用戶端擴充 Api、授權清單
- 用戶端擴充 Api、授權清單
- DRM 用戶端擴充 Api，包含清單
- 用戶端擴充 Api，包含清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374410"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="3345c-122">明確授權和包含清單</span><span class="sxs-lookup"><span data-stu-id="3345c-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="3345c-123">授權可包含包含清單，以明確授權將受 Windows Media DRM 保護的內容匯出至 (CPS) 的其他內容保護設定。</span><span class="sxs-lookup"><span data-stu-id="3345c-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="3345c-124">根據您在 Microsoft 輸入的許可合約條款來啟用 DRM 匯出，您只能匯出到授權包含清單中所識別的有效 CPS。</span><span class="sxs-lookup"><span data-stu-id="3345c-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="3345c-125">包含清單是全域唯一識別碼 (Guid 的系結陣列，) 每個都代表可匯出內容的特定授權 CPS。</span><span class="sxs-lookup"><span data-stu-id="3345c-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="3345c-126">包含清單中列出的 Guid 與輸出保護層級無關， (OPL) 和內容保護層級 (CPL) 。</span><span class="sxs-lookup"><span data-stu-id="3345c-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="3345c-127">強制執行這些限制是您的應用程式的責任。</span><span class="sxs-lookup"><span data-stu-id="3345c-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="3345c-128">在壓縮的內容上執行 Windows Media DRM 匯出時，您可以透過 [**IWMDRMLicense：： GetInclusionList**](iwmdrmlicense-getinclusionlist.md) 方法存取包含清單。</span><span class="sxs-lookup"><span data-stu-id="3345c-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="3345c-129">在未壓縮的內容上執行 Windows Media DRM 匯出時，請使用 [**IWMDRMReader3：： GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) 方法。</span><span class="sxs-lookup"><span data-stu-id="3345c-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="3345c-130">若要將新的內容保護系統註冊為 windows media drm 匯出合規性規則中允許的匯出，請聯絡 wmla@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="3345c-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3345c-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="3345c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3345c-132">**DRM 匯出**</span><span class="sxs-lookup"><span data-stu-id="3345c-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 




