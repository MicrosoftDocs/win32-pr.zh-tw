---
title: Windows Media 裝置管理員 11 SDK
description: Windows Media 裝置管理員 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media 裝置管理員，關於
- 裝置管理員，關於
- '媒體傳輸通訊協定 (MTP) '
- 'MTP (媒體傳輸通訊協定) '
- '大量儲存類別 (SERVICES.MSC) '
- 'SERVICES.MSC (大型儲存類別) '
- Windows Media 裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- 桌面應用程式，關於
- Windows Media 裝置管理員、服務提供者
- 裝置管理員，服務提供者
- 服務提供者，關於
- Windows Media 裝置管理員、外掛程式
- 裝置管理員、外掛程式 insp
- 外掛程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383125"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="b69da-118">Windows Media 裝置管理員 11 SDK</span><span class="sxs-lookup"><span data-stu-id="b69da-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b69da-119">Windows Media 裝置管理員 Api 現在已包含在 Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="b69da-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="b69da-120">不需要其他 SDK 下載。</span><span class="sxs-lookup"><span data-stu-id="b69da-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="b69da-121">Microsoft Windows Media 裝置管理員軟體發展工具組 (SDK) 可讓您建立可與連線可攜式裝置通訊的桌面應用程式和元件。</span><span class="sxs-lookup"><span data-stu-id="b69da-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="b69da-122">Windows Media 裝置管理員可讓您的應用程式或元件列舉、探索和交換具有裝置的檔案、查詢中繼資料，以及要求播放次數資訊。</span><span class="sxs-lookup"><span data-stu-id="b69da-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="b69da-123">Windows Media 裝置管理員上建的應用程式或元件具有一致的 API，可與各種不同的裝置進行通訊，包括媒體傳輸通訊協定 (MTP) 、大型儲存類別 (SERVICES.MSC) 、RAPI，以及其他以最新版本和舊版 Windows Media 技術為基礎的其他裝置。</span><span class="sxs-lookup"><span data-stu-id="b69da-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="b69da-124">您可以使用 Windows Media 裝置管理員 SDK 來建立下列專案：</span><span class="sxs-lookup"><span data-stu-id="b69da-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="b69da-125">桌面應用程式，例如自訂媒體播放機。</span><span class="sxs-lookup"><span data-stu-id="b69da-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="b69da-126">應用程式和可攜式裝置之間的所有通訊都必須經過 Windows Media 裝置管理員，以作為應用程式、Microsoft 數位版權管理系統和服務提供者之間的代理程式。</span><span class="sxs-lookup"><span data-stu-id="b69da-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="b69da-127">服務提供者，可作為自訂裝置和桌面應用程式之間的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="b69da-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="b69da-128">雖然 Microsoft 提供數個服務提供者，可與大部分的裝置通訊，但您可以建立自訂服務提供者，以自訂裝置與桌面應用程式之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="b69da-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="b69da-129">外掛程式，可執行工作，例如要求和記錄裝置上的播放次數。</span><span class="sxs-lookup"><span data-stu-id="b69da-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="b69da-130">這些外掛程式可以附加至其他桌面應用程式，例如 Windows Media Player，以將資訊傳送給內容提供者來處理對演出者的專利款項。</span><span class="sxs-lookup"><span data-stu-id="b69da-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="b69da-131">若要下載 Windows Media 裝置管理員 SDK，請參閱 MSDN 網站上 [的 Windows Media 下載頁面](https://msdn.microsoft.com/windows/desktop/aa904949) 。</span><span class="sxs-lookup"><span data-stu-id="b69da-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="b69da-132">此 SDK 是 Microsoft Windows Media 軟體發展工具組的元件。</span><span class="sxs-lookup"><span data-stu-id="b69da-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="b69da-133">其他元件包括 Windows Media Format SDK、Windows Media Services SDK、Windows Media 編碼器 SDK、Windows Media Rights Manager SDK 和 Windows Media Player SDK。</span><span class="sxs-lookup"><span data-stu-id="b69da-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="b69da-134">本檔包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b69da-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="b69da-135">區段</span><span class="sxs-lookup"><span data-stu-id="b69da-135">Section</span></span>                                            | <span data-ttu-id="b69da-136">描述</span><span class="sxs-lookup"><span data-stu-id="b69da-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b69da-137">快速入門</span><span class="sxs-lookup"><span data-stu-id="b69da-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="b69da-138">描述這一版 Windows Media 裝置管理員的新功能、概述 Windows Media 裝置管理員的運作方式、描述開發應用程式或服務提供者所需的功能，並說明 SDK 隨附的範例。</span><span class="sxs-lookup"><span data-stu-id="b69da-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="b69da-139">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="b69da-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="b69da-140">討論如何建立應用程式和服務提供者。</span><span class="sxs-lookup"><span data-stu-id="b69da-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="b69da-141">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="b69da-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="b69da-142">提供 Windows Media 裝置管理員 SDK 所支援之介面、方法、類別和結構的 c + + 參考資訊。</span><span class="sxs-lookup"><span data-stu-id="b69da-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="b69da-143">*詞彙*</span><span class="sxs-lookup"><span data-stu-id="b69da-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="b69da-144">定義本檔中使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="b69da-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 




