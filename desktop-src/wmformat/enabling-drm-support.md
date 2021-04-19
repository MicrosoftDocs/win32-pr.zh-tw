---
title: 啟用 DRM 支援
description: 啟用 DRM 支援
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Media Format SDK，啟用 DRM 支援
- Advanced Systems Format (ASF) ，啟用 DRM 支援
- ASF (Advanced Systems Format) ，啟用 DRM 支援
- 數位版權管理 (DRM) ，啟用支援
- DRM (數位版權管理) ，啟用支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106979673"
---
# <a name="enabling-drm-support"></a><span data-ttu-id="51f09-108">啟用 DRM 支援</span><span class="sxs-lookup"><span data-stu-id="51f09-108">Enabling DRM Support</span></span>

<span data-ttu-id="51f09-109">您可以使用 Microsoft Windows Media Format 軟體發展工具組 (SDK) 來建立應用程式，這些應用程式可以套用數位版權管理 (DRM) 保護，以及播放即時 DRM 串流或受 DRM 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="51f09-109">You can use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that can apply digital rights management (DRM) protection and play live-DRM streams or DRM-protected files.</span></span> <span data-ttu-id="51f09-110">也提供針對備份和還原播放程式的 DRM 授權，以及 [*individualizing*](wmformat-glossary.md) 播放程式的支援。</span><span class="sxs-lookup"><span data-stu-id="51f09-110">Support is also provided for backing up and restoring a player's DRM licenses, and for [*individualizing*](wmformat-glossary.md) players.</span></span>

<span data-ttu-id="51f09-111">本檔假設您對 Microsoft 的數位版權管理技術有基本的熟悉度。</span><span class="sxs-lookup"><span data-stu-id="51f09-111">This documentation assumes that you have a basic familiarity with Microsoft's digital rights management technology.</span></span> <span data-ttu-id="51f09-112">本檔的 [數位 Rights Management 功能](digital-rights-management-features.md) 一節提供 WINDOWS Media DRM 的基本總覽。</span><span class="sxs-lookup"><span data-stu-id="51f09-112">A basic overview of Windows Media DRM is provided in the [Digital Rights Management Features](digital-rights-management-features.md) section of this documentation.</span></span> <span data-ttu-id="51f09-113">如需 DRM 的詳細資訊，請參閱 [Microsoft](https://windows.microsoft.com/windows/products/windows-media)網站上的數位 Rights Management 頁面。</span><span class="sxs-lookup"><span data-stu-id="51f09-113">For more information on DRM, see the Digital Rights Management page at the [Microsoft Web site](https://windows.microsoft.com/windows/products/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="51f09-114">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="51f09-114">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="51f09-115">下列各節說明如何啟用 DRM 支援。</span><span class="sxs-lookup"><span data-stu-id="51f09-115">The following sections describe how to enable DRM support.</span></span>



| <span data-ttu-id="51f09-116">區段</span><span class="sxs-lookup"><span data-stu-id="51f09-116">Section</span></span>                                                                                                                        | <span data-ttu-id="51f09-117">描述</span><span class="sxs-lookup"><span data-stu-id="51f09-117">Description</span></span>                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51f09-118">取得必要的 DRM 程式庫</span><span class="sxs-lookup"><span data-stu-id="51f09-118">Obtaining the Required DRM Library</span></span>](obtaining-the-required-drm-library.md)                                                   | <span data-ttu-id="51f09-119">描述取得建立啟用 DRM 的應用程式所需的靜態程式庫時所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="51f09-119">Describes the steps involved in obtaining the static library that is required to create DRM-enabled applications.</span></span>                                                                               |
| [<span data-ttu-id="51f09-120">DRM 保護和內容授權發佈</span><span class="sxs-lookup"><span data-stu-id="51f09-120">DRM Protection and Content License Distribution</span></span>](drm-protection-and-content-license-distribution.md)                         | <span data-ttu-id="51f09-121">比較 Windows Media Format SDK 與 Windows Media Rights Manager SDK 的 DRM 功能。</span><span class="sxs-lookup"><span data-stu-id="51f09-121">Compares the DRM capabilities of the Windows Media Format SDK with the Windows Media Rights Manager SDK.</span></span>                                                                                        |
| [<span data-ttu-id="51f09-122">DRM 網路作業</span><span class="sxs-lookup"><span data-stu-id="51f09-122">DRM Network Operations</span></span>](drm-network-operations.md)                                                                           | <span data-ttu-id="51f09-123">描述您的應用程式應該如何處理透過網際網路或其他網路通訊的 DRM 作業。</span><span class="sxs-lookup"><span data-stu-id="51f09-123">Describes how your application should handle the DRM operations that communicate over the Internet, or other networks.</span></span>                                                                          |
| [<span data-ttu-id="51f09-124">建立受保護的檔案</span><span class="sxs-lookup"><span data-stu-id="51f09-124">Creating Protected Files</span></span>](creating-protected-files.md)                                                                       | <span data-ttu-id="51f09-125">說明如何建立受 DRM 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="51f09-125">Describes how to create DRM-protected files.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="51f09-126">讀取受保護的檔案</span><span class="sxs-lookup"><span data-stu-id="51f09-126">Reading Protected Files</span></span>](reading-protected-files.md)                                                                         | <span data-ttu-id="51f09-127">描述取得內容授權的方法，以及執行無訊息授權取得的優點。</span><span class="sxs-lookup"><span data-stu-id="51f09-127">Describes ways to acquire licenses for content and the benefits of implementing silent license acquisition.</span></span>                                                                                     |
| [<span data-ttu-id="51f09-128">查看受保護檔案的屬性</span><span class="sxs-lookup"><span data-stu-id="51f09-128">Viewing Attributes of Protected Files</span></span>](viewing-attributes-of-protected-files.md)                                             | <span data-ttu-id="51f09-129">描述如何使用 [中繼資料編輯器] 物件上的 [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) 介面來查看受保護檔案的屬性，而不需要 DRM 的必要靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="51f09-129">Describes how to use the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface on the metadata editor object to view attributes of protected files without having the required static library for DRM.</span></span> |
| [<span data-ttu-id="51f09-130">使用撤銷清單</span><span class="sxs-lookup"><span data-stu-id="51f09-130">Working with Revocation Lists</span></span>](working-with-revocation-lists.md)                                                             | <span data-ttu-id="51f09-131">描述撤銷清單及其執行方式。</span><span class="sxs-lookup"><span data-stu-id="51f09-131">Describes revocation lists and how they are implemented.</span></span>                                                                                                                                        |
| [<span data-ttu-id="51f09-132">備份和還原授權</span><span class="sxs-lookup"><span data-stu-id="51f09-132">Backing Up and Restoring Licenses</span></span>](backing-up-and-restoring-licenses.md)                                                     | <span data-ttu-id="51f09-133">描述使用者如何藉由備份和還原到目前的電腦或其他電腦，來管理其內容授權。</span><span class="sxs-lookup"><span data-stu-id="51f09-133">Describes how users can manage their content licenses by backing up and restoring them to their current computer or to other computers.</span></span>                                                         |
| [<span data-ttu-id="51f09-134">Individualizing DRM 應用程式</span><span class="sxs-lookup"><span data-stu-id="51f09-134">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)                                                       | <span data-ttu-id="51f09-135">描述 [*如何在 DRM*](wmformat-glossary.md) 系統中提高安全性。</span><span class="sxs-lookup"><span data-stu-id="51f09-135">Describes how the [*individualization*](wmformat-glossary.md) feature increases security in a DRM system.</span></span>                                                           |
| [<span data-ttu-id="51f09-136">使用輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="51f09-136">Working with Output Protection Levels</span></span>](working-with-output-protection-levels.md)                                             | <span data-ttu-id="51f09-137">說明如何支援輸出保護層級，這些層級可用來記錄 DRM 版本10授權中的允許動作。</span><span class="sxs-lookup"><span data-stu-id="51f09-137">Describes how to support Output Protection Levels, which are used to record allowed actions in DRM version 10 licenses.</span></span>                                                                         |
| [<span data-ttu-id="51f09-138">使用 Windows Media DRM 10 進行網路裝置通訊協定</span><span class="sxs-lookup"><span data-stu-id="51f09-138">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md) | <span data-ttu-id="51f09-139">說明如何使用適用于網路裝置的 Windows Media DRM 10 通訊協定來支援安全裝置串流。</span><span class="sxs-lookup"><span data-stu-id="51f09-139">Describes how to support secure device streaming by using the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                                                |
| [<span data-ttu-id="51f09-140">執行授權撤銷</span><span class="sxs-lookup"><span data-stu-id="51f09-140">Implementing License Revocation</span></span>](implementing-license-revocation.md)                                                         | <span data-ttu-id="51f09-141">描述授權撤銷的程式，以及您的應用程式必須採取才能執行的動作。</span><span class="sxs-lookup"><span data-stu-id="51f09-141">Describes the process of license revocation, and the actions your application must take to implement it.</span></span>                                                                                        |
| [<span data-ttu-id="51f09-142">燒錄包含安全檔案的播放清單</span><span class="sxs-lookup"><span data-stu-id="51f09-142">Burning Playlists That Contain Secure Files</span></span>](burning-playlists-that-contain-secure-files.md)                                 | <span data-ttu-id="51f09-143">描述如何在您的應用程式中執行播放清單燒錄。</span><span class="sxs-lookup"><span data-stu-id="51f09-143">Describes how to implement playlist burning in your application.</span></span>                                                                                                                                |



 

<span data-ttu-id="51f09-144">SDK 包含數個範例應用程式，示範如何讀取受保護的檔案;最完整的範例是 DRMShow。</span><span class="sxs-lookup"><span data-stu-id="51f09-144">The SDK includes several sample applications that demonstrate how to read protected files; the fullest example is DRMShow.</span></span> <span data-ttu-id="51f09-145">如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="51f09-145">For more information, see [Sample Applications](sample-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51f09-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="51f09-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51f09-147">**特性**</span><span class="sxs-lookup"><span data-stu-id="51f09-147">**Features**</span></span>](features.md)
</dt> </dl>

 

 




