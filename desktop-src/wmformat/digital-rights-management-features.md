---
title: 數位 Rights Management 功能
description: 數位 Rights Management 功能
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media Format SDK，DRM 功能
- 數位版權管理 (DRM) ，功能
- DRM (數位版權管理) ，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682535"
---
# <a name="digital-rights-management-features"></a><span data-ttu-id="2ca7d-106">數位 Rights Management 功能</span><span class="sxs-lookup"><span data-stu-id="2ca7d-106">Digital Rights Management Features</span></span>

<span data-ttu-id="2ca7d-107">\[Windows Media DRM 功能已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-107">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="2ca7d-108">請改用 [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) 。\]</span><span class="sxs-lookup"><span data-stu-id="2ca7d-108">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="2ca7d-109">數位版權管理 (DRM) 是一種技術，內容擁有者可以使用金鑰來加密數位媒體檔案， (一段資料來鎖定和解除鎖定內容) 。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-109">Digital rights management (DRM) is a technology that content owners can use to protect digital media files by encrypting them with a key (a piece of data that locks and unlocks the content).</span></span> <span data-ttu-id="2ca7d-110">若要播放受保護的 ASF 檔案，取用者必須取得包含金鑰的個別授權。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-110">To play a protected ASF file, a consumer must obtain a separate license containing the key.</span></span> <span data-ttu-id="2ca7d-111">每份授權也包含內容擁有者或授權簽發者所決定的許可權，以指定取用者如何使用該檔案。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-111">Each license also contains rights, determined by the content owner or license issuer, which specify how the consumer can use the file.</span></span> <span data-ttu-id="2ca7d-112">內容擁有者可以使用 DRM 技術，透過網際網路以受保護的檔案格式傳遞歌曲、影片和其他數位媒體檔案，並控制其數位內容的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-112">Using DRM technology, content owners can deliver songs, videos, and other digital media files over the Internet in a protected file format and control the use of their digital content.</span></span> <span data-ttu-id="2ca7d-113">Windows Media Rights Manager、Windows Media 編碼器和 Windows Media Player 也支援 Microsoft DRM 技術。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-113">Microsoft DRM technology is also supported by the Windows Media Rights Manager, the Windows Media Encoder, and Windows Media Player.</span></span> <span data-ttu-id="2ca7d-114">如需有關 Microsoft DRM 技術的詳細背景資訊，請參閱 [Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media)網站。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-114">For more background information on Microsoft's DRM technology, see the [Microsoft Windows Media Web site](https://support.microsoft.com/help/17946/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="2ca7d-115">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-115">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="2ca7d-116">下列各節討論 Windows Media Format SDK 的主要 DRM 相關功能。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-116">The following sections discuss the main DRM-related features of the Windows Media Format SDK.</span></span>



| <span data-ttu-id="2ca7d-117">區段</span><span class="sxs-lookup"><span data-stu-id="2ca7d-117">Section</span></span>                                                                                            | <span data-ttu-id="2ca7d-118">描述</span><span class="sxs-lookup"><span data-stu-id="2ca7d-118">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ca7d-119">DRM 基本概念</span><span class="sxs-lookup"><span data-stu-id="2ca7d-119">DRM Basics</span></span>](drm-basics.md)                                                                       | <span data-ttu-id="2ca7d-120">提供 Windows Media Format SDK 所提供之 DRM 功能的簡短總覽。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-120">Provides a brief overview of the DRM functionality provided by the Windows Media Format SDK.</span></span>                                         |
| [<span data-ttu-id="2ca7d-121">DRM 版本</span><span class="sxs-lookup"><span data-stu-id="2ca7d-121">DRM Versions</span></span>](drm-versions.md)                                                                   | <span data-ttu-id="2ca7d-122">說明可用於應用程式之 DRM 保護版本之間的主要差異。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-122">Describes the main differences between the versions of DRM protection available to applications.</span></span>                                     |
| [<span data-ttu-id="2ca7d-123">即時 DRM</span><span class="sxs-lookup"><span data-stu-id="2ca7d-123">Live DRM</span></span>](live-drm.md)                                                                           | <span data-ttu-id="2ca7d-124">描述「即時」 DRM 保護所能實現的案例。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-124">Describes the scenarios made possible by "on the fly" DRM protection.</span></span>                                                                |
| [<span data-ttu-id="2ca7d-125">DRM 的個人化</span><span class="sxs-lookup"><span data-stu-id="2ca7d-125">DRM Individualization</span></span>](drm-individualization.md)                                                 | <span data-ttu-id="2ca7d-126">描述 DRM 內容擁有者或授權簽發者所能要求的應用程式安全性升級。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-126">Describes the application security upgrade that DRM content owners or license issuers can require.</span></span>                                   |
| [<span data-ttu-id="2ca7d-127">備份與還原 DRM 授權</span><span class="sxs-lookup"><span data-stu-id="2ca7d-127">Backing Up and Restoring of DRM Licenses</span></span>](backing-up-and-restoring-of-drm-licenses.md)           | <span data-ttu-id="2ca7d-128">說明允許使用者備份和還原其內容授權的優缺點。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-128">Describes the pros and cons of permitting users to back up and restore their content licenses.</span></span>                                       |
| [<span data-ttu-id="2ca7d-129">在中繼資料編輯器中查看 DRM 屬性</span><span class="sxs-lookup"><span data-stu-id="2ca7d-129">Viewing DRM Attributes in the Metadata Editor</span></span>](viewing-drm-attributes-in-the-metadata-editor.md) | <span data-ttu-id="2ca7d-130">描述此 DRM helper 物件的功能，以及其設計來支援的案例。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-130">Describes the capabilities of this DRM helper object and the scenarios it was designed to support.</span></span>                                   |
| [<span data-ttu-id="2ca7d-131">輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="2ca7d-131">Output Protection Levels</span></span>](output-protection-levels.md)                                           | <span data-ttu-id="2ca7d-132">描述輸出保護層級如何讓 DRM 版本10授權更具彈性。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-132">Describes how Output Protection Levels make DRM version 10 licenses more flexible.</span></span>                                                   |
| [<span data-ttu-id="2ca7d-133">授權撤銷</span><span class="sxs-lookup"><span data-stu-id="2ca7d-133">License Revocation</span></span>](license-revocation.md)                                                       | <span data-ttu-id="2ca7d-134">描述授權撤銷。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-134">Describes license revocation.</span></span>                                                                                                        |
| [<span data-ttu-id="2ca7d-135">適用于網路裝置的 Windows Media DRM 10</span><span class="sxs-lookup"><span data-stu-id="2ca7d-135">Windows Media DRM 10 for Network Devices</span></span>](windows-media-drm-10-for-network-devices.md)           | <span data-ttu-id="2ca7d-136">介紹適用于網路裝置的 Windows Media DRM 10，以及在此 SDK 中的實作為。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-136">Introduces Windows Media DRM 10 for Network Devices and its implementation in this SDK.</span></span>                                              |
| [<span data-ttu-id="2ca7d-137">Microsoft 安全音訊路徑</span><span class="sxs-lookup"><span data-stu-id="2ca7d-137">Microsoft Secure Audio Path</span></span>](microsoft-secure-audio-path--deprecated.md)                         | <span data-ttu-id="2ca7d-138">描述 Microsoft 安全音訊路徑架構，它可為受保護的音訊內容提供最高程度的保護。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-138">Describes the Microsoft Secure Audio Path architecture, which provides the highest degree of protection for protected audio content.</span></span> |
| [<span data-ttu-id="2ca7d-139">播放清單燒錄</span><span class="sxs-lookup"><span data-stu-id="2ca7d-139">Playlist Burning</span></span>](playlist-burning.md)                                                           | <span data-ttu-id="2ca7d-140">描述 DRM 的播放清單燒錄功能，以及 Windows Media Format SDK 中支援的功能。</span><span class="sxs-lookup"><span data-stu-id="2ca7d-140">Describes the playlist-burning feature of DRM and how it is supported in the Windows Media Format SDK.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="2ca7d-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ca7d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca7d-142">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="2ca7d-142">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="2ca7d-143">**特性**</span><span class="sxs-lookup"><span data-stu-id="2ca7d-143">**Features**</span></span>](features.md)
</dt> </dl>

 

 