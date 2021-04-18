---
title: 安全內容提供者的介面
description: 安全內容提供者的介面
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media 裝置管理員、受 DRM 保護的內容
- 裝置管理員，受 DRM 保護的內容
- 程式設計參考，受 DRM 保護的內容
- Windows Media 裝置管理員的參考，受 DRM 保護的內容
- 受 DRM 保護的內容
- 'Windows Media 裝置管理員，安全內容提供者 (SCP) '
- '裝置管理員， (SCP 的安全內容提供者) '
- '程式設計參考，安全內容提供者 (SCP) '
- 'Windows Media 裝置管理員的參考、安全的內容提供者 (SCP) '
- " (SCP) 的安全內容提供者"
- 'SCP (保護內容提供者) '
- Windows Media 裝置管理員、SCP 介面
- 裝置管理員，SCP 介面
- 程式設計參考，SCP 介面
- Windows Media 裝置管理員、SCP 介面的參考
- SCP 介面，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965177"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="cd4e1-119">安全內容提供者的介面</span><span class="sxs-lookup"><span data-stu-id="cd4e1-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="cd4e1-120">安全內容提供者 (SCP) 是一個外掛程式元件，可讓 Windows Media 裝置管理員從受 DRM 保護的內容傳送和要求許可權資訊。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="cd4e1-121">Microsoft 提供的 SCP 元件可以處理受 DRM 保護的 WMA 和 WMV 檔案。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="cd4e1-122">如果您的裝置或應用程式將使用其他格式的受 DRM 保護內容，它應該藉由執行所有這些介面來建立 SCP 元件。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="cd4e1-123">否則，您將不需要使用這些介面。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="cd4e1-124">介面</span><span class="sxs-lookup"><span data-stu-id="cd4e1-124">Interface</span></span>                                                  | <span data-ttu-id="cd4e1-125">描述</span><span class="sxs-lookup"><span data-stu-id="cd4e1-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd4e1-126">**ISCPSecureAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="cd4e1-127">安全內容提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="cd4e1-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="cd4e1-129">藉由提供取得會話物件的方法來擴充 **ISCPSecureAuthenticate** 。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="cd4e1-130">**ISCPSecureExchange**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="cd4e1-131">用來交換與內容相關聯的受保護內容和許可權。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="cd4e1-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="cd4e1-133">藉由提供新版本的 **TransferContainerData** 方法來擴充 **ISCPSecureExchange** 。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="cd4e1-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="cd4e1-135">藉由提供改良的資料交換效能以及傳送完成的回呼方法，來擴充 **ISCPSecureExchange2** 。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="cd4e1-136">**ISCPSecureQuery**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="cd4e1-137">由 Windows Media 裝置管理員查詢，以決定受保護內容的擁有權。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="cd4e1-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="cd4e1-139">透過可判斷安全內容提供者是否負責內容的功能來擴充 **ISCPSecureQuery** ，如果是的話，請提供 URL 來更新撤銷的元件，並判斷哪些元件已被撤銷。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="cd4e1-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="cd4e1-141">擴充 **ISCPSecureQuery2** ，方法是提供一組新方法來取得明確通道的許可權並進行決策。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="cd4e1-142">**ISCPSession**</span><span class="sxs-lookup"><span data-stu-id="cd4e1-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="cd4e1-143">為多項作業提供有效率的一般狀態管理。</span><span class="sxs-lookup"><span data-stu-id="cd4e1-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 




