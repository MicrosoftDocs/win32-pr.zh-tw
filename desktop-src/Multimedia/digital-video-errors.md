---
title: Digital-Video 錯誤
description: Digital-Video 錯誤
ms.assetid: 177436fc-543f-4692-8281-1555c1fa21b0
keywords:
- MCIERR 傳回值、數位視訊錯誤
- 多媒體參考、數位視訊錯誤
- 多媒體、數位視訊錯誤的參考
- 媒體控制介面 (MCI) 、數位影片錯誤
- MCI (媒體控制介面) 、數位影片錯誤
- MCI 的參考、數位視訊錯誤
- MCI 參考、數位視訊錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- 數位影片錯誤
- MCI 數位-影片錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6938330d15777ed867bf7d151a9d626e60b28646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675016"
---
# <a name="digital-video-errors"></a><span data-ttu-id="9881d-116">Digital-Video 錯誤</span><span class="sxs-lookup"><span data-stu-id="9881d-116">Digital-Video Errors</span></span>

<span data-ttu-id="9881d-117">數位視訊裝置會定義下列額外的傳回值：</span><span class="sxs-lookup"><span data-stu-id="9881d-117">The following additional return values are defined for digital-video devices:</span></span>



| <span data-ttu-id="9881d-118">值</span><span class="sxs-lookup"><span data-stu-id="9881d-118">Value</span></span>                           | <span data-ttu-id="9881d-119">意義</span><span class="sxs-lookup"><span data-stu-id="9881d-119">Meaning</span></span>                                                         |
|---------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9881d-120">MCIAVI \_ PRODUCTNAME</span><span class="sxs-lookup"><span data-stu-id="9881d-120">MCIAVI\_PRODUCTNAME</span></span>             | <span data-ttu-id="9881d-121">影片</span><span class="sxs-lookup"><span data-stu-id="9881d-121">Video</span></span>                                                           |
| <span data-ttu-id="9881d-122">MCIERR \_ AVI \_ AUDIOERROR</span><span class="sxs-lookup"><span data-stu-id="9881d-122">MCIERR\_AVI\_AUDIOERROR</span></span>         | <span data-ttu-id="9881d-123">嘗試播放音訊時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9881d-123">Unknown error while attempting to play audio.</span></span>                   |
| <span data-ttu-id="9881d-124">MCIERR \_ AVI \_ BADPALETTE</span><span class="sxs-lookup"><span data-stu-id="9881d-124">MCIERR\_AVI\_BADPALETTE</span></span>         | <span data-ttu-id="9881d-125">無法切換至新的調色板。</span><span class="sxs-lookup"><span data-stu-id="9881d-125">Unable to switch to new palette.</span></span>                                |
| <span data-ttu-id="9881d-126">MCIERR \_ AVI \_ CANTPLAYFULLSCREEN</span><span class="sxs-lookup"><span data-stu-id="9881d-126">MCIERR\_AVI\_CANTPLAYFULLSCREEN</span></span> | <span data-ttu-id="9881d-127">此 AVI 檔案無法在全螢幕模式中播放。</span><span class="sxs-lookup"><span data-stu-id="9881d-127">This AVI file cannot be played in full screen mode.</span></span>             |
| <span data-ttu-id="9881d-128">MCIERR \_ AVI \_ DISPLAYERROR</span><span class="sxs-lookup"><span data-stu-id="9881d-128">MCIERR\_AVI\_DISPLAYERROR</span></span>       | <span data-ttu-id="9881d-129">嘗試顯示影片時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9881d-129">Unknown error while attempting to display video.</span></span>                |
| <span data-ttu-id="9881d-130">MCIERR \_ AVI \_ NOCOMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="9881d-130">MCIERR\_AVI\_NOCOMPRESSOR</span></span>       | <span data-ttu-id="9881d-131">找不到播放此檔案所需的可安裝壓縮檔。</span><span class="sxs-lookup"><span data-stu-id="9881d-131">Can't locate installable compressor needed to play this file.</span></span>   |
| <span data-ttu-id="9881d-132">MCIERR \_ AVI \_ NODISPDIB</span><span class="sxs-lookup"><span data-stu-id="9881d-132">MCIERR\_AVI\_NODISPDIB</span></span>          | <span data-ttu-id="9881d-133">256無法使用 color VGA 模式。</span><span class="sxs-lookup"><span data-stu-id="9881d-133">256 color VGA mode not available.</span></span>                               |
| <span data-ttu-id="9881d-134">MCIERR \_ AVI \_ NOTINTERLEAVED</span><span class="sxs-lookup"><span data-stu-id="9881d-134">MCIERR\_AVI\_NOTINTERLEAVED</span></span>     | <span data-ttu-id="9881d-135">這個 AVI 檔案不是交錯的。</span><span class="sxs-lookup"><span data-stu-id="9881d-135">This AVI file is not interleaved.</span></span>                               |
| <span data-ttu-id="9881d-136">MCIERR \_ AVI \_ OLDAVIFORMAT</span><span class="sxs-lookup"><span data-stu-id="9881d-136">MCIERR\_AVI\_OLDAVIFORMAT</span></span>       | <span data-ttu-id="9881d-137">此 AVI 檔案的格式為過時。</span><span class="sxs-lookup"><span data-stu-id="9881d-137">This AVI file is of an obsolete format.</span></span>                         |
| <span data-ttu-id="9881d-138">MCIERR \_ AVI \_ TOOBIGFORVGA</span><span class="sxs-lookup"><span data-stu-id="9881d-138">MCIERR\_AVI\_TOOBIGFORVGA</span></span>       | <span data-ttu-id="9881d-139">這個 AVI 檔案太大，無法在選取的 VGA 模式下播放。</span><span class="sxs-lookup"><span data-stu-id="9881d-139">This AVI file is too big to be played in the selected VGA mode.</span></span> |



 

 

 




