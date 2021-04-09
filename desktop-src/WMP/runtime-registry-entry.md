---
title: 執行時間登錄專案
description: 執行時間登錄專案
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player，執行時間登錄專案
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，執行時間專案
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- 執行時間登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021693"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="e0c45-111">執行時間登錄專案</span><span class="sxs-lookup"><span data-stu-id="e0c45-111">Runtime Registry Entry</span></span>

<span data-ttu-id="e0c45-112">當 Windows Media Player 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="e0c45-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="e0c45-113">此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。</span><span class="sxs-lookup"><span data-stu-id="e0c45-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="e0c45-114">其中一個可出現在擴充功能子機碼底下的登錄專案是 **運行** 時間專案。</span><span class="sxs-lookup"><span data-stu-id="e0c45-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="e0c45-115">**運行** 時間專案會指定 Windows Media Player 可用來播放或轉換具有自訂延伸模組之數位媒體檔案的基礎技術。</span><span class="sxs-lookup"><span data-stu-id="e0c45-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="e0c45-116">**運行** 時間專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="e0c45-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="e0c45-117">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e0c45-117">**Name**</span></span> | <span data-ttu-id="e0c45-118">**型別**</span><span class="sxs-lookup"><span data-stu-id="e0c45-118">**Type**</span></span>       | <span data-ttu-id="e0c45-119">**ReplTest1**</span><span class="sxs-lookup"><span data-stu-id="e0c45-119">**Value**</span></span>                                                     |
| <span data-ttu-id="e0c45-120">執行階段</span><span class="sxs-lookup"><span data-stu-id="e0c45-120">Runtime</span></span>  | <span data-ttu-id="e0c45-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e0c45-121">**REG\_DWORD**</span></span> | <span data-ttu-id="e0c45-122">識別基礎技術的正整數。</span><span class="sxs-lookup"><span data-stu-id="e0c45-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="e0c45-123">**運行** 時間專案的值必須是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="e0c45-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="e0c45-124">**值 (decimal)**</span><span class="sxs-lookup"><span data-stu-id="e0c45-124">**Value (decimal)**</span></span> | <span data-ttu-id="e0c45-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="e0c45-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c45-126">6</span><span class="sxs-lookup"><span data-stu-id="e0c45-126">6</span></span>                   | <span data-ttu-id="e0c45-127">使用 Windows Media Format SDK 轉譯。</span><span class="sxs-lookup"><span data-stu-id="e0c45-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="e0c45-128">7</span><span class="sxs-lookup"><span data-stu-id="e0c45-128">7</span></span>                   | <span data-ttu-id="e0c45-129">使用 Microsoft DirectShow 轉譯。</span><span class="sxs-lookup"><span data-stu-id="e0c45-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="e0c45-130">13</span><span class="sxs-lookup"><span data-stu-id="e0c45-130">13</span></span>                  | <span data-ttu-id="e0c45-131">使用指定的轉換外掛程式來轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="e0c45-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="e0c45-132">需要 Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="e0c45-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="e0c45-133">Windows Media Player 9 系列和更新版本支援 **運行** 時間登錄專案值6和7。</span><span class="sxs-lookup"><span data-stu-id="e0c45-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="e0c45-134">Windows Media Player 11 支援值13。</span><span class="sxs-lookup"><span data-stu-id="e0c45-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c45-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0c45-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c45-136">**ConvertPluginCLSID 子機碼**</span><span class="sxs-lookup"><span data-stu-id="e0c45-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="e0c45-137">**副檔名登錄設定**</span><span class="sxs-lookup"><span data-stu-id="e0c45-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




