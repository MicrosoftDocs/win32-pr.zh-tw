---
title: RGB 色彩空間
description: RGB 色彩空間的建立方式是將紅色、綠色和藍色色彩對應到立體笛卡兒座標系統。
ms.assetid: fbe00c2a-700f-4905-a67a-47e3fd2bfa5c
keywords:
- Windows Color System (WCS) 、RGB 色彩空間
- WCS (Windows 色彩系統) 、RGB 色彩空間
- 影像色彩管理、RGB 色彩空間
- 色彩管理、RGB 色彩空間
- 色彩，RGB 色彩空間
- 色彩空間、RGB
- RGB 色彩空間
- '紅色綠色藍色 (RGB) '
- 'RGB (red 綠 blue) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a73ac8b87847dda92332a3dd1041043e093590
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106976610"
---
# <a name="rgb-color-spaces"></a><span data-ttu-id="15c9d-112">RGB 色彩空間</span><span class="sxs-lookup"><span data-stu-id="15c9d-112">RGB Color Spaces</span></span>

<span data-ttu-id="15c9d-113">RGB [色彩空間](c.md) 的建立方式是將紅色、綠色和藍色色彩對應到立體笛卡兒座標系統。</span><span class="sxs-lookup"><span data-stu-id="15c9d-113">An RGB [color space](c.md) is created by mapping the colors red, green, and blue onto a 3-D Cartesian coordinate system.</span></span> <span data-ttu-id="15c9d-114">此結果是立體 cube，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="15c9d-114">This results is a 3-D cube like the ones shown in the following figure.</span></span> <span data-ttu-id="15c9d-115">此圖顯示兩個不同角度的相同 RGB cube。</span><span class="sxs-lookup"><span data-stu-id="15c9d-115">This figure displays the same RGB cube from two different angles.</span></span> <span data-ttu-id="15c9d-116">請注意，座標系統的原點是黑色。</span><span class="sxs-lookup"><span data-stu-id="15c9d-116">Notice that the origin of the coordinate system is black.</span></span> <span data-ttu-id="15c9d-117">這是紅色、綠色和藍色 (RGB) 色彩元件全部0.0 的位置。</span><span class="sxs-lookup"><span data-stu-id="15c9d-117">This is where the red, green, and blue (RGB) color components are all 0.0.</span></span> <span data-ttu-id="15c9d-118">Cube 對角的邊角是白色，其中 RGB 色彩元件的最大值為。</span><span class="sxs-lookup"><span data-stu-id="15c9d-118">The diagonally opposite corner of the cube is white, where the RGB color components are at their maximum value.</span></span>

![rgb 色彩空間 cube （最大值）](images/rgbclrs1.png)

![rgb 色彩空間 cube （最小值）](images/rgbclrs2.png)

<span data-ttu-id="15c9d-121">如同大部分的 [色彩](c.md)空間，RGB 色彩空間已正規化。</span><span class="sxs-lookup"><span data-stu-id="15c9d-121">Like most [color spaces](c.md), the RGB color space is normalized.</span></span> <span data-ttu-id="15c9d-122">也就是說，所有色彩值都受限於零到一個（含）的範圍。</span><span class="sxs-lookup"><span data-stu-id="15c9d-122">That is, all color values are restricted to the range of zero to one inclusive.</span></span> <span data-ttu-id="15c9d-123">黑色是 (0.0、0.0、0.0) ，而白色 (1.0、1.0、1.0) 。</span><span class="sxs-lookup"><span data-stu-id="15c9d-123">So black is (0.0, 0.0, 0.0), and white is (1.0, 1.0, 1.0).</span></span>

<span data-ttu-id="15c9d-124">在 RGB 色彩空間中， [主要色彩](p.md) 為紅色、綠色和藍色。</span><span class="sxs-lookup"><span data-stu-id="15c9d-124">In the RGB color space, the [primary colors](p.md) are red, green, and blue.</span></span> <span data-ttu-id="15c9d-125">次要色彩為青色、黃色和洋紅。</span><span class="sxs-lookup"><span data-stu-id="15c9d-125">The secondary colors are cyan, yellow, and magenta.</span></span>

<span data-ttu-id="15c9d-126">RGB 色彩空間可與裝置相依或與裝置無關。</span><span class="sxs-lookup"><span data-stu-id="15c9d-126">RGB color spaces can be device dependent or device independent.</span></span>

 

 




