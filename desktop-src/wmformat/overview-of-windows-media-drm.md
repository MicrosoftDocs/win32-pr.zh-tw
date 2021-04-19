---
title: Windows Media DRM 總覽
description: Windows Media DRM 總覽
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- 數位版權管理 (DRM) ，關於
- DRM (數位版權管理) ，關於
- 數位版權管理 (DRM) ，封裝 Windows Media 檔案
- DRM (數位版權管理) ，封裝 Windows Media 檔案
- 數位版權管理 (DRM) 、受保護的檔案授權
- DRM (數位版權管理) 、受保護的檔案授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) ，讀取受保護的檔案
- DRM (數位版權管理) ，讀取受保護的檔案
- 'Advanced Systems Format (ASF) 、數位版權管理 (DRM) '
- 'ASF (Advanced Systems Format) 、數位版權管理 (DRM) '
- 授權，DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106983281"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="850da-119">Windows Media DRM 總覽</span><span class="sxs-lookup"><span data-stu-id="850da-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="850da-120">Windows Media 數位 Rights Management (DRM) 是保護 Windows Media 檔案中的內容，讓未經授權的使用者無法存取的系統。</span><span class="sxs-lookup"><span data-stu-id="850da-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="850da-121">基本 DRM 週期有三個階段：封裝、授權和讀取。</span><span class="sxs-lookup"><span data-stu-id="850da-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="850da-122">封裝 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="850da-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="850da-123">Windows Media DRM 是設計用來處理 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="850da-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="850da-124">Windows Media 檔案是符合 Advanced Systems 格式的檔案 (ASF) 規格，而且只包含使用 Windows Media 音訊和影片編解碼器壓縮的音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="850da-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="850da-125">將 ASF 檔案封裝之後，會在標頭中加入 DRM 特定區段。</span><span class="sxs-lookup"><span data-stu-id="850da-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="850da-126">DRM 標頭包含金鑰識別碼，可識別授權用途的內容，以及取得授權取得 URL，這是網頁的位址，可發出授權以讀取受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="850da-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="850da-127">還有更多可放在 DRM 標頭中的資訊，但它是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="850da-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="850da-128">DRM 標頭已簽署，因此可以驗證封裝程式。</span><span class="sxs-lookup"><span data-stu-id="850da-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="850da-129">在封裝程式期間會加密 ASF 檔案中的內容。</span><span class="sxs-lookup"><span data-stu-id="850da-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="850da-130">但是，即使用戶端沒有授權，也可以使用封裝檔案中的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="850da-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="850da-131">儲存在 ASF 標頭中的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="850da-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="850da-132">某些儲存在 DRM 標頭中的中繼資料 (例如，您一律可以) 取得授權取得 URL。</span><span class="sxs-lookup"><span data-stu-id="850da-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="850da-133">授權受保護的檔案</span><span class="sxs-lookup"><span data-stu-id="850da-133">Licensing Protected Files</span></span>

<span data-ttu-id="850da-134">若要讀取封裝的檔案，必須將授權發行至用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="850da-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="850da-135">授權是一組資料，其描述可讀取受保護檔案中資料的條件。</span><span class="sxs-lookup"><span data-stu-id="850da-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="850da-136">最常見的情況是，針對受保護的檔案發出授權，以回應嘗試在檔案上執行某些作業的使用者。</span><span class="sxs-lookup"><span data-stu-id="850da-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="850da-137">不過，授權簽發者也可以在明確要求之前，將授權傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="850da-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="850da-138">如需授權的詳細資訊，請參閱 [授權](licenses.md)。</span><span class="sxs-lookup"><span data-stu-id="850da-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="850da-139">從受保護的檔案讀取資料</span><span class="sxs-lookup"><span data-stu-id="850da-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="850da-140">當使用者嘗試在受保護的檔案上執行作業時 (播放、燒錄至 CD、複製到裝置等) ，應用程式必須檢查用戶端電腦上的內容授權。</span><span class="sxs-lookup"><span data-stu-id="850da-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="850da-141">如果用戶端電腦上有有效的授權，則可以繼續執行此操作。</span><span class="sxs-lookup"><span data-stu-id="850da-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="850da-142">如果沒有內容的授權，或用戶端電腦上沒有內容的授權允許要求的動作，則必須取得授權。</span><span class="sxs-lookup"><span data-stu-id="850da-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="850da-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="850da-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="850da-144">**關於 Windows Media DRM 用戶端擴充 Api**</span><span class="sxs-lookup"><span data-stu-id="850da-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




