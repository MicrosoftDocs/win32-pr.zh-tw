---
title: Device-Dependent 色彩空間
description: 大部分的色彩空間都與裝置相依。
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Color System (WCS) 、裝置相關的色彩空間
- WCS (Windows 色彩系統) ，與裝置相關的色彩空間
- 影像色彩管理、裝置相關的色彩空間
- 色彩管理、裝置相關的色彩空間
- 色彩、裝置相關的色彩空間
- 色彩空間、裝置相依
- 裝置相關的色彩空間
- 白色點
- 著色 劑
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106986421"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="0116f-112">Device-Dependent 色彩空間</span><span class="sxs-lookup"><span data-stu-id="0116f-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="0116f-113">大部分的 [色彩空間](c.md) 都與裝置相依。</span><span class="sxs-lookup"><span data-stu-id="0116f-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="0116f-114">雖然特定裝置（例如印表機）可能會使用 CMYK 色彩空間，但針對特定 CMYK 值轉譯的色彩通常會與其他所有類型的印表機稍微不同。</span><span class="sxs-lookup"><span data-stu-id="0116f-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="0116f-115">這是因為 WCS 1.0 色彩管理系統很有用。</span><span class="sxs-lookup"><span data-stu-id="0116f-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="0116f-116">所有色彩空間都有一個 *白色點*，其定義為可在該色彩空間中產生的 whitest 白色。</span><span class="sxs-lookup"><span data-stu-id="0116f-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="0116f-117">由於裝置可以彼此不同，因此其重點也可能不同。</span><span class="sxs-lookup"><span data-stu-id="0116f-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="0116f-118">裝置可以產生的所有色彩都是相對於其白點。</span><span class="sxs-lookup"><span data-stu-id="0116f-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="0116f-119">因此，色彩管理系統必須能夠將某個色彩空間的白色點對應到另一個色彩空間，並保留所有色彩的相對位置。</span><span class="sxs-lookup"><span data-stu-id="0116f-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="0116f-120">它也必須能夠將某個色彩空間中的色彩對應到另一個色彩空間中最接近的相符，而不論這些點之間的差異。</span><span class="sxs-lookup"><span data-stu-id="0116f-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="0116f-121">WCS 1.0 能夠完成這兩項工作。</span><span class="sxs-lookup"><span data-stu-id="0116f-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="0116f-122">RGB 色彩空間通常用於電腦監視器。</span><span class="sxs-lookup"><span data-stu-id="0116f-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="0116f-123">因此，它會相依于裝置。</span><span class="sxs-lookup"><span data-stu-id="0116f-123">As such, it is device dependent.</span></span> <span data-ttu-id="0116f-124">印表機通常會使用 CMYK [colorants](c.md)。</span><span class="sxs-lookup"><span data-stu-id="0116f-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="0116f-125">每部印表機都會執行自己的 CMYK 色彩空間版本。</span><span class="sxs-lookup"><span data-stu-id="0116f-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="0116f-126">數位影像可能不會實際儲存色彩。</span><span class="sxs-lookup"><span data-stu-id="0116f-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="0116f-127">它們可能會將索引編號儲存在色彩的調色板中。</span><span class="sxs-lookup"><span data-stu-id="0116f-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="0116f-128">結果是，個別的應用程式開發人員很難使用或提供標準化的方法，將色彩影像從某個裝置移到另一個裝置。</span><span class="sxs-lookup"><span data-stu-id="0116f-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="0116f-129">影像專家通常會經歷在電腦螢幕上建立圖形影像，並讓它在列印時以非常不同的方式開啟的挫折。</span><span class="sxs-lookup"><span data-stu-id="0116f-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="0116f-130">WCS 1.0 滿足這些映射需求。</span><span class="sxs-lookup"><span data-stu-id="0116f-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




