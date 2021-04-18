---
title: Microsoft Windows Media DRM 用戶端介面
description: Microsoft Windows Media DRM 用戶端介面
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK，介面
- 數位版權管理 (DRM) ，介面
- DRM (數位版權管理) ，介面
- DRM 用戶端擴充 Api，介面
- 用戶端擴充 Api，介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383581"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="68ffe-108">Microsoft Windows Media DRM 用戶端介面</span><span class="sxs-lookup"><span data-stu-id="68ffe-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="68ffe-109">下表說明 Windows Media DRM 用戶端 Api 所支援的介面。</span><span class="sxs-lookup"><span data-stu-id="68ffe-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="68ffe-110">介面</span><span class="sxs-lookup"><span data-stu-id="68ffe-110">Interface</span></span>                                                                    | <span data-ttu-id="68ffe-111">描述</span><span class="sxs-lookup"><span data-stu-id="68ffe-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68ffe-112">**IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="68ffe-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="68ffe-113">提供狀態回呼的定義，您可以執行此作業來處理非同步 DRM 作業。</span><span class="sxs-lookup"><span data-stu-id="68ffe-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="68ffe-114">**IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="68ffe-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="68ffe-115">提供解密內容的方法。</span><span class="sxs-lookup"><span data-stu-id="68ffe-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="68ffe-116">**IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="68ffe-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="68ffe-117">提供就地加密資料的方法。</span><span class="sxs-lookup"><span data-stu-id="68ffe-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="68ffe-118">**IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="68ffe-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="68ffe-119">加密非連續區塊中的資料。</span><span class="sxs-lookup"><span data-stu-id="68ffe-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="68ffe-120">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="68ffe-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="68ffe-121">**IMFMediaEventGenerator** 介面的延伸模組，可提供取消非同步作業的方法。</span><span class="sxs-lookup"><span data-stu-id="68ffe-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="68ffe-122">**IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="68ffe-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="68ffe-123">啟用有關「個人化」進度的 advanced status 資訊。</span><span class="sxs-lookup"><span data-stu-id="68ffe-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="68ffe-124">**IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="68ffe-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="68ffe-125">代表本機授權存放區中的一或多個授權。</span><span class="sxs-lookup"><span data-stu-id="68ffe-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="68ffe-126">**IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="68ffe-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="68ffe-127">啟用有關授權備份或還原作業的詳細狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="68ffe-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="68ffe-128">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="68ffe-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="68ffe-129">啟用本機授權存放的管理作業。</span><span class="sxs-lookup"><span data-stu-id="68ffe-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="68ffe-130">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="68ffe-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="68ffe-131">提供本機授權存放區的其他管理選項。</span><span class="sxs-lookup"><span data-stu-id="68ffe-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="68ffe-132">**IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="68ffe-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="68ffe-133">可讓應用程式查詢受保護檔案的許可權和授權狀態。</span><span class="sxs-lookup"><span data-stu-id="68ffe-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="68ffe-134">**IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="68ffe-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="68ffe-135">提供所需的方法來建立網路裝置接收者應用程式的 Microsoft Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="68ffe-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="68ffe-136">**IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="68ffe-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="68ffe-137">提供所需的方法，為網路裝置發送器應用程式建立 Microsoft Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="68ffe-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="68ffe-138">**IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="68ffe-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="68ffe-139">提供可讓使用者介入取得授權的方法。</span><span class="sxs-lookup"><span data-stu-id="68ffe-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="68ffe-140">**IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="68ffe-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="68ffe-141">建立 Microsoft Windows Media DRM 用戶端擴充 Api 的其他物件。</span><span class="sxs-lookup"><span data-stu-id="68ffe-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="68ffe-142">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="68ffe-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="68ffe-143">管理用戶端電腦和 DRM 子系統的各種安全性相關處理常式。</span><span class="sxs-lookup"><span data-stu-id="68ffe-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="68ffe-144">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="68ffe-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="68ffe-145">管理元件撤銷和更新。</span><span class="sxs-lookup"><span data-stu-id="68ffe-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="68ffe-146">**IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="68ffe-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="68ffe-147">啟用緩衝區的加密和解密。</span><span class="sxs-lookup"><span data-stu-id="68ffe-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="68ffe-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="68ffe-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ffe-149">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="68ffe-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




