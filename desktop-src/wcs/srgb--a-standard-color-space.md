---
title: sRGB 標準色彩空間
description: 由於網際網路頻寬的考慮，Hewlett-Packard 和 Microsoft 已建議採用標準的預先定義色彩空間，稱為 sRGB (IEC 61966-2-1) ，因此可讓您以極少的資料負擔進行精確的色彩對應。
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS) 、sRGB 色彩空間
- WCS (Windows 色彩系統) 、sRGB 色彩空間
- 影像色彩管理、sRGB 色彩空間
- 色彩管理、sRGB 色彩空間
- 色彩、sRGB 色彩空間
- sRGB 色彩空間
- 色彩空間、sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2021
ms.locfileid: "107000340"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="ab913-110">sRGB：標準色彩空間</span><span class="sxs-lookup"><span data-stu-id="ab913-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="ab913-111">由於網際網路頻寬的考慮，Hewlett-Packard 和 Microsoft 已建議採用標準的預先定義 [色彩空間](c.md) ，稱為 *sRGB* (IEC 61966-2-1) ，因此可讓您以極少的資料負擔進行精確的 [色彩對應](c.md) 。</span><span class="sxs-lookup"><span data-stu-id="ab913-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="ab913-112">您可以在 WCS 1.0 程式設計人員參考的 [說明] 資料夾中，找到可討論 sRGB （sRGB）技術詳細資料的白皮書說明文件版本 \\ 。</span><span class="sxs-lookup"><span data-stu-id="ab913-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="ab913-113">不同的檔案格式可能會使用或新增旗標，以指定影像位於 sRGB 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="ab913-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="ab913-114">在與 Windows 裝置無關的點陣圖中 (DIB) 格式，將 [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md)結構的 **bV5CSType** 成員設定為 **LCS \_ sRGB** ，會指定 DIB 色彩位於 sRGB 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="ab913-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="ab913-115">WCS 1.0 提供 sRGB 的原生支援。</span><span class="sxs-lookup"><span data-stu-id="ab913-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="ab913-116">有兩種方式可以使用 WCS 1.0 來轉譯定義于 sRGB 色彩空間中的影像：</span><span class="sxs-lookup"><span data-stu-id="ab913-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="ab913-117">**在裝置內容中呈現影像**</span><span class="sxs-lookup"><span data-stu-id="ab913-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="ab913-118">在顯示裝置上 (DC) 建立裝置內容。</span><span class="sxs-lookup"><span data-stu-id="ab913-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="ab913-119">使用 [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) 函數設定色彩管理。</span><span class="sxs-lookup"><span data-stu-id="ab913-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="ab913-120">使用 [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) 函式，將 DIB 傳送至 DC。</span><span class="sxs-lookup"><span data-stu-id="ab913-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="ab913-121">只要 Dib [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md)結構的 **bV5CSMType** 成員設定為 **LCS \_ sRGB**，系統就會執行適當的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="ab913-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="ab913-122">**若要在裝置內容外部呈現影像**</span><span class="sxs-lookup"><span data-stu-id="ab913-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="ab913-123">使用 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw)建立轉換。</span><span class="sxs-lookup"><span data-stu-id="ab913-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="ab913-124">*PLogColorSpace* 參數所指向之 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)結構的 **LcsCSType** 成員應設定為 **LCS \_ sRGB**。</span><span class="sxs-lookup"><span data-stu-id="ab913-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="ab913-125">*HDestProfile* 參數會指出顯示裝置的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="ab913-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="ab913-126">在裝置上顯示影像之前，請先使用已建立的色彩轉換來將影像色彩符合。</span><span class="sxs-lookup"><span data-stu-id="ab913-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="ab913-127">輸入色彩空間和輸出設定檔的 WCS 1.0 預設值</span><span class="sxs-lookup"><span data-stu-id="ab913-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="ab913-128">未指定任何輸入色彩空間時，根據預設，WCS 1.0 會使用 sRGB 色彩空間作為 [色彩對應](c.md)的輸入色彩空間。</span><span class="sxs-lookup"><span data-stu-id="ab913-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="ab913-129">如果未指定輸出設定檔，但指定了預設裝置，則 WCS 1.0 會選取預設的輸出設定檔。</span><span class="sxs-lookup"><span data-stu-id="ab913-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="ab913-130">如果預設裝置沒有相關聯的設定檔，則 WCS 1.0 會使用 sRGB 色彩空間作為輸出設定檔。</span><span class="sxs-lookup"><span data-stu-id="ab913-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="ab913-131">下表顯示當預設裝置無法使用時，所產生的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="ab913-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|                                 | <span data-ttu-id="ab913-132">指定的輸出設定檔</span><span class="sxs-lookup"><span data-stu-id="ab913-132">Output Profile Specified</span></span>                              | <span data-ttu-id="ab913-133">未指定輸出設定檔</span><span class="sxs-lookup"><span data-stu-id="ab913-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ab913-134">指定的輸入色彩空間</span><span class="sxs-lookup"><span data-stu-id="ab913-134">Input Color Space Specified</span></span>     | <span data-ttu-id="ab913-135">轉換會使用指定的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ab913-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="ab913-136">轉換會從已知的輸入色彩空間轉換成 sRGB。</span><span class="sxs-lookup"><span data-stu-id="ab913-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="ab913-137">未指定輸入色彩空間</span><span class="sxs-lookup"><span data-stu-id="ab913-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="ab913-138">轉換會從 sRGB 轉換成已知的輸出設定檔。</span><span class="sxs-lookup"><span data-stu-id="ab913-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="ab913-139">假設是從 sRGB 轉換成 sRGB，未完成任何動作。</span><span class="sxs-lookup"><span data-stu-id="ab913-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="ab913-140">sRGB 和 Embedded 設定檔</span><span class="sxs-lookup"><span data-stu-id="ab913-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="ab913-141">從 ICM 版本2.0 開始，利用 WCS 的應用程式可以將設定檔內嵌于映射中。</span><span class="sxs-lookup"><span data-stu-id="ab913-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="ab913-142">內嵌設定檔可協助使用者的應用程式維持一致的色彩外觀，即使影像是經由網際網路傳輸亦同。</span><span class="sxs-lookup"><span data-stu-id="ab913-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="ab913-143">使用 sRGB 色彩空間的影像不需要內嵌色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="ab913-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="ab913-144">因為它們沒有內嵌的設定檔，所以在頻寬有限的資料通道之間，以 sRGB 為基礎的映射較小且更容易轉移。</span><span class="sxs-lookup"><span data-stu-id="ab913-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="ab913-145">應用程式應在影像的點陣圖標頭中設定 **LCS \_ sRGB** ，以指出影像使用 sRGB 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="ab913-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="ab913-146">如需詳細資訊，請參閱 [Windows 點陣圖標頭結構](using-structures-in-wcs-1-0.md) 和 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)。</span><span class="sxs-lookup"><span data-stu-id="ab913-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 