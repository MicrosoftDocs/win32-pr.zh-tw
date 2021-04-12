---
title: Windows Media DRM 用戶端擴充 Api
description: Windows Media DRM 用戶端擴充 Api
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
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
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375473"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="2d61d-116">Windows Media DRM 用戶端擴充 Api</span><span class="sxs-lookup"><span data-stu-id="2d61d-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="2d61d-117">\[Windows Media DRM 功能已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="2d61d-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="2d61d-118">請改用 [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) 。\]</span><span class="sxs-lookup"><span data-stu-id="2d61d-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="2d61d-119">本檔說明 Microsoft Windows Media 數位 Rights Management (DRM) 用戶端擴充應用程式開發介面 (Api) 。</span><span class="sxs-lookup"><span data-stu-id="2d61d-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="2d61d-120">Windows Media DRM 用戶端擴充 Api 包括可用來管理用戶端電腦上的 Windows Media 數位 Rights Management (DRM) 作業的物件。</span><span class="sxs-lookup"><span data-stu-id="2d61d-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="2d61d-121">這些 Api 的主要焦點在於管理受保護數位媒體內容的授權。</span><span class="sxs-lookup"><span data-stu-id="2d61d-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="2d61d-122">此外，您也可以使用 Api 來更新用戶端電腦上的 DRM 元件，並建立應用程式，以使用適用于網路裝置的 Windows Media DRM 來傳輸內容。</span><span class="sxs-lookup"><span data-stu-id="2d61d-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="2d61d-123">這些 Api 構成 Windows Media Rights Manager SDK 的用戶端對應項。</span><span class="sxs-lookup"><span data-stu-id="2d61d-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="2d61d-124">Windows Media Rights Manager 用來建立保護檔案和頒發用授權的線上服務，Windows Media DRM 用戶端擴充 Api 是用來建立使用該內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2d61d-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="2d61d-125">本檔包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="2d61d-125">This document includes the following sections.</span></span>



| <span data-ttu-id="2d61d-126">區段</span><span class="sxs-lookup"><span data-stu-id="2d61d-126">Section</span></span>                                                                                                  | <span data-ttu-id="2d61d-127">描述</span><span class="sxs-lookup"><span data-stu-id="2d61d-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d61d-128">關於 Windows Media DRM 用戶端擴充 Api</span><span class="sxs-lookup"><span data-stu-id="2d61d-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="2d61d-129">提供在開發使用 Api 的應用程式之前，您應該先熟悉的總覽和背景資訊。</span><span class="sxs-lookup"><span data-stu-id="2d61d-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="2d61d-130">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2d61d-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="2d61d-131">提供執行各種用戶端 DRM 作業的詳細指示。</span><span class="sxs-lookup"><span data-stu-id="2d61d-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="2d61d-132">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="2d61d-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="2d61d-133">提供有關 Windows Media DRM 用戶端擴充 Api 中所包含之介面、方法、函式、結構、列舉類型和常數的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="2d61d-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 