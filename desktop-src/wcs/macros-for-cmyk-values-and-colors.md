---
title: CMYK 值和色彩的宏
description: 下列宏在操作 CMYK 值時很有用。
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS) 、CMYK 宏
- WCS (Windows Color System) 、CMYK 宏
- 影像色彩管理、CMYK 宏
- 色彩管理、CMYK 宏
- 色彩、CMYK 宏
- WCS 參考，CMYK 宏
- WCS、CMYK 宏的參考
- CMYK 宏
- '青色洋紅色黃色黑色 (CMYK) '
- 'CMYK (青色洋黃色黑色) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106981909"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="19d5c-113">CMYK 值和色彩的宏</span><span class="sxs-lookup"><span data-stu-id="19d5c-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="19d5c-114">下列宏在操作 CMYK 值時很有用。</span><span class="sxs-lookup"><span data-stu-id="19d5c-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="19d5c-115">巨集</span><span class="sxs-lookup"><span data-stu-id="19d5c-115">Macro</span></span>                          | <span data-ttu-id="19d5c-116">Description</span><span class="sxs-lookup"><span data-stu-id="19d5c-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="19d5c-117">**Cmyk**</span><span class="sxs-lookup"><span data-stu-id="19d5c-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="19d5c-118">從個別的青色、洋紅、黃色和黑色值建立 CMYK 值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="19d5c-119">**GetCValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="19d5c-120">從 CMYK 色彩值抓取青色色彩值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="19d5c-121">**GetKValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="19d5c-122">從 CMYK 色彩值抓取黑色色彩值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="19d5c-123">**GetMValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="19d5c-124">從 CMYK 色彩值抓取洋紅值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="19d5c-125">**GetYValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="19d5c-126">從 CMYK 色彩值抓取黃色的色彩值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="19d5c-127">下列宏會搭配色彩使用。</span><span class="sxs-lookup"><span data-stu-id="19d5c-127">The following macros are used with color.</span></span>



| <span data-ttu-id="19d5c-128">巨集</span><span class="sxs-lookup"><span data-stu-id="19d5c-128">Macro</span></span>                                | <span data-ttu-id="19d5c-129">Description</span><span class="sxs-lookup"><span data-stu-id="19d5c-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19d5c-130">**GetBValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="19d5c-131">取得 RGB 藍色值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="19d5c-132">**GetGValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="19d5c-133">取得 RGB 綠值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="19d5c-134">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="19d5c-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="19d5c-135">取得 RGB 紅色值。</span><span class="sxs-lookup"><span data-stu-id="19d5c-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="19d5c-136">[**調色盤索引**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19d5c-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="19d5c-137">接受邏輯色彩調色板專案的索引，並傳回檔色板輸入規範。</span><span class="sxs-lookup"><span data-stu-id="19d5c-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="19d5c-138">**PALETTERGB**</span><span class="sxs-lookup"><span data-stu-id="19d5c-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="19d5c-139">接受代表紅色、綠色和藍色之相對濃度的三個值，並傳回與調色板相關的紅色、綠色、藍色 (RGB) 規範。</span><span class="sxs-lookup"><span data-stu-id="19d5c-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="19d5c-140">RGB</span><span class="sxs-lookup"><span data-stu-id="19d5c-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="19d5c-141">根據提供的引數和輸出裝置的色彩功能，選取紅色、綠色、藍色 (RGB) 色彩。</span><span class="sxs-lookup"><span data-stu-id="19d5c-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 