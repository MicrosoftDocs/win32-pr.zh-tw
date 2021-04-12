---
title: Windows Media Format SDK 使用者簡介
description: Windows Media Format SDK 使用者簡介
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- DRM 用戶端擴充 Api，關於
- 用戶端擴充 Api，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372235"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="61163-116">Windows Media Format SDK 使用者簡介</span><span class="sxs-lookup"><span data-stu-id="61163-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="61163-117">Windows Media DRM 用戶端擴充 Api 所提供的許多功能，與 Windows Media 格式 SDK 的物件所提供的功能相同。</span><span class="sxs-lookup"><span data-stu-id="61163-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="61163-118">Windows Media Format SDK 為開發人員提供建立、存取和操作使用 Advanced Systems 格式的媒體檔案所需的物件 (ASF) 檔案結構。</span><span class="sxs-lookup"><span data-stu-id="61163-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="61163-119">因為 Windows Media DRM 是為了保護 ASF 檔案，所以用戶端 DRM 功能已包含在 Windows Media Format SDK 中。</span><span class="sxs-lookup"><span data-stu-id="61163-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="61163-120">Windows Media DRM 用戶端擴充 Api 與 Microsoft 的新一代數位媒體平臺（Microsoft 媒體基礎 SDK）一起發行。</span><span class="sxs-lookup"><span data-stu-id="61163-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="61163-121">媒體基礎將包含與 Windows Media Format SDK 的部分功能重迭的 ASF 功能。</span><span class="sxs-lookup"><span data-stu-id="61163-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="61163-122">因為現在有兩個可操作 ASF 檔案的 Microsoft Sdk，所以用戶端 DRM 功能會與 Windows media DRM 用戶端擴充 Api 分開。</span><span class="sxs-lookup"><span data-stu-id="61163-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="61163-123">這些 Api 可由 Windows Media 格式 SDK 和媒體基礎 SDK 的使用者存取。</span><span class="sxs-lookup"><span data-stu-id="61163-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="61163-124">目前，這些 Api 包含在 Windows Media Format SDK 安裝套件中，並記載為 Windows Media Format SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="61163-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="61163-125">不過，Windows Media DRM 用戶端擴充 Api 會在自己的程式庫中執行，並擁有自己的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="61163-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="61163-126">在安裝 Windows Media Format SDK 之後，您可以使用它們自己的 Api，而不需在應用程式中包含任何 Windows Media Format SDK 標頭或程式庫。</span><span class="sxs-lookup"><span data-stu-id="61163-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="61163-127">如果您開發使用 Windows Media 格式 SDK 的應用程式，您必須決定是否要使用 SDK 提供的 DRM 功能，或使用 Windows Media DRM 用戶端擴充 Api。</span><span class="sxs-lookup"><span data-stu-id="61163-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="61163-128">雖然這兩個 Sdk 的許多功能非常類似，但 Windows Media DRM 用戶端擴充 Api 提供下列功能，而這些功能不適用於舊版 DRM 常式的使用者：</span><span class="sxs-lookup"><span data-stu-id="61163-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="61163-129">能夠匯入協力廠商 rights management 系統所保護的內容。</span><span class="sxs-lookup"><span data-stu-id="61163-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="61163-130">將受 Windows Media DRM 保護的內容匯出至協力廠商版權管理系統的能力。</span><span class="sxs-lookup"><span data-stu-id="61163-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="61163-131">在授權存放中直接列舉授權。</span><span class="sxs-lookup"><span data-stu-id="61163-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="61163-132">以金鑰識別碼為基礎的簡單、匯總的許可權查詢 (不需要載入媒體檔案) 。</span><span class="sxs-lookup"><span data-stu-id="61163-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="61163-133">使用標準媒體基礎介面（ **IMFContentEnabler**）更新撤銷的元件的能力。</span><span class="sxs-lookup"><span data-stu-id="61163-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61163-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="61163-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61163-135">**關於 Windows Media DRM 用戶端擴充 Api**</span><span class="sxs-lookup"><span data-stu-id="61163-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




