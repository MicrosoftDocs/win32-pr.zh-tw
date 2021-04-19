---
title: " (淘汰的) 觀看或修改音樂信號"
description: " (淘汰的) 觀看或修改音樂信號"
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- 'Windows Media 格式 SDK、Microsoft 安全音訊路徑 (SAP) '
- '數位版權管理 (DRM) 、Microsoft 安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 、Microsoft 安全音訊路徑 (SAP) '
- Windows Media 格式 SDK， (SAP) 的安全音訊路徑
- '數位版權管理 (DRM) 的安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 的安全音訊路徑 (SAP) '
- Windows Media Format SDK、音樂信號觀賞或修改
- 數位版權管理 (DRM) 、音樂信號觀賞或修改
- DRM (數位版權管理) 、音樂信號觀賞或修改
- Microsoft 安全音訊路徑 (SAP) 、音樂信號觀賞或修改
- " (SAP) 的安全音訊路徑、觀看或修改音樂信號"
- SAP (安全音訊路徑) 、音樂信號觀賞或修改
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969481"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="20c47-115"> (淘汰的) 觀看或修改音樂信號</span><span class="sxs-lookup"><span data-stu-id="20c47-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="20c47-116">本頁面記載了在未來的 Windows 版本中，將會受到不同技術解決方案支援的功能。</span><span class="sxs-lookup"><span data-stu-id="20c47-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="20c47-117">在 Microsoft 安全音訊路徑 (SAP) 模型中，應用程式無法以任何方式修改受保護的音樂。</span><span class="sxs-lookup"><span data-stu-id="20c47-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="20c47-118">例如，當應用程式嘗試攔截音樂信號時，信號聽起來像是隨機雜訊。</span><span class="sxs-lookup"><span data-stu-id="20c47-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="20c47-119">如此一來，通常會修改信號 (的應用程式（例如等化器) ）無法變更音樂的音效。</span><span class="sxs-lookup"><span data-stu-id="20c47-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="20c47-120">有些應用程式只會看到音樂信號。</span><span class="sxs-lookup"><span data-stu-id="20c47-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="20c47-121">例如，有些應用程式會以音樂信號顯示時間閃爍的燈，但不會加以修改。</span><span class="sxs-lookup"><span data-stu-id="20c47-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="20c47-122">為了容納可查看信號的應用程式，會以純文字格式解密音樂的一小部分，並以加密的內容傳遞。</span><span class="sxs-lookup"><span data-stu-id="20c47-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="20c47-123">產生的信號很差 (比電話品質更糟) 但可滿足用來查看信號的應用程式。</span><span class="sxs-lookup"><span data-stu-id="20c47-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20c47-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="20c47-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c47-125">**Microsoft 安全音訊路徑**</span><span class="sxs-lookup"><span data-stu-id="20c47-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




