---
title: 設定 VBR 資料流程
description: 設定 VBR 資料流程
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 資料流程，IWMPropertyVault 介面
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932924"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="3c2bb-109">設定 VBR 資料流程</span><span class="sxs-lookup"><span data-stu-id="3c2bb-109">Configuring VBR Streams</span></span>

<span data-ttu-id="3c2bb-110">您可以使用變數位元速率 (VBR) 編碼來產生本機檔案的高品質串流，或進行下載和播放。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="3c2bb-111">有三個適用于 VBR 的選項：品質型 (一次傳遞) 、未受限制的 (雙通路) ，以及限制 (雙通路) 。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="3c2bb-112">如需有關 VBR 編碼類型的詳細資訊，請參閱 [變數位元速率 (VBR) 編碼](variable-bit-rate--vbr--encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="3c2bb-113">您可以使用 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) 介面設定屬性，以在設定檔中設定 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="3c2bb-114">下表說明用來設定 VBR 編碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="3c2bb-115">屬性</span><span class="sxs-lookup"><span data-stu-id="3c2bb-115">Property</span></span>                     | <span data-ttu-id="3c2bb-116">描述</span><span class="sxs-lookup"><span data-stu-id="3c2bb-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2bb-117">**g \_ wszVBREnabled**</span><span class="sxs-lookup"><span data-stu-id="3c2bb-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="3c2bb-118">布林值。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-118">Boolean value.</span></span> <span data-ttu-id="3c2bb-119">設定為 True 以使用 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="3c2bb-120">**g \_ wszVBRQuality**</span><span class="sxs-lookup"><span data-stu-id="3c2bb-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="3c2bb-121">**DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-121">**DWORD** value.</span></span> <span data-ttu-id="3c2bb-122">設定為所需的品質層級 (1 到 100) 以品質為基礎的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="3c2bb-123">**g \_ wszVBRBitrateMax**</span><span class="sxs-lookup"><span data-stu-id="3c2bb-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="3c2bb-124">**DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-124">**DWORD** value.</span></span> <span data-ttu-id="3c2bb-125">針對限制的 VBR 編碼，設定為最大位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="3c2bb-126">**g \_ wszVBRBufferWindowMax**</span><span class="sxs-lookup"><span data-stu-id="3c2bb-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="3c2bb-127">**DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-127">**DWORD** value.</span></span> <span data-ttu-id="3c2bb-128">針對受限的 VBR 編碼設定為最大緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="3c2bb-129">下列各節說明如何使用不同類型的變數位速率編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="3c2bb-130">區段</span><span class="sxs-lookup"><span data-stu-id="3c2bb-130">Section</span></span>                                                              | <span data-ttu-id="3c2bb-131">描述</span><span class="sxs-lookup"><span data-stu-id="3c2bb-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c2bb-132">設定 Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="3c2bb-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="3c2bb-133">描述如何根據靜態品質等級來使用變數位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="3c2bb-134">設定未受限制的 VBR</span><span class="sxs-lookup"><span data-stu-id="3c2bb-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="3c2bb-135">描述如何根據目標平均位元速率（沒有明確的尖峰值）來使用變數位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="3c2bb-136">設定限制的 VBR</span><span class="sxs-lookup"><span data-stu-id="3c2bb-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="3c2bb-137">描述如何根據目標平均位元速率和明確尖峰值，來使用變數位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="3c2bb-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="3c2bb-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c2bb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c2bb-139">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="3c2bb-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




