---
title: 在裝置內容之外使用的 Advanced 函數
description: 這些函式會在裝置內容之外提供先進的色彩管理功能。
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04b7afe98f468fd3f580adf3eff145bce3aa1ac
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "107000506"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a><span data-ttu-id="8c530-110">在裝置內容之外使用的 Advanced 函數</span><span class="sxs-lookup"><span data-stu-id="8c530-110">Advanced Functions for Use Outside of a Device Context</span></span>

<span data-ttu-id="8c530-111">這些函式會在裝置內容之外提供先進的色彩管理功能。</span><span class="sxs-lookup"><span data-stu-id="8c530-111">These functions provide advanced color management capabilities outside of device contexts.</span></span>



| <span data-ttu-id="8c530-112">函式</span><span class="sxs-lookup"><span data-stu-id="8c530-112">Function</span></span>                                                           | <span data-ttu-id="8c530-113">描述</span><span class="sxs-lookup"><span data-stu-id="8c530-113">Description</span></span>                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c530-114">**PCMSCALLBACKW**</span><span class="sxs-lookup"><span data-stu-id="8c530-114">**PCMSCALLBACKW**</span></span>](/windows/win32/api/icm/nc-icm-pcmscallbackw) | <span data-ttu-id="8c530-115">\**PCMSCALLBACKW*\* (或 **ApplyCallbackFunction**) 是一種回呼函式，您會在執行 [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) 函式所顯示的對話方塊時，執行此函數來更新 WCS 設定資料。</span><span class="sxs-lookup"><span data-stu-id="8c530-115">\**PCMSCALLBACKW*\* (or **ApplyCallbackFunction**) is a callback function that you implement that updates the WCS configuration data while the dialog box displayed by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function is executing.</span></span> |
| [<span data-ttu-id="8c530-116">**CheckBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="8c530-116">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits) | <span data-ttu-id="8c530-117">檢查指定點陣圖中的圖元是否位於指定轉換 [的輸出範圍](g.md) 內。</span><span class="sxs-lookup"><span data-stu-id="8c530-117">Checks whether the pixels in a specified bitmap lie within the output [gamut](g.md) of a specified transform.</span></span> |
| [<span data-ttu-id="8c530-118">**CheckColors**</span><span class="sxs-lookup"><span data-stu-id="8c530-118">**CheckColors**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits) | <span data-ttu-id="8c530-119">判斷陣列中的色彩是否位於指定轉換 [的輸出範圍](g.md) 內。</span><span class="sxs-lookup"><span data-stu-id="8c530-119">Determines whether the colors in an array lie within the output [gamut](g.md) of a specified transform.</span></span> |
| [<span data-ttu-id="8c530-120">**ConvertColorNameToIndex**</span><span class="sxs-lookup"><span data-stu-id="8c530-120">**ConvertColorNameToIndex**</span></span>](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | <span data-ttu-id="8c530-121">將命名色彩空間中的色彩名稱轉換成 (ICC) 色彩設定檔的國際色彩協會中的索引編號。</span><span class="sxs-lookup"><span data-stu-id="8c530-121">Converts color names in a named color space to index numbers in an International Color Consortium (ICC) color profile.</span></span> |
| [<span data-ttu-id="8c530-122">**ConvertIndexToColorName**</span><span class="sxs-lookup"><span data-stu-id="8c530-122">**ConvertIndexToColorName**</span></span>](/windows/win32/api/icm/nf-icm-convertindextocolorname) | <span data-ttu-id="8c530-123">將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="8c530-123">Transforms indices in a color space to an array of names in a named color space.</span></span> |
| [<span data-ttu-id="8c530-124">**CreateColorTransformW**</span><span class="sxs-lookup"><span data-stu-id="8c530-124">**CreateColorTransformW**</span></span>](/windows/win32/api/icm/nf-icm-createcolortransformw) | <span data-ttu-id="8c530-125">將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="8c530-125">Transforms indices in a color space to an array of names in a named color space.</span></span> |
| [<span data-ttu-id="8c530-126">**CreateMultiProfileTransform**</span><span class="sxs-lookup"><span data-stu-id="8c530-126">**CreateMultiProfileTransform**</span></span>](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | <span data-ttu-id="8c530-127">接受設定檔的陣列或單一 [裝置連結設定檔](d.md) ，並建立應用程式可用來執行色彩對應的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="8c530-127">Accepts an array of profiles or a single [device link profile](d.md) and creates a color transform that applications can use to perform color mapping.</span></span> |
| [<span data-ttu-id="8c530-128">**DeleteColorTransform**</span><span class="sxs-lookup"><span data-stu-id="8c530-128">**DeleteColorTransform**</span></span>](/windows/win32/api/icm/nf-icm-deletecolortransform) | <span data-ttu-id="8c530-129">刪除指定的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="8c530-129">Deletes a given color transform.</span></span> |
| [<span data-ttu-id="8c530-130">**GetCMMInfo**</span><span class="sxs-lookup"><span data-stu-id="8c530-130">**GetCMMInfo**</span></span>](/windows/win32/api/icm/nf-icm-getcmminfo) | <span data-ttu-id="8c530-131">抓取有關建立指定的色彩轉換 (CMM) 之色彩管理模組的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="8c530-131">Retrieves various information about the color management module (CMM) that created the specified color transform.</span></span> |
| [<span data-ttu-id="8c530-132">**GetNamedProfileInfo**</span><span class="sxs-lookup"><span data-stu-id="8c530-132">**GetNamedProfileInfo**</span></span>](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | <span data-ttu-id="8c530-133">抓取第一個參數中所指定的「國際色彩協會」 (ICC) 命名色彩設定檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c530-133">Retrieves information about the International Color Consortium (ICC) named color profile that is specified in the first parameter.</span></span> |
| [<span data-ttu-id="8c530-134">**ICMProgressProcCallback**</span><span class="sxs-lookup"><span data-stu-id="8c530-134">**ICMProgressProcCallback**</span></span>](icmprogressproccallback.md)         | <span data-ttu-id="8c530-135">用來報告進度的應用程式提供回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8c530-135">Application-supplied callback function to report progress.</span></span> <span data-ttu-id="8c530-136">這個函式的名稱也是由應用程式所定義。</span><span class="sxs-lookup"><span data-stu-id="8c530-136">The name of this function is also defined by the application.</span></span>                                                 |
| [<span data-ttu-id="8c530-137">**SelectCMM**</span><span class="sxs-lookup"><span data-stu-id="8c530-137">**SelectCMM**</span></span>](/windows/win32/api/icm/nf-icm-selectcmm) | <span data-ttu-id="8c530-138">可讓您選取慣用的色彩管理模組 (要使用的 CMM) 。</span><span class="sxs-lookup"><span data-stu-id="8c530-138">Allows you to select the preferred color management module (CMM) to use.</span></span> |
| [<span data-ttu-id="8c530-139">**SetupColorMatchingW**</span><span class="sxs-lookup"><span data-stu-id="8c530-139">**SetupColorMatchingW**</span></span>](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | <span data-ttu-id="8c530-140">以對話方塊的方式，提供使用者控制項的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="8c530-140">Provides user control over color management by way of a dialog box.</span></span>                                                                                                      |
| [<span data-ttu-id="8c530-141">**TranslateBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="8c530-141">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | <span data-ttu-id="8c530-142">使用色彩轉換來轉換點陣圖色彩。</span><span class="sxs-lookup"><span data-stu-id="8c530-142">Converts bitmap colors using a color transform.</span></span>                                                                                                                          |
| [<span data-ttu-id="8c530-143">**TranslateColors**</span><span class="sxs-lookup"><span data-stu-id="8c530-143">**TranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-translatecolors) | <span data-ttu-id="8c530-144">將色彩的陣列從來源 [色彩空間](c.md) 轉譯為目的色彩空間，如色彩轉換所定義。</span><span class="sxs-lookup"><span data-stu-id="8c530-144">Translates an array of colors from the source [color space](c.md) to the destination color space as defined by a color transform.</span></span> |
| [<span data-ttu-id="8c530-145">**WcsCheckColors**</span><span class="sxs-lookup"><span data-stu-id="8c530-145">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | <span data-ttu-id="8c530-146">判斷陣列中的色彩是否在指定之 WCS 色彩轉換的輸出範圍內。</span><span class="sxs-lookup"><span data-stu-id="8c530-146">Determines whether the colors in an array are within the output gamut of a specified WCS color transform.</span></span>                                                                |
| [<span data-ttu-id="8c530-147">**WcsTranslateColors**</span><span class="sxs-lookup"><span data-stu-id="8c530-147">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | <span data-ttu-id="8c530-148">將色彩的陣列從來源色彩空間轉譯為目的色彩空間，如色彩轉換所定義。</span><span class="sxs-lookup"><span data-stu-id="8c530-148">Translates an array of colors from the source color space to the destination color space as defined by a color transform.</span></span>                                                |



 

 

 




