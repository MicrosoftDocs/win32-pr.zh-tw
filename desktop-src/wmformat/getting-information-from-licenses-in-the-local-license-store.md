---
title: 從本機授權存放中的授權取得資訊
description: 從本機授權存放中的授權取得資訊
ms.assetid: dd1abd5e-6536-4d8f-9607-b800c5a16d04
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，本機授權存放
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) 的本機授權商店
- DRM (數位版權管理) ，本機授權商店
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api，本機授權存放
- 用戶端擴充 Api，本機授權存放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c7b9351535ba15c75da8a2ee3ddad1b273805
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965570"
---
# <a name="getting-information-from-licenses-in-the-local-license-store"></a><span data-ttu-id="f8346-122">從本機授權存放中的授權取得資訊</span><span class="sxs-lookup"><span data-stu-id="f8346-122">Getting Information from Licenses in the Local License Store</span></span>

<span data-ttu-id="f8346-123">Windows Media DRM 用戶端擴充 Api 提供多種方式來取得本機授權存放區中授權所授與的許可權資訊。</span><span class="sxs-lookup"><span data-stu-id="f8346-123">The Windows Media DRM Client Extended APIs provide multiple ways to get information about the rights granted by licenses in the local license store.</span></span> <span data-ttu-id="f8346-124">下列主題將說明如何取得這些不同類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="f8346-124">The following topics describe how to get these various types of information.</span></span>



| <span data-ttu-id="f8346-125">主題</span><span class="sxs-lookup"><span data-stu-id="f8346-125">Topic</span></span>                                                                                                  | <span data-ttu-id="f8346-126">描述</span><span class="sxs-lookup"><span data-stu-id="f8346-126">Description</span></span>                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8346-127">查詢簡單的許可權資訊</span><span class="sxs-lookup"><span data-stu-id="f8346-127">Querying for Simple Rights Information</span></span>](querying-for-simple-rights-information.md)                   | <span data-ttu-id="f8346-128">描述如何取得受保護內容是否允許特定動作的簡單資訊。</span><span class="sxs-lookup"><span data-stu-id="f8346-128">Describes how to get simple information about whether specific actions are allowed for protected content.</span></span> <span data-ttu-id="f8346-129">例如，應用程式可以播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="f8346-129">For example, can an application play a media file.</span></span>                    |
| [<span data-ttu-id="f8346-130">查詢詳細的許可權資訊</span><span class="sxs-lookup"><span data-stu-id="f8346-130">Querying for Detailed Rights Information</span></span>](querying-for-detailed-rights-information.md)               | <span data-ttu-id="f8346-131">描述如何使用金鑰識別碼，取得受保護內容的本機授權存放區中，所有授權所授與之許可權的詳細匯總資訊。</span><span class="sxs-lookup"><span data-stu-id="f8346-131">Describes how to get detailed aggregated information about the rights granted by all the licenses in the local license store for a piece of protected content using the key ID.</span></span> |
| [<span data-ttu-id="f8346-132">列舉本機授權存放區中的授權</span><span class="sxs-lookup"><span data-stu-id="f8346-132">Enumerating Licenses in the Local License Store</span></span>](enumerating-licenses-in-the-local-license-store.md) | <span data-ttu-id="f8346-133">說明如何從本機授權商店取得個別授權。</span><span class="sxs-lookup"><span data-stu-id="f8346-133">Describes how to get individual licenses from the local license store.</span></span>                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="f8346-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8346-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8346-135">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="f8346-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




