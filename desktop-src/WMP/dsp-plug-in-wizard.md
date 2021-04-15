---
title: DSP 外掛程式嚮導
description: DSP 外掛程式嚮導
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Windows Media Player 外掛程式，外掛程式嚮導
- 外掛程式、外掛程式嚮導
- 數位信號處理外掛程式，外掛程式嚮導
- DSP 外掛程式，外掛程式嚮導
- 外掛程式嚮導
- Visual Studio，DSP 外掛程式 wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507185"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="d4244-109">DSP 外掛程式嚮導</span><span class="sxs-lookup"><span data-stu-id="d4244-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="d4244-110">Windows Media Player SDK 提供可讓您新增至 Visual Studio 的外掛程式 wizard。</span><span class="sxs-lookup"><span data-stu-id="d4244-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="d4244-111">Wizard 可以產生各種外掛程式的範例程式碼，包括下列類型的 DSP 外掛程式：</span><span class="sxs-lookup"><span data-stu-id="d4244-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="d4244-112">音訊 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="d4244-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="d4244-113">音訊 DSP 外掛程式 (雙重模式) </span><span class="sxs-lookup"><span data-stu-id="d4244-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="d4244-114">影片 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="d4244-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="d4244-115"> (雙重模式的影片 DSP 外掛程式) </span><span class="sxs-lookup"><span data-stu-id="d4244-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="d4244-116">這兩個基本的範例外掛程式（音訊 DSP 和 Video DSP）都會以 DirectX 媒體物件的形式運作， (的) 。</span><span class="sxs-lookup"><span data-stu-id="d4244-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="d4244-117">也就是說，每個範例外掛程式都會執行 **IMediaObject** 介面。</span><span class="sxs-lookup"><span data-stu-id="d4244-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="d4244-118">這兩個雙重模式範例外掛程式的每一個都可以做為一或媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="d4244-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="d4244-119">也就是說，每個雙重模式的範例外掛程式都會同時執行 **IMediaObject** 介面和 **IMFTransform** 介面。</span><span class="sxs-lookup"><span data-stu-id="d4244-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="d4244-120">您可以編譯、連結、註冊和測試範例外掛程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="d4244-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="d4244-121">然後您可以修改產生的範例程式碼，以建立您自己的 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="d4244-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4244-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4244-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4244-123">**建立 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="d4244-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="d4244-124">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="d4244-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="d4244-125">**Windows Media Player 11 的 DSP 外掛程式嚮導更新**</span><span class="sxs-lookup"><span data-stu-id="d4244-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




