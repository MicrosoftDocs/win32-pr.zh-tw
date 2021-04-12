---
title: DRM 保護和內容授權發佈
description: DRM 保護和內容授權發佈
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK，DRM 內容保護
- Windows Media Format SDK，DRM 授權
- Advanced Systems Format (ASF) ，DRM 內容保護
- ASF (Advanced Systems Format) ，DRM 內容保護
- Advanced Systems Format (ASF) ，DRM 授權發佈
- ASF (Advanced Systems Format) ，DRM 授權發佈
- 數位版權管理 (DRM) ，內容保護
- DRM (數位版權管理) 、內容保護
- 數位版權管理 (DRM) 、授權發佈
- DRM (數位版權管理) 、授權發佈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311451"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="0a160-113">DRM 保護和內容授權發佈</span><span class="sxs-lookup"><span data-stu-id="0a160-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="0a160-114">在建立端，數位版權管理技術牽涉到兩個主要的程式： (1) 保護內容和 (2) 提供內容的授權。</span><span class="sxs-lookup"><span data-stu-id="0a160-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="0a160-115">保護檔案基本上涉及加密內容，並在檔案標頭中包含 URL，以指定可能取得內容授權的位置。</span><span class="sxs-lookup"><span data-stu-id="0a160-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="0a160-116">如果您想要使用保護檔案，然後將檔案發佈到其他電腦或裝置，您可以使用 Windows Media Format SDK 或 Windows Media Rights Manager SDK 來保護檔案。</span><span class="sxs-lookup"><span data-stu-id="0a160-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="0a160-117">針對即時 DRM 案例，您必須使用 Windows Media Format SDK 來保護正在編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="0a160-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="0a160-118">若要建立併發行受保護內容的授權，您可以使用 Windows Media Rights Manager SDK 的物件來建立自己的自訂解決方案，也可以使用由協力廠商執行的服務。</span><span class="sxs-lookup"><span data-stu-id="0a160-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="0a160-119">無論您使用哪種方法，您所建立的受保護檔案都會包含在 DRM 標頭物件中，此 URL 會告知用戶端應用程式在何處取得內容的授權。</span><span class="sxs-lookup"><span data-stu-id="0a160-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="0a160-120">Windows Media Format SDK 不提供建立或發行授權的支援。</span><span class="sxs-lookup"><span data-stu-id="0a160-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="0a160-121">在播放端，啟用 DRM 的應用程式必須能夠取得受保護內容的授權、使用授權中所含的金鑰將該內容解密，以及強制執行授許可權制（例如檔案可能播放的次數），或是否可將檔案複製到其他裝置。</span><span class="sxs-lookup"><span data-stu-id="0a160-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="0a160-122">Windows Media Format SDK 提供建立完全啟用的 DRM 播放應用程式所需的所有支援。</span><span class="sxs-lookup"><span data-stu-id="0a160-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="0a160-123">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="0a160-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0a160-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a160-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a160-125">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="0a160-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="0a160-126">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="0a160-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




