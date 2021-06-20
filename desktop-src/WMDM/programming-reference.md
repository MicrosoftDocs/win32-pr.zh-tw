---
title: WMDM 參考
description: Windows Media 裝置管理員 SDK 是由介面、結構、列舉和常數的集合所組成。 使用這些參考文章。
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media 裝置管理員，程式設計參考
- 裝置管理員，程式設計參考
- Windows Media 裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- Windows Media 裝置管理員、服務提供者
- 裝置管理員，服務提供者
- 桌面應用程式，程式設計參考
- 服務提供者，程式設計參考
- 程式設計參考，桌面應用程式
- 服務提供者的程式設計參考
- Windows Media 裝置管理員程式設計參考
- Windows Media 裝置管理員的參考，關於
- Windows Media 裝置管理員的參考，桌面應用程式
- Windows Media 裝置管理員、服務提供者的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e624bbc445d5d5e376cad926248ae4ee4db17a6e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406521"
---
# <a name="wmdm-reference"></a><span data-ttu-id="b8fc6-118">WMDM 參考</span><span class="sxs-lookup"><span data-stu-id="b8fc6-118">WMDM reference</span></span>

<span data-ttu-id="b8fc6-119">Windows Media 裝置管理員 SDK 是由介面、結構、列舉和常數的集合所組成。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-119">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="b8fc6-120">參考區段會根據使用這些介面的物件類型，將它們分割成群組。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-120">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="b8fc6-121">區段</span><span class="sxs-lookup"><span data-stu-id="b8fc6-121">Section</span></span>                                                                                                    | <span data-ttu-id="b8fc6-122">描述</span><span class="sxs-lookup"><span data-stu-id="b8fc6-122">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8fc6-123">應用程式的介面</span><span class="sxs-lookup"><span data-stu-id="b8fc6-123">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="b8fc6-124">描述僅供桌面應用程式、Windows Media Player 外掛程式或需要高階可攜式裝置存取的 COM 物件使用或執行的介面。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-124">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="b8fc6-125">服務提供者的介面</span><span class="sxs-lookup"><span data-stu-id="b8fc6-125">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="b8fc6-126">描述只由服務提供者使用或執行的介面，此介面會處理與可攜式裝置的實際低層級通訊。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-126">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="b8fc6-127">Windows Media DRM-Implemented 介面</span><span class="sxs-lookup"><span data-stu-id="b8fc6-127">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="b8fc6-128">描述不打算由協力廠商服務提供者執行的介面，而是由 Windows Media DRM 和 Windows Media 裝置管理員在內部執行和呼叫的介面。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-128">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="b8fc6-129">服務提供者和應用程式的介面</span><span class="sxs-lookup"><span data-stu-id="b8fc6-129">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="b8fc6-130">描述應用程式或服務提供者可以使用的介面。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-130">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="b8fc6-131">安全內容提供者的介面</span><span class="sxs-lookup"><span data-stu-id="b8fc6-131">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="b8fc6-132">描述必須由裝置或應用程式所執行的介面，該裝置或應用程式將會使用受 DRM 保護的內容。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-132">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="b8fc6-133">結構</span><span class="sxs-lookup"><span data-stu-id="b8fc6-133">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="b8fc6-134">描述用於 Windows Media 裝置管理員方法的結構。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-134">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="b8fc6-135">列舉類型</span><span class="sxs-lookup"><span data-stu-id="b8fc6-135">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="b8fc6-136">描述用於 Windows Media 裝置管理員方法的列舉。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-136">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="b8fc6-137">中繼資料常數</span><span class="sxs-lookup"><span data-stu-id="b8fc6-137">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="b8fc6-138">描述 Windows Media 裝置管理員 SDK 所定義的常數，以針對裝置或裝置上的裝置或物件來設定或抓取不同的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-138">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="b8fc6-139">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b8fc6-139">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="b8fc6-140">描述 Windows Media 裝置管理員 SDK 方法可傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b8fc6-140">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




