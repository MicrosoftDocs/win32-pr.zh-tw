---
title: DRM 匯入
description: DRM 匯入
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 匯入
- Windows Media Format SDK，匯入
- 'Windows Media Format SDK，content protection system (CPS) '
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- '數位版權管理 (DRM) 、內容保護系統 (CPS) '
- 'DRM (數位版權管理) 、內容保護系統 (CPS) '
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- 'DRM 用戶端擴充 Api、內容保護系統 (CPS) '
- '用戶端擴充 Api，content protection system (CPS) '
- " (CPS) 的內容保護系統"
- 'CPS (內容保護系統) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673619"
---
# <a name="drm-import"></a><span data-ttu-id="d4dbf-127">DRM 匯入</span><span class="sxs-lookup"><span data-stu-id="d4dbf-127">DRM Import</span></span>

<span data-ttu-id="d4dbf-128">下列各節說明如何將協力廠商內容保護系統 (CPS) 的媒體內容轉換成 Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="d4dbf-129">此程式稱為「DRM 匯入」，基本上是由下列步驟所組成：</span><span class="sxs-lookup"><span data-stu-id="d4dbf-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="d4dbf-130">建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="d4dbf-131">建立授權。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-131">Creating the license.</span></span>
3.  <span data-ttu-id="d4dbf-132">選擇性地刪除授權。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-132">Optionally deleting the license.</span></span>

<span data-ttu-id="d4dbf-133">下列各節將說明 DRM 匯入。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="d4dbf-134">區段</span><span class="sxs-lookup"><span data-stu-id="d4dbf-134">Section</span></span>                                                                              | <span data-ttu-id="d4dbf-135">描述</span><span class="sxs-lookup"><span data-stu-id="d4dbf-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4dbf-136">匯入授權和金鑰內容</span><span class="sxs-lookup"><span data-stu-id="d4dbf-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="d4dbf-137">描述如何在本機發出授權，並將其匯入 Windows Media DRM 中。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="d4dbf-138">檢查憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="d4dbf-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="d4dbf-139">說明如何檢查憑證撤銷。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="d4dbf-140">建立 XMR 授權</span><span class="sxs-lookup"><span data-stu-id="d4dbf-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="d4dbf-141">說明如何建立 XMR 授權，並將其傳遞至 DRM 子系統。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="d4dbf-142">建立和初始化 DRM 寫入器</span><span class="sxs-lookup"><span data-stu-id="d4dbf-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="d4dbf-143">說明如何初始化 ASF 寫入器物件，以準備進行 DRM 匯入。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="d4dbf-144">加密和匯入媒體範例</span><span class="sxs-lookup"><span data-stu-id="d4dbf-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="d4dbf-145">說明如何將個別媒體範例加密並匯入 Windows Media DRM 中。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="d4dbf-146">刪除授權</span><span class="sxs-lookup"><span data-stu-id="d4dbf-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="d4dbf-147">說明如何刪除本機建立的授權。</span><span class="sxs-lookup"><span data-stu-id="d4dbf-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="d4dbf-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4dbf-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4dbf-149">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="d4dbf-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




