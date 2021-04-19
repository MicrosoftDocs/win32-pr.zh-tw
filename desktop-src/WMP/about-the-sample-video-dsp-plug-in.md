---
title: 關於範例影片 DSP 外掛程式
description: 關於範例影片 DSP 外掛程式
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Windows Media Player 外掛程式，範例
- 外掛程式，範例
- 數位信號處理外掛程式，範例
- DSP 外掛程式，範例
- Windows Media Player 外掛程式、影片 DSP
- 外掛程式、視頻 DSP
- 數位信號處理外掛程式、影片範例
- DSP 外掛程式、影片範例
- 範例，DSP 外掛程式
- 影片 DSP 外掛程式、範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966176"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="a351d-113">關於範例影片 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="a351d-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="a351d-114">範例影片 DSP 外掛程式提供簡單的處理常式，可根據使用者在屬性頁中提供的因素來調整影片的色彩飽和度。</span><span class="sxs-lookup"><span data-stu-id="a351d-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="a351d-115">外掛程式接受介於0和1之間的值。</span><span class="sxs-lookup"><span data-stu-id="a351d-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="a351d-116">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="a351d-116">The default value is 1.</span></span> <span data-ttu-id="a351d-117">值為1時，不會影響影片影像;其他比例因素會反滲透影像色彩。</span><span class="sxs-lookup"><span data-stu-id="a351d-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="a351d-118">例如，值 .5 會導致50% 的色彩飽和度。</span><span class="sxs-lookup"><span data-stu-id="a351d-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="a351d-119">零的值會產生灰階影片。</span><span class="sxs-lookup"><span data-stu-id="a351d-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="a351d-120">範例影片 DSP 外掛程式適用于下列影片格式：</span><span class="sxs-lookup"><span data-stu-id="a351d-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="a351d-121">NV12</span><span class="sxs-lookup"><span data-stu-id="a351d-121">NV12</span></span>
-   <span data-ttu-id="a351d-122">YV12</span><span class="sxs-lookup"><span data-stu-id="a351d-122">YV12</span></span>
-   <span data-ttu-id="a351d-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="a351d-123">YUY2</span></span>
-   <span data-ttu-id="a351d-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="a351d-124">UYVY</span></span>
-   <span data-ttu-id="a351d-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="a351d-125">RGB32</span></span>
-   <span data-ttu-id="a351d-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="a351d-126">RGB24</span></span>
-   <span data-ttu-id="a351d-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="a351d-127">RGB555</span></span>
-   <span data-ttu-id="a351d-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="a351d-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="a351d-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a351d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a351d-130">**建立 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="a351d-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




