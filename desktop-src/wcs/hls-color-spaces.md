---
title: HLS 色彩空間
description: HLS 色彩空間也會由演出者廣泛使用。 其色彩元件為色調、亮度和飽和度 (色度) 。
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Windows Color System (WCS) ，HLS 色彩空間
- WCS (Windows 色彩系統) ，HLS 色彩空間
- 影像色彩管理、HLS 色彩空間
- 色彩管理，HLS 色彩空間
- 色彩，HLS 色彩空間
- 色彩空間、HLS
- HLS 色彩空間
- 色調
- 飽和
- 亮度
- 零飽和度
- '色調亮度飽和度 (HLS) '
- 'HLS (色調亮度飽和度) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106985173"
---
# <a name="hls-color-spaces"></a><span data-ttu-id="0db3a-117">HLS 色彩空間</span><span class="sxs-lookup"><span data-stu-id="0db3a-117">HLS Color Spaces</span></span>

<span data-ttu-id="0db3a-118">HLS [色彩空間](c.md) 也會由演出者廣泛使用。</span><span class="sxs-lookup"><span data-stu-id="0db3a-118">HLS [color spaces](c.md) are also widely used by artists.</span></span> <span data-ttu-id="0db3a-119">其色彩元件為色調、亮度和飽和度 (色度) 。</span><span class="sxs-lookup"><span data-stu-id="0db3a-119">Its color components are hue, lightness, and saturation (chroma).</span></span>

<span data-ttu-id="0db3a-120">色調與 HSV 模型具有相同的意義，但在此模型中，色調角度0會對應到藍色。</span><span class="sxs-lookup"><span data-stu-id="0db3a-120">Hue has the same meaning as the HSV model, except that a hue angle of 0 corresponds to blue in this model.</span></span> <span data-ttu-id="0db3a-121">洋紅色在60，紅色是120。</span><span class="sxs-lookup"><span data-stu-id="0db3a-121">Magenta is at 60, red is at 120.</span></span> <span data-ttu-id="0db3a-122">就像 HSV 模型一樣，互補色彩也是180。</span><span class="sxs-lookup"><span data-stu-id="0db3a-122">As with the HSV model, complementary colors are 180 apart.</span></span>

<span data-ttu-id="0db3a-123">亮度是色彩中的黑色或白色的量。</span><span class="sxs-lookup"><span data-stu-id="0db3a-123">Lightness is the amount of black or white in a color.</span></span> <span data-ttu-id="0db3a-124">提高亮度可將白色增加到色調。</span><span class="sxs-lookup"><span data-stu-id="0db3a-124">Increasing lightness adds white to the hue.</span></span> <span data-ttu-id="0db3a-125">減少亮度會將黑色增加到色調。</span><span class="sxs-lookup"><span data-stu-id="0db3a-125">Decreasing lightness adds black to the hue.</span></span>

<span data-ttu-id="0db3a-126">HLS 模型中的[飽和度](s.md)是色調的「純度」量值。</span><span class="sxs-lookup"><span data-stu-id="0db3a-126">[Saturation](s.md) in the HLS model is a measure of the "purity" of a hue.</span></span> <span data-ttu-id="0db3a-127">當飽和度減少時，色調會變得更灰色。</span><span class="sxs-lookup"><span data-stu-id="0db3a-127">As saturation is decreased, the hue becomes more gray.</span></span> <span data-ttu-id="0db3a-128">飽和度值為零會產生灰色的值。</span><span class="sxs-lookup"><span data-stu-id="0db3a-128">A saturation value of zero results in a gray-scale value.</span></span>

<span data-ttu-id="0db3a-129">下圖是 HLS 空間的線條繪圖，也就是雙重 hexcone。</span><span class="sxs-lookup"><span data-stu-id="0db3a-129">The following figure is a line drawing of HLS space, which is a double hexcone.</span></span> <span data-ttu-id="0db3a-130">HLS 色彩空間的任何水準交叉區段都是六邊形。</span><span class="sxs-lookup"><span data-stu-id="0db3a-130">Any horizontal cross section of the HLS color space is a hexagon.</span></span> <span data-ttu-id="0db3a-131">HLS 是正規化的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="0db3a-131">HLS is a normalized color space.</span></span> <span data-ttu-id="0db3a-132">也就是說，亮度和飽和度值的範圍是從0.0 到1.0 （含）。</span><span class="sxs-lookup"><span data-stu-id="0db3a-132">That is, the lightness and saturation values range from 0.0 to 1.0 inclusive.</span></span> <span data-ttu-id="0db3a-133">色調會因0和360（含）而異。</span><span class="sxs-lookup"><span data-stu-id="0db3a-133">Hue varies from 0 to 360 inclusive.</span></span>

![hls 色彩空間](images/hlsline.png)

<span data-ttu-id="0db3a-135">HLS 色彩空間可與裝置相依或與裝置無關。</span><span class="sxs-lookup"><span data-stu-id="0db3a-135">HLS color spaces can be device dependent or device independent.</span></span>

 

 




