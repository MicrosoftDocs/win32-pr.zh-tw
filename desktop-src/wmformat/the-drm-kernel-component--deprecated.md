---
title: 'DRM 核心元件 (已淘汰) '
description: 'DRM 核心元件 (已淘汰) '
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- 'Windows Media 格式 SDK、Microsoft 安全音訊路徑 (SAP) '
- '數位版權管理 (DRM) 、Microsoft 安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 、Microsoft 安全音訊路徑 (SAP) '
- Windows Media 格式 SDK， (SAP) 的安全音訊路徑
- '數位版權管理 (DRM) 的安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 的安全音訊路徑 (SAP) '
- Windows Media Format SDK，DRM 核心元件
- 數位版權管理 (DRM) ，核心元件
- DRM (數位版權管理) ，核心元件
- " (SAP) ，DRM 核心元件的 Microsoft 安全音訊路徑"
- " (SAP) ，DRM 核心元件的安全音訊路徑"
- SAP (安全音訊路徑) ，DRM 核心元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024308"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="2059b-115">DRM 核心元件 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="2059b-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="2059b-116">本頁面記載了在未來的 Windows 版本中，將會受到不同技術解決方案支援的功能。</span><span class="sxs-lookup"><span data-stu-id="2059b-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="2059b-117">在 Microsoft 安全音訊路徑 (SAP) 模型中，DRM 核心元件提供兩項基本功能，可保護加密音樂的完整性。</span><span class="sxs-lookup"><span data-stu-id="2059b-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="2059b-118">首先，當播放音樂檔案時，DRM 用戶端元件和 DRM 核心元件會進行通訊。</span><span class="sxs-lookup"><span data-stu-id="2059b-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="2059b-119">這兩個元件之間的通訊，可防止任何人篡改加密信號或插入 false 資訊。</span><span class="sxs-lookup"><span data-stu-id="2059b-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="2059b-120">其次，在所有剩餘的元件都經過驗證之前，DRM 核心元件不會將音樂信號解密。</span><span class="sxs-lookup"><span data-stu-id="2059b-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="2059b-121">也就是說，在解密內容並將它傳遞給下一個系統元件之前，DRM 核心元件會檢查每個可存取內容) 的元件 (每個元件的路徑，並確認這些元件已使用 Microsoft 的憑證進行簽署。</span><span class="sxs-lookup"><span data-stu-id="2059b-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="2059b-122">未簽署的元件可能表示有可疑的元件或惡意的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2059b-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="2059b-123">因此，當 DRM 核心元件驗證剩餘的元件時，如果有任何元件無法進行這項測試，則信號會暫停且無法播放。</span><span class="sxs-lookup"><span data-stu-id="2059b-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="2059b-124">否則，如果所有元件都通過驗證，DRM 核心元件會將音樂解密，並將其傳遞給下一個元件。</span><span class="sxs-lookup"><span data-stu-id="2059b-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="2059b-125">Microsoft 數位簽署的驅動程式會將 Windows®硬體品質實驗室 (WHQL) 測試，以確保使用者使用最高品質的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2059b-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="2059b-126">這是標準的做法，可確保元件的真實性，因為簽章無法偽造，也不能修改程式碼，而不會終結簽章。</span><span class="sxs-lookup"><span data-stu-id="2059b-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="2059b-127">經認證的安全音訊路徑的驅動程式，必須保護其所處理的音訊資料免于受信任元件的存取。</span><span class="sxs-lookup"><span data-stu-id="2059b-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="2059b-128">Windows Millennium Edition 和 Windows XP 隨附的驅動程式會更新為安全音訊路徑並簽署。</span><span class="sxs-lookup"><span data-stu-id="2059b-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="2059b-129">未簽署可用於 Windows Me 或 Windows XP 的驅動程式無法播放受保護的音樂。</span><span class="sxs-lookup"><span data-stu-id="2059b-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="2059b-130">驅動程式製造商可以重新發出經 WHQL 簽署的更新版驅動程式，並將其發佈到網際網路供取用者下載。</span><span class="sxs-lookup"><span data-stu-id="2059b-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2059b-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="2059b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2059b-132">**Microsoft 安全音訊路徑**</span><span class="sxs-lookup"><span data-stu-id="2059b-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




