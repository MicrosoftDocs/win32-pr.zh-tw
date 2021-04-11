---
title: 處理受保護的內容
description: 處理受保護的內容
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media 裝置管理員，憑證
- 裝置管理員，憑證
- 桌面應用程式，憑證
- 服務提供者，憑證
- 程式設計指南，憑證
- certificates
- 'Windows Media 裝置管理員，安全內容提供者 (SCP) '
- '裝置管理員， (SCP 的安全內容提供者) '
- '桌面應用程式，安全內容提供者 (SCP) '
- '服務提供者、安全內容提供者 (SCP) '
- '程式設計指南，安全內容提供者 (SCP) '
- " (SCP) 的安全內容提供者"
- 'SCP (保護內容提供者) '
- Windows Media 裝置管理員、受 DRM 保護的內容
- 裝置管理員，受 DRM 保護的內容
- 程式設計指南，受 DRM 保護的內容
- 桌面應用程式，受 DRM 保護的內容
- 服務提供者，受 DRM 保護的內容
- 受 DRM 保護的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372049"
---
# <a name="handling-protected-content"></a><span data-ttu-id="c70bc-122">處理受保護的內容</span><span class="sxs-lookup"><span data-stu-id="c70bc-122">Handling Protected Content</span></span>

<span data-ttu-id="c70bc-123">如果您要建立的應用程式或服務提供者將取用 Windows Media 數位版權管理 (DRM) 所保護的內容，您必須有 Microsoft 所發行的金鑰/憑證組。</span><span class="sxs-lookup"><span data-stu-id="c70bc-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="c70bc-124">若要瞭解取得此憑證的位置，請參閱 [適用于開發的工具](tools-for-development.md)。</span><span class="sxs-lookup"><span data-stu-id="c70bc-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="c70bc-125">如果您不想要處理受保護的內容，您可以在名為 key. c 的檔案中使用此 SDK 提供的虛擬金鑰和憑證。</span><span class="sxs-lookup"><span data-stu-id="c70bc-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="c70bc-126">針對受 DRM 技術保護的任何檔案，Windows Media 裝置管理員需要有安全的內容提供者 (SCP) 適用于該檔案格式。</span><span class="sxs-lookup"><span data-stu-id="c70bc-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="c70bc-127">Microsoft 為 WMA 和 WMV 檔案提供 SCP 模組。</span><span class="sxs-lookup"><span data-stu-id="c70bc-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="c70bc-128">如果您的應用程式或服務提供者將處理另一種格式的受 DRM 保護的內容，您必須提供您自己的 SCP 模組。</span><span class="sxs-lookup"><span data-stu-id="c70bc-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="c70bc-129">SCP 模組是一種 COM 物件，可 [執行安全內容提供者](interfaces-for-secure-content-providers.md)的所有介面。</span><span class="sxs-lookup"><span data-stu-id="c70bc-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="c70bc-130">應用程式可以將受 DRM 保護的內容傳送至以 Windows Media DRM 10 （適用于可攜式裝置）為基礎的裝置，或可移植裝置 DRM (PDDRM) 。</span><span class="sxs-lookup"><span data-stu-id="c70bc-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="c70bc-131">不過，您只能為建立在 PDDRM 上的裝置建立服務提供者;您無法為可攜式裝置的 Windows Media DRM 10 上建立的裝置建立服務提供者。</span><span class="sxs-lookup"><span data-stu-id="c70bc-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="c70bc-132">這些後端裝置只能使用 Microsoft 提供的 MTP 服務提供者。</span><span class="sxs-lookup"><span data-stu-id="c70bc-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="c70bc-133">以 PDDRM 為基礎的裝置只能支援已購買內容的授權。</span><span class="sxs-lookup"><span data-stu-id="c70bc-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="c70bc-134">只有以 Windows Media DRM 10 為便攜裝置所建立的裝置，才支援具有期限到期條件的授權，而這些裝置具有特殊需求，例如安全的時鐘和個人化。</span><span class="sxs-lookup"><span data-stu-id="c70bc-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="c70bc-135">適用于可攜式裝置的 Windows Media DRM 10 SDK 提供支援版本10技術的裝置需求詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c70bc-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="c70bc-136">將 DRM 內容傳送到裝置之前，應用程式應該先驗證幾件事：</span><span class="sxs-lookup"><span data-stu-id="c70bc-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="c70bc-137">裝置支援 DRM 技術。</span><span class="sxs-lookup"><span data-stu-id="c70bc-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="c70bc-138">它支援 (10 版或更早版本) 的 DRM 技術版本。</span><span class="sxs-lookup"><span data-stu-id="c70bc-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="c70bc-139">如果裝置是以第10版為基礎，則其所有元件都是最新的 (例如，安全的時鐘和任何) 的個人化需求。</span><span class="sxs-lookup"><span data-stu-id="c70bc-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="c70bc-140">解決這些問題的所有方法呼叫都是由用戶端所建立，並由 Windows Media 裝置管理員和安全內容提供者元件所處理;服務提供者不會處理上述任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="c70bc-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="c70bc-141">如果裝置不支援適用于可攜式裝置的 Windows Media DRM 10，則根據內容授權和裝置設計) ，其可能仍能使用受保護的內容 (，但任何傳送給它的內容都將擁有有限許可權的簡化使用權 (例如，沒有時間到期) 。</span><span class="sxs-lookup"><span data-stu-id="c70bc-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="c70bc-142">如需示範應用程式如何確認裝置是否可以處理受保護的內容，以及是否需要更新其 DRM 元件的範例，請參閱在 [應用程式中處理受保護的內容](handling-protected-content-in-the-application.md)。</span><span class="sxs-lookup"><span data-stu-id="c70bc-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="c70bc-143">如需建立可處理受保護內容之服務提供者的詳細資訊，請參閱在 [服務提供者中處理受保護的內容](handling-protected-content-in-the-service-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="c70bc-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="c70bc-144">許多 Windows Media 裝置管理員檔案傳輸或要求方法的許可權) ，在處理已附加偵錯工具的受 DRM 保護的檔案時， (通常會失敗。</span><span class="sxs-lookup"><span data-stu-id="c70bc-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="c70bc-145">因此，您必須使用替代的方法來對程式碼進行偵錯工具，例如將輸出記錄到 Windows form 或記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c70bc-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="c70bc-146">如需記錄選項的詳細資訊，請參閱 [啟用記錄](enabling-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="c70bc-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="c70bc-147">如果您在受保護的內容上執行偵錯工具，方法將會傳回 DRM 區段 [錯誤碼](error-codes.md)中所列的其中一個錯誤碼，或可能是未知的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c70bc-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="c70bc-148">如果您在受保護的內容或方法上執行偵錯工具時，收到神秘的 **HRESULT** 值，DRM 保護可能是原因。</span><span class="sxs-lookup"><span data-stu-id="c70bc-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c70bc-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="c70bc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c70bc-150">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="c70bc-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




