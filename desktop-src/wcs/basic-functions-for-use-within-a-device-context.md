---
title: 在裝置內容中使用的基本函數
description: 下列 WCS 函數會在裝置內容中提供基本的色彩對應功能。 這些應用程式對於所有需要以低額外負荷來執行色彩管理的應用程式，以及最少的使用者介入都很有用。
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- Windows Color System (WCS) 、裝置內容
- WCS (Windows 色彩系統) 、裝置內容
- 影像色彩管理、裝置內容
- 色彩管理，裝置內容
- 色彩、裝置內容
- WCS 參考，裝置內容
- WCS、裝置內容的參考
- 裝置內容
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "106993765"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="df2a0-119">在裝置內容中使用的基本函數</span><span class="sxs-lookup"><span data-stu-id="df2a0-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="df2a0-120">下列 WCS 函數會在裝置內容中提供基本的 [色彩對應](c.md) 功能。</span><span class="sxs-lookup"><span data-stu-id="df2a0-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="df2a0-121">這些應用程式對於所有需要以低額外負荷來執行色彩管理的應用程式，以及最少的使用者介入都很有用。</span><span class="sxs-lookup"><span data-stu-id="df2a0-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="df2a0-122">函式</span><span class="sxs-lookup"><span data-stu-id="df2a0-122">Function</span></span>                                                           | <span data-ttu-id="df2a0-123">描述</span><span class="sxs-lookup"><span data-stu-id="df2a0-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df2a0-124">**CheckColorsInGamut**</span><span class="sxs-lookup"><span data-stu-id="df2a0-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="df2a0-125">檢查指定的色彩是否在裝置的範圍中。</span><span class="sxs-lookup"><span data-stu-id="df2a0-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="df2a0-126">**ColorCorrectPalette**</span><span class="sxs-lookup"><span data-stu-id="df2a0-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="df2a0-127">更正裝置內容之調色板中的專案。</span><span class="sxs-lookup"><span data-stu-id="df2a0-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="df2a0-128">**ColorMatchToTarget**</span><span class="sxs-lookup"><span data-stu-id="df2a0-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="df2a0-129">針對預覽用途執行色彩對應。</span><span class="sxs-lookup"><span data-stu-id="df2a0-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="df2a0-130">**CreateColorSpace**</span><span class="sxs-lookup"><span data-stu-id="df2a0-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="df2a0-131">建立色彩空間。</span><span class="sxs-lookup"><span data-stu-id="df2a0-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="df2a0-132">**DeleteColorSpace**</span><span class="sxs-lookup"><span data-stu-id="df2a0-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="df2a0-133">刪除色彩空間。</span><span class="sxs-lookup"><span data-stu-id="df2a0-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="df2a0-134">**EnumICMProfiles**</span><span class="sxs-lookup"><span data-stu-id="df2a0-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="df2a0-135">列舉適用于指定之裝置內容的輸出色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="df2a0-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="df2a0-136">**EnumICMProfilesProcCallback**</span><span class="sxs-lookup"><span data-stu-id="df2a0-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="df2a0-137">[**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="df2a0-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="df2a0-138">這個函式的名稱也是由應用程式所定義。</span><span class="sxs-lookup"><span data-stu-id="df2a0-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="df2a0-139">**GetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="df2a0-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="df2a0-140">取得裝置內容中目前的輸入色彩空間。</span><span class="sxs-lookup"><span data-stu-id="df2a0-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="df2a0-141">**GetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="df2a0-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="df2a0-142">取得裝置內容目前的輸出色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="df2a0-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="df2a0-143">**GetLogColorSpace**</span><span class="sxs-lookup"><span data-stu-id="df2a0-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="df2a0-144">取得裝置內容的 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) 結構。</span><span class="sxs-lookup"><span data-stu-id="df2a0-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="df2a0-145">**SetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="df2a0-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="df2a0-146">設定裝置內容的輸入色彩空間。</span><span class="sxs-lookup"><span data-stu-id="df2a0-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="df2a0-147">**SetICMMode**</span><span class="sxs-lookup"><span data-stu-id="df2a0-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="df2a0-148">在裝置內容中開啟或關閉色彩管理。</span><span class="sxs-lookup"><span data-stu-id="df2a0-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="df2a0-149">**SetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="df2a0-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="df2a0-150">設定指定之裝置內容的輸出色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="df2a0-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="df2a0-151">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="df2a0-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="df2a0-152">列舉符合指定設定檔管理範圍中的列舉準則的所有色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="df2a0-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




