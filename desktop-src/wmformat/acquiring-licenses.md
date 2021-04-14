---
title: 取得授權
description: 取得授權
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，取得授權
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) ，取得授權
- DRM (數位版權管理) ，取得授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api，取得授權
- 用戶端擴充 Api，取得授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371879"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="a26a3-122">取得授權</span><span class="sxs-lookup"><span data-stu-id="a26a3-122">Acquiring Licenses</span></span>

<span data-ttu-id="a26a3-123">取得授權的常見案例是當使用者擁有受保護的 Windows Media 檔案，且第一次嘗試存取內容時。</span><span class="sxs-lookup"><span data-stu-id="a26a3-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="a26a3-124">由於 Windows Media DRM 用戶端擴充 Api 與 ASF 檔案處理常式不同，因此在支援時，基本授權取得案例需要的 API 呼叫比使用 Windows Media 格式 SDK 和媒體基礎 SDK 更多。</span><span class="sxs-lookup"><span data-stu-id="a26a3-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="a26a3-125">本節說明如何使用 Windows Media DRM 用戶端擴充 Api 來取得在用戶端電腦上的本機授權存放區中儲存的授權。</span><span class="sxs-lookup"><span data-stu-id="a26a3-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="a26a3-126">其中包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="a26a3-126">It contains the following topics.</span></span>



| <span data-ttu-id="a26a3-127">主題</span><span class="sxs-lookup"><span data-stu-id="a26a3-127">Topic</span></span>                                                                | <span data-ttu-id="a26a3-128">描述</span><span class="sxs-lookup"><span data-stu-id="a26a3-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a26a3-129">無訊息授權取得</span><span class="sxs-lookup"><span data-stu-id="a26a3-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="a26a3-130">描述如何在不需要使用者介入的情況下取得授權。</span><span class="sxs-lookup"><span data-stu-id="a26a3-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="a26a3-131">取得非無訊息授權</span><span class="sxs-lookup"><span data-stu-id="a26a3-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="a26a3-132">描述如何在使用者介入 (（例如需要支付內容) ）時取得授權。</span><span class="sxs-lookup"><span data-stu-id="a26a3-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="a26a3-133">授權預先傳遞</span><span class="sxs-lookup"><span data-stu-id="a26a3-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="a26a3-134">說明如何從授權伺服器提取授權給用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="a26a3-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="a26a3-135">在本機建立授權</span><span class="sxs-lookup"><span data-stu-id="a26a3-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="a26a3-136">說明如何建立您自己的授權，而不需要從授權伺服器下載，以及如何將它們儲存在本機授權存放區中。</span><span class="sxs-lookup"><span data-stu-id="a26a3-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a26a3-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="a26a3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a26a3-138">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="a26a3-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




