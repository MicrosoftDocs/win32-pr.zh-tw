---
title: 應用程式所需的程式庫和標頭檔
description: 應用程式所需的程式庫和標頭檔
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Media 裝置管理員、程式庫
- 裝置管理員，程式庫
- 程式設計指南，程式庫
- 桌面應用程式，程式庫
- 建立 Windows Media 裝置管理員應用程式、程式庫
- 程式庫
- Windows Media 裝置管理員、標頭檔
- 裝置管理員，標頭檔
- 程式設計指南，標頭檔
- 桌面應用程式，標頭檔
- 建立 Windows Media 裝置管理員應用程式，標頭檔
- 標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021577"
---
# <a name="required-library-and-header-files-for-an-application"></a><span data-ttu-id="41472-115">應用程式所需的程式庫和標頭檔</span><span class="sxs-lookup"><span data-stu-id="41472-115">Required Library and Header Files for an Application</span></span>

<span data-ttu-id="41472-116">本節會列出您必須包含的程式庫、標頭檔或 IDL 檔案，才能裝置管理員應用程式或外掛程式來開發 Windows Media。</span><span class="sxs-lookup"><span data-stu-id="41472-116">This section lists the libraries, header files or IDL files you will need to include to develop a Windows Media Device Manager application or plug-in.</span></span> <span data-ttu-id="41472-117">如同 [編譯 sdk 所提供的 idl](compiling-the-idl-files-supplied-with-the-sdk.md)檔案所述，SDK 包含 idl 檔案和預先建立的標頭檔，而您的應用程式可以使用其中一種。</span><span class="sxs-lookup"><span data-stu-id="41472-117">As mentioned in [Compiling the IDL Files Supplied with the SDK](compiling-the-idl-files-supplied-with-the-sdk.md), the SDK includes both IDL files and prebuilt header files, and your application can use either.</span></span> <span data-ttu-id="41472-118"> (請注意，某些標頭檔沒有對應的 IDL 檔案，而且您無法自行建立。 ) 如果建立您自己的 IDL 檔案，請在編譯隨附于 SDK 的 IDL 檔案中包含相依性。</span><span class="sxs-lookup"><span data-stu-id="41472-118">(Note that some header files do not have corresponding IDL files, and you cannot build them yourself.) If building your own IDL files, include the dependencies listed in Compiling the IDL Files Supplied with the SDK.</span></span>

<span data-ttu-id="41472-119">並非所有應用程式都需要所有檔案;閱讀描述以瞭解您的應用程式是否需要檔案。</span><span class="sxs-lookup"><span data-stu-id="41472-119">Not all applications will require all files; read the description to learn whether your application requires a file.</span></span>



| <span data-ttu-id="41472-120">預建的標頭或程式庫</span><span class="sxs-lookup"><span data-stu-id="41472-120">Prebuilt header or library</span></span>       | <span data-ttu-id="41472-121">相等的 IDL</span><span class="sxs-lookup"><span data-stu-id="41472-121">Equivalent IDL</span></span>                                | <span data-ttu-id="41472-122">Description</span><span class="sxs-lookup"><span data-stu-id="41472-122">Description</span></span>                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41472-123">mssachlp .lib</span><span class="sxs-lookup"><span data-stu-id="41472-123">mssachlp.lib</span></span>                     | <span data-ttu-id="41472-124">無</span><span class="sxs-lookup"><span data-stu-id="41472-124">none</span></span>                                          | <span data-ttu-id="41472-125">所有應用程式都需要。</span><span class="sxs-lookup"><span data-stu-id="41472-125">Required by all applications.</span></span> <span data-ttu-id="41472-126">包含 Windows Media 裝置管理員物件。</span><span class="sxs-lookup"><span data-stu-id="41472-126">Contains Windows Media Device Manager objects.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="41472-127">wmvcore .lib</span><span class="sxs-lookup"><span data-stu-id="41472-127">wmvcore.lib</span></span>                      | <span data-ttu-id="41472-128">無</span><span class="sxs-lookup"><span data-stu-id="41472-128">none</span></span>                                          | <span data-ttu-id="41472-129">使用 Windows Media 格式 SDK 物件或函式的應用程式所需。</span><span class="sxs-lookup"><span data-stu-id="41472-129">Required by applications that use Windows Media Format SDK objects or functions.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="41472-130">initguid。h</span><span class="sxs-lookup"><span data-stu-id="41472-130">initguid.h</span></span>                       | <span data-ttu-id="41472-131">無 (Platform SDK 標頭) </span><span class="sxs-lookup"><span data-stu-id="41472-131">none (Platform SDK header)</span></span>                    | <span data-ttu-id="41472-132">所有應用程式都需要使用預建的 Mswmdm .h 檔案定義 **GUID** 值。</span><span class="sxs-lookup"><span data-stu-id="41472-132">Required by all applications to define the **GUID** values using the prebuilt Mswmdm.h file.</span></span> <span data-ttu-id="41472-133">您必須在專案中只包含 initguid 一次。</span><span class="sxs-lookup"><span data-stu-id="41472-133">You must include initguid.h once and only once in your project.</span></span> <span data-ttu-id="41472-134">此標頭會重新定義 **定義 \_ guid** 宏，以避免外部 **GUID** 命名問題。</span><span class="sxs-lookup"><span data-stu-id="41472-134">This header redefines the **DEFINE\_GUID** macro to avoid external **GUID** naming problems.</span></span> |
| <span data-ttu-id="41472-135">mmreg。h</span><span class="sxs-lookup"><span data-stu-id="41472-135">mmreg.h</span></span>                          | <span data-ttu-id="41472-136">無 (Platform SDK 標頭) </span><span class="sxs-lookup"><span data-stu-id="41472-136">none (Platform SDK header)</span></span>                    | <span data-ttu-id="41472-137">參考各種標準 Windows Media 格式定義的應用程式（例如 **WAVEFORMATEX**）所需。</span><span class="sxs-lookup"><span data-stu-id="41472-137">Required by applications that reference various standard Windows Media format definitions, such as **WAVEFORMATEX**.</span></span>                                                                                                                                      |
| <span data-ttu-id="41472-138">mswmdm。h</span><span class="sxs-lookup"><span data-stu-id="41472-138">mswmdm.h</span></span>                         | <span data-ttu-id="41472-139">WMDM. idlicomponentauthenticate .idl</span><span class="sxs-lookup"><span data-stu-id="41472-139">WMDM.idlicomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="41472-140">所有應用程式都需要。</span><span class="sxs-lookup"><span data-stu-id="41472-140">Required by all applications.</span></span> <span data-ttu-id="41472-141">定義所有的應用程式介面，以及結構、中繼資料、錯誤和其他常數。</span><span class="sxs-lookup"><span data-stu-id="41472-141">Defines all the application interfaces, as well as structures, metadata, error, and other constants.</span></span>                                                                                                                        |
| <span data-ttu-id="41472-142">sac. h</span><span class="sxs-lookup"><span data-stu-id="41472-142">sac.h</span></span>                            | <span data-ttu-id="41472-143">無</span><span class="sxs-lookup"><span data-stu-id="41472-143">none</span></span>                                          | <span data-ttu-id="41472-144">所有應用程式都需要。</span><span class="sxs-lookup"><span data-stu-id="41472-144">Required by all applications.</span></span> <span data-ttu-id="41472-145">定義 SAC 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="41472-145">Defines SAC protocols.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="41472-146">scclient。h</span><span class="sxs-lookup"><span data-stu-id="41472-146">scclient.h</span></span>                       | <span data-ttu-id="41472-147">無</span><span class="sxs-lookup"><span data-stu-id="41472-147">none</span></span>                                          | <span data-ttu-id="41472-148">所有應用程式都需要。</span><span class="sxs-lookup"><span data-stu-id="41472-148">Required by all applications.</span></span> <span data-ttu-id="41472-149">宣告 [CSecureChannelClient](csecurechannelclient-class.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="41472-149">Declares the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span>                                                                                                                                                  |
| <span data-ttu-id="41472-150">wmdmlog. hwmdmlog \_ c。</span><span class="sxs-lookup"><span data-stu-id="41472-150">wmdmlog.hwmdmlog\_i.c</span></span><br/> | <span data-ttu-id="41472-151">Wmdmlog .idl</span><span class="sxs-lookup"><span data-stu-id="41472-151">Wmdmlog.idl</span></span>                                   | <span data-ttu-id="41472-152">使用 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) 介面的應用程式所需。</span><span class="sxs-lookup"><span data-stu-id="41472-152">Required by applications that use the [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) interface.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="41472-153">wmdrmdeviceapp。h</span><span class="sxs-lookup"><span data-stu-id="41472-153">wmdrmdeviceapp.h</span></span>                 | <span data-ttu-id="41472-154">WMDRMDeviceApp .idl</span><span class="sxs-lookup"><span data-stu-id="41472-154">WMDRMDeviceApp.idl</span></span>                            | <span data-ttu-id="41472-155">在裝置上更新 DRM 元件或計量播放次數的應用程式或外掛程式的必要項。</span><span class="sxs-lookup"><span data-stu-id="41472-155">Required by applications or plug-ins that update DRM components or meter play counts on devices.</span></span>                                                                                                                                                          |
| <span data-ttu-id="41472-156">wmsdk。h</span><span class="sxs-lookup"><span data-stu-id="41472-156">wmsdk.h</span></span>                          | <span data-ttu-id="41472-157">無 (Windows Media Format SDK 提供) </span><span class="sxs-lookup"><span data-stu-id="41472-157">none (provided by Windows Media Format SDK)</span></span>   | <span data-ttu-id="41472-158">使用 Windows Media 格式 SDK 方法的應用程式所需。</span><span class="sxs-lookup"><span data-stu-id="41472-158">Required for applications that use Windows Media Format SDK methods.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="41472-159">MtpExt。h</span><span class="sxs-lookup"><span data-stu-id="41472-159">MtpExt.h</span></span>                         | <span data-ttu-id="41472-160">無</span><span class="sxs-lookup"><span data-stu-id="41472-160">none</span></span>                                          | <span data-ttu-id="41472-161">在 MTP 裝置上呼叫 [**IWMDMDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) 的應用程式所需。</span><span class="sxs-lookup"><span data-stu-id="41472-161">Required for applications that call [**IWMDMDevice3::DeviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) on MTP devices.</span></span> <span data-ttu-id="41472-162">定義各種標準 MTP 常數和結構。</span><span class="sxs-lookup"><span data-stu-id="41472-162">Defines various standard MTP constants and structures.</span></span>                                                                          |
| <span data-ttu-id="41472-163">C。</span><span class="sxs-lookup"><span data-stu-id="41472-163">Key.c</span></span>                            | <span data-ttu-id="41472-164">無</span><span class="sxs-lookup"><span data-stu-id="41472-164">none</span></span>                                          | <span data-ttu-id="41472-165">定義來自 Microsoft 的金鑰和憑證。</span><span class="sxs-lookup"><span data-stu-id="41472-165">Defines a key and certificate from Microsoft.</span></span> <span data-ttu-id="41472-166">SDK 隨附的版本包含測試虛擬機器碼，可讓您使用非 DRM 保護的 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="41472-166">The version shipped with the SDK includes a test dummy key that will allow the use of non-DRM protected Windows Media files.</span></span>                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="41472-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="41472-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41472-168">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="41472-168">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





