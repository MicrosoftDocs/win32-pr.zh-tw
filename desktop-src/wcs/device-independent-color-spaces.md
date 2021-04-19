---
title: Device-Independent 色彩空間
description: 辨識標準、裝置與裝置無關的色彩測量需求、國際 de l'Eclairage (國際化委員會的照明) 或 CIE、根據 \ 0034 建立色彩空間、虛構 0034;原色。
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Color System (WCS) 、與裝置無關的色彩空間
- WCS (Windows 色彩系統) ，與裝置無關的色彩空間
- 影像色彩管理、與裝置無關的色彩空間
- 色彩管理、與裝置無關的色彩空間
- 色彩，與裝置無關的色彩空間
- 色彩空間、與裝置無關
- 與裝置無關的色彩空間
- L'Eclairage) 的委員會 (CIE
- '在照明上的國際委員會 (CIE) '
- "CIE (委員會國際 de l'Eclairage) "
- CIE (照明) 的國際委員會
- CIEXYZ 色彩空間
- XYZ 色彩空間
- sRGB 色彩空間
- 色彩空間、CIEXYZ
- 色彩空間、sRGB
- 色彩空間、XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106982125"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="9ad0f-120">Device-Independent 色彩空間</span><span class="sxs-lookup"><span data-stu-id="9ad0f-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="9ad0f-121">辨識標準、裝置與裝置無關的色彩測量的需求，國際 de l'Eclairage (國際化的照明) 或 CIE，根據「虛構」[主要色彩](p.md)建立[色彩空間](c.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="9ad0f-122">沒有實際的裝置預期會在此色彩空間中產生色彩。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="9ad0f-123">它是用來將色彩從某個色彩空間轉換成另一個色彩空間的方法。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="9ad0f-124">此色彩空間中的主要色彩為 X、Y 和 Z 的抽象色彩。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="9ad0f-125">1931 CIEXYZ 色彩空間已廣泛用來作為色彩空間轉換的基礎。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="9ad0f-126">不過，隨著網際網路的增加，頻寬的考慮使得 XYZ 色彩空間變得難以處理。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="9ad0f-127">透過網際網路的有限頻寬交換影像，會有更精簡的 [色彩模型](c.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="9ad0f-128">如此一來，Hewlett-Packard 和 Microsoft 已提議採用標準的預先定義 RGB 色彩空間，稱為 sRGB，因此可讓您以極少的資料負擔進行精確的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="9ad0f-129">這項標準已被核准為國際電子電機委員會 (IEC) 的正式國際標準，IEC 61966-2-1：多媒體系統和 EquipmentColour 測量，以及 ManagementPart 2-1：彩色 ManagementDefault RGB 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="9ad0f-130">您可以直接從 IEC 的取得 <https://www.iec.ch/> 。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="9ad0f-131">您可以從網際網路上的網際網路上，取得與 sRGB 相關的技術問題的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="9ad0f-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="9ad0f-132">適用于網際網路的標準預設色彩空間-sRGB</span><span class="sxs-lookup"><span data-stu-id="9ad0f-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="9ad0f-133">說明檔案版本的白皮書會討論 sRGB （sRGB）中所涉及的技術問題，可在「WCS 1.0 程式設計師」在 \\ PLATFORM SDK 中參考的說明資料夾中取得。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="9ad0f-134">不同的檔案格式可能會使用或新增旗標，以指定影像位於 sRGB 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="9ad0f-135">在與 Windows 裝置無關的點陣圖中 (DIB) 格式，將 [BITMAPV5HEADER](using-structures-in-wcs-1-0.md)結構的 **bV5CSType** 成員設定為 LCS \_ sRGB，會指定 DIB 色彩位於 sRGB 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="9ad0f-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




