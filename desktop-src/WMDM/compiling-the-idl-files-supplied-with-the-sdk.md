---
title: 編譯 SDK 提供的 IDL 檔案
description: 編譯 SDK 提供的 IDL 檔案
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media 裝置管理員、IDL 檔案
- 裝置管理員，IDL 檔案
- 桌面應用程式，IDL 檔案
- 服務提供者，IDL 檔案
- 程式設計指南，IDL 檔案
- IDL 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444009"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="5092b-109">編譯 SDK 提供的 IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="5092b-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="5092b-110">Windows Media 裝置管理員 SDK 包含這些標頭檔的標頭檔和來源 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="5092b-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="5092b-111">標頭檔位於 \\ \\ SDK 安裝路徑的 inc. 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="5092b-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="5092b-112">IDL 檔案位於 \\ idl \\ 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="5092b-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="5092b-113">先行編譯的標頭很容易使用，而且有數個 IDL 檔案會合並成單一提供的標頭。</span><span class="sxs-lookup"><span data-stu-id="5092b-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="5092b-114">但是，如果您決定要從提供的 IDL 檔案處理自己的標頭檔，本主題將說明哪些 IDL 檔案會建立哪些標頭檔，以及描述每個 IDL 檔案的相依性。</span><span class="sxs-lookup"><span data-stu-id="5092b-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="5092b-115">**相等的 IDL 和提供的標頭檔**</span><span class="sxs-lookup"><span data-stu-id="5092b-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="5092b-116">**Idl**</span><span class="sxs-lookup"><span data-stu-id="5092b-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="5092b-117">**對等提供的標頭**</span><span class="sxs-lookup"><span data-stu-id="5092b-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="5092b-118">**說明**</span><span class="sxs-lookup"><span data-stu-id="5092b-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5092b-119">WMDM .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-119">WMDM.idl</span></span><br/> <span data-ttu-id="5092b-120">WMSP .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-120">WMSP.idl</span></span><br/> <span data-ttu-id="5092b-121">WMSCP .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-121">WMSCP.idl</span></span><br/> <span data-ttu-id="5092b-122">icomponentauthenticate .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="5092b-123">Mswmdm。h</span><span class="sxs-lookup"><span data-stu-id="5092b-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="5092b-124">這四個 IDL 檔案都包含在這個單一提供的標頭中。</span><span class="sxs-lookup"><span data-stu-id="5092b-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="5092b-125">**WMDM** 會定義所有的應用程式介面，以及所需的結構、常數和錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5092b-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="5092b-126">**WMSP** 會定義所有服務提供者介面。</span><span class="sxs-lookup"><span data-stu-id="5092b-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="5092b-127">**WMSCP** 會定義安全內容提供者所需的所有介面、GUID 值和常數。</span><span class="sxs-lookup"><span data-stu-id="5092b-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="5092b-128">**icomponentauthenticate** 會定義 [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) 介面。</span><span class="sxs-lookup"><span data-stu-id="5092b-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="5092b-129">Wmdmlog .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="5092b-130">Wmdmlog。h</span><span class="sxs-lookup"><span data-stu-id="5092b-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="5092b-131">wmdmlog \_ c。</span><span class="sxs-lookup"><span data-stu-id="5092b-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="5092b-132">定義記錄介面。</span><span class="sxs-lookup"><span data-stu-id="5092b-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="5092b-133">由於 IDL 檔案有問題，因此必須使用所提供的標頭檔，而不只是 .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="5092b-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5092b-134">WMDRMDeviceApp .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="5092b-135">Wmdrmdeviceapp。h</span><span class="sxs-lookup"><span data-stu-id="5092b-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="5092b-136">定義應用程式所使用的 [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) 和 [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) 介面，以更新裝置上的 DRM 或裝置上的計量播放次數。</span><span class="sxs-lookup"><span data-stu-id="5092b-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="5092b-137">**IDL 相依性**</span><span class="sxs-lookup"><span data-stu-id="5092b-137">**IDL Dependencies**</span></span>

<span data-ttu-id="5092b-138">許多提供的 IDL 檔案都有組建相依性。</span><span class="sxs-lookup"><span data-stu-id="5092b-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="5092b-139">如果您打算自行編譯 IDL 檔案，您必須依照下表所示的順序來處理這些外部相依性。</span><span class="sxs-lookup"><span data-stu-id="5092b-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="5092b-140">Idl</span><span class="sxs-lookup"><span data-stu-id="5092b-140">IDL</span></span>                      |   <span data-ttu-id="5092b-141">相依性</span><span class="sxs-lookup"><span data-stu-id="5092b-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5092b-142">icomponentauthenticate .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="5092b-143">匯入 "oaidl.idl .idl";</span><span class="sxs-lookup"><span data-stu-id="5092b-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="5092b-144">\#包含 "icomponentauthenticate .idl"</span><span class="sxs-lookup"><span data-stu-id="5092b-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="5092b-145">WMDM .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-145">WMDM.idl</span></span>                   | <span data-ttu-id="5092b-146">沒有外部相依性</span><span class="sxs-lookup"><span data-stu-id="5092b-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="5092b-147">WmdmLog .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-147">WmdmLog.idl</span></span>                | <span data-ttu-id="5092b-148">沒有外部相依性</span><span class="sxs-lookup"><span data-stu-id="5092b-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="5092b-149">WMDRMDeviceApp .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="5092b-150">沒有外部相依性</span><span class="sxs-lookup"><span data-stu-id="5092b-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="5092b-151">WMSCP .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-151">WMSCP.idl</span></span>                  | <span data-ttu-id="5092b-152">\#包含 "WMDRMDeviceApp .idl"</span><span class="sxs-lookup"><span data-stu-id="5092b-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="5092b-153">\#包含 "WMSP .idl"</span><span class="sxs-lookup"><span data-stu-id="5092b-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="5092b-154">WMSP .idl</span><span class="sxs-lookup"><span data-stu-id="5092b-154">WMSP.idl</span></span>                   | <span data-ttu-id="5092b-155">\#包含 "WMDM .idl"</span><span class="sxs-lookup"><span data-stu-id="5092b-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="5092b-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="5092b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5092b-157">**應用程式和服務提供者的一般工作**</span><span class="sxs-lookup"><span data-stu-id="5092b-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





