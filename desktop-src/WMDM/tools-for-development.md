---
title: 適用于開發的工具
description: 適用于開發的工具
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media 裝置管理員，開發工具
- 裝置管理員，開發工具
- Windows Media 裝置管理員，憑證
- 裝置管理員，憑證
- Windows Media 裝置管理員，金鑰
- 裝置管理員，金鑰
- Windows Media 裝置管理員、程式庫
- 裝置管理員，程式庫
- 'Windows Media 裝置管理員，軟體發展工具組 (SDK) '
- '裝置管理員，軟體發展工具組 (SDK) '
- Windows Media 裝置管理員 SDK
- 裝置管理員 SDK
- Windows Media Player SDK
- Windows Media Format SDK
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106967503"
---
# <a name="tools-for-development"></a><span data-ttu-id="37cef-118">適用于開發的工具</span><span class="sxs-lookup"><span data-stu-id="37cef-118">Tools for Development</span></span>

<span data-ttu-id="37cef-119">本節說明使用 Windows Media 裝置管理員 SDK 進行程式設計所需的各種憑證和金鑰、程式庫和 Sdk。</span><span class="sxs-lookup"><span data-stu-id="37cef-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="37cef-120">憑證和金鑰</span><span class="sxs-lookup"><span data-stu-id="37cef-120">Certificates and Keys</span></span>

<span data-ttu-id="37cef-121">Windows Media 裝置管理員 SDK 隨附的「測試金鑰/憑證」組 (在可讓應用程式或服務提供者在未受保護的內容上使用 Windows Media 裝置管理員方法的「金鑰」/「憑證」) 。</span><span class="sxs-lookup"><span data-stu-id="37cef-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="37cef-122">此金鑰/憑證組可讓應用程式或服務提供者使用大部分的 Windows Media 裝置管理員功能。</span><span class="sxs-lookup"><span data-stu-id="37cef-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="37cef-123">不過，若要開發可處理受 DRM 保護內容的應用程式或服務提供者，您必須使用 [Windows Media 授權頁面](https://www.microsoft.com/licensing/default)中的金鑰) ，要求一或多個憑證 (。</span><span class="sxs-lookup"><span data-stu-id="37cef-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="37cef-124">下列應用程式或物件需要憑證：</span><span class="sxs-lookup"><span data-stu-id="37cef-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="37cef-125">處理受 DRM 保護內容的服務提供者需要 Windows Media 裝置管理員 Service Provider 憑證 (和金鑰) </span><span class="sxs-lookup"><span data-stu-id="37cef-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="37cef-126">傳送受 DRM 保護內容的應用程式需要 Windows Media 裝置管理員傳輸憑證 (和金鑰) </span><span class="sxs-lookup"><span data-stu-id="37cef-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="37cef-127">播放受 DRM 保護內容的應用程式需要 DRM 憑證 (和金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="37cef-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="37cef-128">授權計量元件需要計量憑證。</span><span class="sxs-lookup"><span data-stu-id="37cef-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="37cef-129">這是由 Windows Media Rights Manager SDK 上建的授權計量服務所提供，可以在 Windows Media 授權頁面上要求。</span><span class="sxs-lookup"><span data-stu-id="37cef-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="37cef-130">程式庫和標頭</span><span class="sxs-lookup"><span data-stu-id="37cef-130">Libraries and Headers</span></span>

<span data-ttu-id="37cef-131">除了 [應用程式所需](required-library-and-header-files-for-an-application.md) 的程式庫和標頭檔中所述的程式庫和標頭，或是 [服務提供者所需](required-libraries-and-headers-for-a-service-provider.md)的程式庫和標頭之外，先前連結至 WMDRMSDK 的任何應用程式或外掛程式，都應該改為連結到 WMDRMSDKStub .lib。</span><span class="sxs-lookup"><span data-stu-id="37cef-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="37cef-132">此程式庫檔案是用來存取受 DRM 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="37cef-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="37cef-133">您也可以從 Windows Media 授權頁面要求此程式庫。</span><span class="sxs-lookup"><span data-stu-id="37cef-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="37cef-134">相關 Sdk</span><span class="sxs-lookup"><span data-stu-id="37cef-134">Related SDKs</span></span>

<span data-ttu-id="37cef-135">下列 Microsoft Sdk 提供您在設計便攜媒體裝置的解決方案時可能需要的元素。</span><span class="sxs-lookup"><span data-stu-id="37cef-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="37cef-136">需要 SDK</span><span class="sxs-lookup"><span data-stu-id="37cef-136">SDK Required</span></span>                     | <span data-ttu-id="37cef-137">必要的 .。。</span><span class="sxs-lookup"><span data-stu-id="37cef-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cef-138">Windows Media 裝置管理員 SDK</span><span class="sxs-lookup"><span data-stu-id="37cef-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="37cef-139">與可攜式裝置通訊的桌面媒體播放機應用程式</span><span class="sxs-lookup"><span data-stu-id="37cef-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="37cef-140">可以與可攜式裝置交換檔案或資訊的桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="37cef-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="37cef-141">Windows Media Player 計量 COM 物件</span><span class="sxs-lookup"><span data-stu-id="37cef-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="37cef-142">Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="37cef-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="37cef-143">Windows Media Player 外掛程式</span><span class="sxs-lookup"><span data-stu-id="37cef-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="37cef-144">Windows Media Player 計量 COM 物件</span><span class="sxs-lookup"><span data-stu-id="37cef-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="37cef-145">Windows Media Player 的外觀</span><span class="sxs-lookup"><span data-stu-id="37cef-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="37cef-146">Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="37cef-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="37cef-147">可以建立或播放檔案 (特別是 ASF 檔案的音訊或影片播放程式) </span><span class="sxs-lookup"><span data-stu-id="37cef-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="37cef-148">音訊或影片編輯應用程式</span><span class="sxs-lookup"><span data-stu-id="37cef-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="37cef-149">Windows Media Rights Manager SDK</span><span class="sxs-lookup"><span data-stu-id="37cef-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="37cef-150">在桌面或裝置上計量播放次數的應用程式或外掛程式。</span><span class="sxs-lookup"><span data-stu-id="37cef-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="37cef-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="37cef-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37cef-152">**開始使用**</span><span class="sxs-lookup"><span data-stu-id="37cef-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 





