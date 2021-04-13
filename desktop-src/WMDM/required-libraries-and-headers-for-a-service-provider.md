---
title: 服務提供者所需的程式庫和標頭
description: 服務提供者所需的程式庫和標頭
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Media 裝置管理員、程式庫
- 裝置管理員，程式庫
- 程式設計指南，程式庫
- 服務提供者，程式庫
- 建立服務提供者，程式庫
- 程式庫
- Windows Media 裝置管理員、標頭檔
- 裝置管理員，標頭檔
- 程式設計指南，標頭檔
- 服務提供者，標頭檔
- 建立服務提供者，標頭檔
- 標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301064"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a><span data-ttu-id="1caa1-115">服務提供者所需的程式庫和標頭</span><span class="sxs-lookup"><span data-stu-id="1caa1-115">Required Libraries and Headers for a Service Provider</span></span>

<span data-ttu-id="1caa1-116">本節會列出您必須包含的程式庫、標頭檔或 IDL 檔案，才能裝置管理員應用程式或外掛程式來開發 Windows Media。</span><span class="sxs-lookup"><span data-stu-id="1caa1-116">This section lists the libraries, header files or IDL files you will need to include to develop a Windows Media Device Manager application or plug-in.</span></span> <span data-ttu-id="1caa1-117">如同 [編譯 sdk 所提供的 idl](compiling-the-idl-files-supplied-with-the-sdk.md)檔案所述，SDK 包含 idl 檔案和預先建立的標頭檔，而您的應用程式可以使用其中一種。</span><span class="sxs-lookup"><span data-stu-id="1caa1-117">As mentioned in [Compiling the IDL Files Supplied with the SDK](compiling-the-idl-files-supplied-with-the-sdk.md), the SDK includes both IDL files and prebuilt header files, and your application can use either.</span></span> <span data-ttu-id="1caa1-118"> (請注意，某些標頭檔沒有對應的 IDL 檔案，而且您無法自行建立。 ) 如果建立您自己的 IDL 檔案，請在編譯隨附于 SDK 的 IDL 檔案中包含相依性。</span><span class="sxs-lookup"><span data-stu-id="1caa1-118">(Note that some header files do not have corresponding IDL files, and you cannot build them yourself.) If building your own IDL files, include the dependencies listed in Compiling the IDL Files Supplied with the SDK.</span></span>

<span data-ttu-id="1caa1-119">並非所有應用程式都需要所有檔案;閱讀描述以瞭解您的應用程式是否需要檔案。</span><span class="sxs-lookup"><span data-stu-id="1caa1-119">Not all applications will require all files; read the description to learn if your application requires a file.</span></span>



| <span data-ttu-id="1caa1-120">預建的標頭或程式庫</span><span class="sxs-lookup"><span data-stu-id="1caa1-120">Prebuilt header or library</span></span>       | <span data-ttu-id="1caa1-121">相等的 IDL</span><span class="sxs-lookup"><span data-stu-id="1caa1-121">Equivalent IDL</span></span>                                                                | <span data-ttu-id="1caa1-122">Description</span><span class="sxs-lookup"><span data-stu-id="1caa1-122">Description</span></span>                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1caa1-123">mssachlp .lib</span><span class="sxs-lookup"><span data-stu-id="1caa1-123">mssachlp.lib</span></span>                     | <span data-ttu-id="1caa1-124">無</span><span class="sxs-lookup"><span data-stu-id="1caa1-124">none</span></span>                                                                          | <span data-ttu-id="1caa1-125">所有服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-125">Required by all service providers.</span></span> <span data-ttu-id="1caa1-126">定義 Windows Media 裝置管理員物件。</span><span class="sxs-lookup"><span data-stu-id="1caa1-126">Defines Windows Media Device Manager objects.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="1caa1-127">initguid。h</span><span class="sxs-lookup"><span data-stu-id="1caa1-127">initguid.h</span></span>                       | <span data-ttu-id="1caa1-128">無 (Platform SDK 標頭) </span><span class="sxs-lookup"><span data-stu-id="1caa1-128">none (Platform SDK header)</span></span>                                                    | <span data-ttu-id="1caa1-129">所有服務提供者都需要使用預建的 Mswmdm .h 檔案定義 **GUID** 值。</span><span class="sxs-lookup"><span data-stu-id="1caa1-129">Required by all service providers to define the **GUID** values using the prebuilt Mswmdm.h file.</span></span> <span data-ttu-id="1caa1-130">您必須在專案中只包含 initguid 一次。</span><span class="sxs-lookup"><span data-stu-id="1caa1-130">You must include initguid.h once and only once in your project.</span></span> <span data-ttu-id="1caa1-131">此標頭會重新定義 **定義 \_ guid** 宏，以避免外部 **GUID** 命名問題。</span><span class="sxs-lookup"><span data-stu-id="1caa1-131">This header redefines the **DEFINE\_GUID** macro to avoid external **GUID** naming problems.</span></span> |
| <span data-ttu-id="1caa1-132">mswmdm。h</span><span class="sxs-lookup"><span data-stu-id="1caa1-132">mswmdm.h</span></span>                         | <span data-ttu-id="1caa1-133">WMDM .idl</span><span class="sxs-lookup"><span data-stu-id="1caa1-133">WMDM.idl</span></span><br/> <span data-ttu-id="1caa1-134">WMSP .idl</span><span class="sxs-lookup"><span data-stu-id="1caa1-134">WMSP.idl</span></span><br/> <span data-ttu-id="1caa1-135">icomponentauthenticate .idl</span><span class="sxs-lookup"><span data-stu-id="1caa1-135">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="1caa1-136">所有服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-136">Required by all service providers.</span></span> <span data-ttu-id="1caa1-137">定義所有服務提供者介面、結構、中繼資料、錯誤碼和其他常數。</span><span class="sxs-lookup"><span data-stu-id="1caa1-137">Defines all the service provider interfaces, structures, metadata, error codes, and other constants.</span></span>                                                                                                                        |
| <span data-ttu-id="1caa1-138">sac. h</span><span class="sxs-lookup"><span data-stu-id="1caa1-138">sac.h</span></span>                            | <span data-ttu-id="1caa1-139">無</span><span class="sxs-lookup"><span data-stu-id="1caa1-139">none</span></span>                                                                          | <span data-ttu-id="1caa1-140">所有服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-140">Required by all service providers.</span></span> <span data-ttu-id="1caa1-141">定義 SAC 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1caa1-141">Defines SAC protocols.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="1caa1-142">scserver。h</span><span class="sxs-lookup"><span data-stu-id="1caa1-142">scserver.h</span></span>                       | <span data-ttu-id="1caa1-143">無</span><span class="sxs-lookup"><span data-stu-id="1caa1-143">none</span></span>                                                                          | <span data-ttu-id="1caa1-144">所有服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-144">Required by all service providers.</span></span> <span data-ttu-id="1caa1-145">宣告 [CSecureChannelServer](csecurechannelserver-class.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="1caa1-145">Declares the [CSecureChannelServer](csecurechannelserver-class.md) class.</span></span>                                                                                                                                                  |
| <span data-ttu-id="1caa1-146">wmdmlog. hwmdmlog \_ c。</span><span class="sxs-lookup"><span data-stu-id="1caa1-146">wmdmlog.hwmdmlog\_i.c</span></span><br/> | <span data-ttu-id="1caa1-147">Wmdmlog .idl</span><span class="sxs-lookup"><span data-stu-id="1caa1-147">Wmdmlog.idl</span></span>                                                                   | <span data-ttu-id="1caa1-148">使用 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) 介面的服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-148">Required by service providers that use the [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) interface.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="1caa1-149">wmsdk。h</span><span class="sxs-lookup"><span data-stu-id="1caa1-149">wmsdk.h</span></span>                          | <span data-ttu-id="1caa1-150">無 (Windows Media Format SDK 提供) </span><span class="sxs-lookup"><span data-stu-id="1caa1-150">none (provided by Windows Media Format SDK)</span></span>                                   | <span data-ttu-id="1caa1-151">使用 Windows Media 格式 SDK 方法的服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-151">Required for service providers that use Windows Media Format SDK methods.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="1caa1-152">wmvcore .lib</span><span class="sxs-lookup"><span data-stu-id="1caa1-152">wmvcore.lib</span></span>                      | <span data-ttu-id="1caa1-153">無</span><span class="sxs-lookup"><span data-stu-id="1caa1-153">none</span></span>                                                                          | <span data-ttu-id="1caa1-154">使用 Windows Media 格式 SDK 物件或函式的服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-154">Required by service providers that use Windows Media Format SDK objects or functions.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="1caa1-155">mmreg。h</span><span class="sxs-lookup"><span data-stu-id="1caa1-155">mmreg.h</span></span>                          | <span data-ttu-id="1caa1-156">無 (Platform SDK 標頭) </span><span class="sxs-lookup"><span data-stu-id="1caa1-156">none (Platform SDK header)</span></span>                                                    | <span data-ttu-id="1caa1-157">參考各種標準 Windows Media 格式定義的服務提供者（例如 **WAVEFORMATEX**）所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-157">Required by service providers that reference various standard Windows Media format definitions, such as **WAVEFORMATEX**.</span></span>                                                                                                                                      |
| <span data-ttu-id="1caa1-158">MtpExt。h</span><span class="sxs-lookup"><span data-stu-id="1caa1-158">MtpExt.h</span></span>                         | <span data-ttu-id="1caa1-159">無</span><span class="sxs-lookup"><span data-stu-id="1caa1-159">none</span></span>                                                                          | <span data-ttu-id="1caa1-160">在 MTP 裝置上處理 [**IMDSPDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) 的服務提供者所需。</span><span class="sxs-lookup"><span data-stu-id="1caa1-160">Required for service providers that handle [**IMDSPDevice3::DeviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) on MTP devices.</span></span> <span data-ttu-id="1caa1-161">定義各種標準 MTP 常數和結構。</span><span class="sxs-lookup"><span data-stu-id="1caa1-161">Defines various standard MTP constants and structures.</span></span>                                                                        |
| <span data-ttu-id="1caa1-162">C。</span><span class="sxs-lookup"><span data-stu-id="1caa1-162">Key.c</span></span>                            | <span data-ttu-id="1caa1-163">無</span><span class="sxs-lookup"><span data-stu-id="1caa1-163">none</span></span>                                                                          | <span data-ttu-id="1caa1-164">定義來自 Microsoft 的金鑰和憑證。</span><span class="sxs-lookup"><span data-stu-id="1caa1-164">Defines a key and certificate from Microsoft.</span></span> <span data-ttu-id="1caa1-165">SDK 隨附的版本包含測試虛擬機器碼，可讓您使用非 DRM 保護的 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="1caa1-165">The version shipped with the SDK includes a test dummy key that will allow the use of non-DRM protected Windows Media files.</span></span>                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="1caa1-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="1caa1-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1caa1-167">**建立服務提供者**</span><span class="sxs-lookup"><span data-stu-id="1caa1-167">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 





