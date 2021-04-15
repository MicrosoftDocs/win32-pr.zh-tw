---
title: " (淘汰的安全音訊路徑模型) "
description: " (淘汰的安全音訊路徑模型) "
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- 'Windows Media 格式 SDK、Microsoft 安全音訊路徑 (SAP) '
- '數位版權管理 (DRM) 、Microsoft 安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 、Microsoft 安全音訊路徑 (SAP) '
- Windows Media 格式 SDK， (SAP) 的安全音訊路徑
- '數位版權管理 (DRM) 的安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 的安全音訊路徑 (SAP) '
- Microsoft 安全音訊路徑 (SAP) ，模型
- " (SAP) 、模型的安全音訊路徑"
- SAP (安全音訊路徑) ，模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372085"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="8d236-112"> (淘汰的安全音訊路徑模型) </span><span class="sxs-lookup"><span data-stu-id="8d236-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="8d236-113">本頁面記載了在未來的 Windows 版本中，將會受到不同技術解決方案支援的功能。</span><span class="sxs-lookup"><span data-stu-id="8d236-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="8d236-114">Microsoft 安全音訊路徑 (SAP) 是 Microsoft Windows® Me 和 Microsoft Windows XP 的一項功能。</span><span class="sxs-lookup"><span data-stu-id="8d236-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="8d236-115">只有透過安全音訊路徑來播放音訊檔案的需求，是在 DRM 授權中指定，並由 DRM 用戶端元件強制執行。</span><span class="sxs-lookup"><span data-stu-id="8d236-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="8d236-116">在一開始保護僅限 SAP 的檔案時，不會新增額外的加密。</span><span class="sxs-lookup"><span data-stu-id="8d236-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="8d236-117">在播放時，DRM 元件會自動新增 SAP 加密，就像播放時所牽涉到的所有軟體元件的驗證程式一樣。</span><span class="sxs-lookup"><span data-stu-id="8d236-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="8d236-118">因此，SAP 的運作方式對應用程式而言是完全透明的，這就是為什麼 Windows Media Format SDK 沒有任何方法或屬性可用於啟用或停用 SAP。</span><span class="sxs-lookup"><span data-stu-id="8d236-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="8d236-119">如有需要，在建立受保護的檔案時，內容擁有者可以新增名為 "DRMHeader. SAPRequired" 的自訂標頭屬性，以指示授權伺服器將 SAP 需求新增至授權。</span><span class="sxs-lookup"><span data-stu-id="8d236-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="8d236-120">這種配置的執行是由內容擁有者和授權服務所組成。</span><span class="sxs-lookup"><span data-stu-id="8d236-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="8d236-121">在目前的 DRM 模型中，如果未套用 SAP，當播放受保護的數位音樂時，加密的內容會傳遞至 DRM 用戶端元件。</span><span class="sxs-lookup"><span data-stu-id="8d236-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="8d236-122">DRM 用戶端會驗證結合 Windows Media 格式 SDK 的應用程式和 DRM 元件是否有效。</span><span class="sxs-lookup"><span data-stu-id="8d236-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="8d236-123">如果有效，DRM 用戶端會解密內容，並將內容傳送至應用程式，然後將它傳送至較低層的音訊元件。</span><span class="sxs-lookup"><span data-stu-id="8d236-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="8d236-124">此時，解密的音樂適用于使用者模式應用程式和外掛程式，以及可以攔截解密音訊位的核心模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8d236-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="8d236-125">套用安全音訊路徑需求時，該內容不會由應用程式解密，而是會以加密狀態傳遞給較低層級的元件，而這些元件全都由 Microsoft 驗證為值得信任。</span><span class="sxs-lookup"><span data-stu-id="8d236-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="8d236-126">受信任的音訊元件是指除了其他特定的受信任元件之外，不會將音訊內容提供給任何系統元件。</span><span class="sxs-lookup"><span data-stu-id="8d236-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="8d236-127">如此一來，數位內容就會一直向下保護到驅動程式等級。</span><span class="sxs-lookup"><span data-stu-id="8d236-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="8d236-128">下圖顯示與安全音訊路徑模型比較的目前模型。</span><span class="sxs-lookup"><span data-stu-id="8d236-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![安全音訊路徑模型的圖表](images/sap.png)

 

 




