---
title: 匯入和匯出受 DRM 保護的內容
description: 匯入和匯出受 DRM 保護的內容
ms.assetid: 1c0520dd-b698-4174-a70e-32f43e2395b1
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，匯入
- Windows Media 格式 SDK，匯出
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) ，匯入受保護的內容
- DRM (數位版權管理) ，匯入受保護的內容
- 數位版權管理 (DRM) ，匯出受保護的內容
- DRM (數位版權管理) ，匯出受保護的內容
- DRM 用戶端擴充 Api，關於
- 用戶端擴充 Api，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f368417b62c9746b6d2c9e331b9cd849455b8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675108"
---
# <a name="importing-and-exporting-drm-protected-content"></a><span data-ttu-id="0530f-122">匯入和匯出受 DRM 保護的內容</span><span class="sxs-lookup"><span data-stu-id="0530f-122">Importing and Exporting DRM Protected Content</span></span>

<span data-ttu-id="0530f-123">新 Windows Media DRM 用戶端擴充 Api 的主要角色之一，是要將受 DRM 保護的內容匯入和匯出至協力廠商 rights management 系統。</span><span class="sxs-lookup"><span data-stu-id="0530f-123">One of the primary roles of the new Windows Media DRM Client Extended APIs is to enable the import and export of DRM-protected content to third-party rights management systems.</span></span>

<span data-ttu-id="0530f-124">在您的應用程式中匯入和匯出受保護資料的主要挑戰，是要在您的系統與 DRM 子系統之間妥善共用 ASF 資料範例。</span><span class="sxs-lookup"><span data-stu-id="0530f-124">The primary challenge of importing and exporting protected data in your application is to robustly share ASF data samples between your system and the DRM subsystem.</span></span> <span data-ttu-id="0530f-125">當您的應用程式處理資料範例時，必須確保符合特定的穩定性標準，以避免可能被規避防護機制。</span><span class="sxs-lookup"><span data-stu-id="0530f-125">When your application handles data samples it has to assure that certain robustness standards are met to avoid the potential for the protection mechanism to be circumvented.</span></span> <span data-ttu-id="0530f-126">這些標準會在您同意 DRM 時同意的健全狀況和合規性規則中加以概述。</span><span class="sxs-lookup"><span data-stu-id="0530f-126">These standards are outlined in the robustness and compliance rules that you agree to when you license DRM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0530f-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="0530f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0530f-128">**關於 Windows Media DRM 用戶端擴充 Api**</span><span class="sxs-lookup"><span data-stu-id="0530f-128">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




