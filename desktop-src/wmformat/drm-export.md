---
title: DRM 匯出
description: DRM 匯出
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 匯出
- Windows Media 格式 SDK，匯出
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) 、匯出
- DRM (數位版權管理) ，匯出
- DRM 用戶端擴充 Api，匯出
- 用戶端擴充 Api，匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301011"
---
# <a name="drm-export"></a><span data-ttu-id="53074-120">DRM 匯出</span><span class="sxs-lookup"><span data-stu-id="53074-120">DRM Export</span></span>

<span data-ttu-id="53074-121">Windows Media DRM 匯出功能可讓您建立授權的應用程式，以解密受 Windows Media DRM 保護的內容，並在 (CPS 的輸出內容保護設定中重新加密，) 由相關聯的授權簽發者明確指定。</span><span class="sxs-lookup"><span data-stu-id="53074-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="53074-122">授權簽發者會透過包含清單，明確地授權將內容匯出至特定 CPS。</span><span class="sxs-lookup"><span data-stu-id="53074-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="53074-123">若要存取匯出功能，您必須申請來自 Microsoft 的 [匯出應用程式憑證](export-application-certificate.md) 。</span><span class="sxs-lookup"><span data-stu-id="53074-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="53074-124">下列各節將說明 Windows Media DRM 匯出功能。</span><span class="sxs-lookup"><span data-stu-id="53074-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="53074-125">區段</span><span class="sxs-lookup"><span data-stu-id="53074-125">Section</span></span>                                                                                      | <span data-ttu-id="53074-126">描述</span><span class="sxs-lookup"><span data-stu-id="53074-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53074-127">匯出應用程式憑證</span><span class="sxs-lookup"><span data-stu-id="53074-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="53074-128">描述匯出應用程式憑證。</span><span class="sxs-lookup"><span data-stu-id="53074-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="53074-129">明確授權和包含清單</span><span class="sxs-lookup"><span data-stu-id="53074-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="53074-130">說明明確授權的程式，以及包含清單的運作方式。</span><span class="sxs-lookup"><span data-stu-id="53074-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="53074-131">匯出壓縮的內容</span><span class="sxs-lookup"><span data-stu-id="53074-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="53074-132">說明如何從 Windows Media DRM 受保護的音訊或影片內容匯出已壓縮的內容。</span><span class="sxs-lookup"><span data-stu-id="53074-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="53074-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="53074-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53074-134">**明確授權和包含清單**</span><span class="sxs-lookup"><span data-stu-id="53074-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="53074-135">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="53074-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




