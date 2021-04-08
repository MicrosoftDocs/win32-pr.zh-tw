---
title: glRasterPos 函式
description: 這些函數會指定圖元作業的點陣位置。
ms.assetid: 2a661893-0818-441d-9399-0103560737c3
keywords:
- OpenGL、glRasterPos 函式
- OpenGL 參考，glRasterPos 函式
- OpenGL，glRasterPos 函式的參考
- OpenGL、點陣函數
- OpenGL 參考，點陣函數
- OpenGL、點陣函數的參考
- glRasterPos 函式
- 點陣向量函數
- OpenGL，圖元函數
- OpenGL 參考，圖元函數
- OpenGL，圖元函數的參考
- 圖元、函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f2ce2f387e70b3ea7a378b5463a03a88a4d5d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674096"
---
# <a name="glrasterpos-functions"></a><span data-ttu-id="26b92-115">glRasterPos 函式</span><span class="sxs-lookup"><span data-stu-id="26b92-115">glRasterPos Functions</span></span>

<span data-ttu-id="26b92-116">這些函數會指定圖元作業的點陣位置：</span><span class="sxs-lookup"><span data-stu-id="26b92-116">These functions specify the raster position for pixel operations:</span></span>

-   [<span data-ttu-id="26b92-117">**glRasterPos2d**</span><span class="sxs-lookup"><span data-stu-id="26b92-117">**glRasterPos2d**</span></span>](glrasterpos2d.md)
-   [<span data-ttu-id="26b92-118">**glRasterPos2f**</span><span class="sxs-lookup"><span data-stu-id="26b92-118">**glRasterPos2f**</span></span>](glrasterpos2f.md)
-   [<span data-ttu-id="26b92-119">**glRasterPos2i**</span><span class="sxs-lookup"><span data-stu-id="26b92-119">**glRasterPos2i**</span></span>](glrasterpos2i.md)
-   [<span data-ttu-id="26b92-120">**glRasterPos2s**</span><span class="sxs-lookup"><span data-stu-id="26b92-120">**glRasterPos2s**</span></span>](glrasterpos2s.md)
-   [<span data-ttu-id="26b92-121">**glRasterPos3d**</span><span class="sxs-lookup"><span data-stu-id="26b92-121">**glRasterPos3d**</span></span>](glrasterpos3d.md)
-   [<span data-ttu-id="26b92-122">**glRasterPos3f**</span><span class="sxs-lookup"><span data-stu-id="26b92-122">**glRasterPos3f**</span></span>](glrasterpos3f.md)
-   [<span data-ttu-id="26b92-123">**glRasterPos3i**</span><span class="sxs-lookup"><span data-stu-id="26b92-123">**glRasterPos3i**</span></span>](glrasterpos3i.md)
-   [<span data-ttu-id="26b92-124">**glRasterPos3s**</span><span class="sxs-lookup"><span data-stu-id="26b92-124">**glRasterPos3s**</span></span>](glrasterpos3s.md)
-   [<span data-ttu-id="26b92-125">**glRasterPos4d**</span><span class="sxs-lookup"><span data-stu-id="26b92-125">**glRasterPos4d**</span></span>](glrasterpos4d.md)
-   [<span data-ttu-id="26b92-126">**glRasterPos4f**</span><span class="sxs-lookup"><span data-stu-id="26b92-126">**glRasterPos4f**</span></span>](glrasterpos4f.md)
-   [<span data-ttu-id="26b92-127">**glRasterPos4i**</span><span class="sxs-lookup"><span data-stu-id="26b92-127">**glRasterPos4i**</span></span>](glrasterpos4i.md)
-   [<span data-ttu-id="26b92-128">**glRasterPos4s**</span><span class="sxs-lookup"><span data-stu-id="26b92-128">**glRasterPos4s**</span></span>](glrasterpos4s.md)
-   [<span data-ttu-id="26b92-129">**glRasterPos2dv**</span><span class="sxs-lookup"><span data-stu-id="26b92-129">**glRasterPos2dv**</span></span>](glrasterpos2dv.md)
-   [<span data-ttu-id="26b92-130">**glRasterPos2fv**</span><span class="sxs-lookup"><span data-stu-id="26b92-130">**glRasterPos2fv**</span></span>](glrasterpos2fv.md)
-   [<span data-ttu-id="26b92-131">**glRasterPos2iv**</span><span class="sxs-lookup"><span data-stu-id="26b92-131">**glRasterPos2iv**</span></span>](glrasterpos2iv.md)
-   [<span data-ttu-id="26b92-132">**glRasterPos2sv**</span><span class="sxs-lookup"><span data-stu-id="26b92-132">**glRasterPos2sv**</span></span>](glrasterpos2sv.md)
-   [<span data-ttu-id="26b92-133">**glRasterPos3dv**</span><span class="sxs-lookup"><span data-stu-id="26b92-133">**glRasterPos3dv**</span></span>](glrasterpos3dv.md)
-   [<span data-ttu-id="26b92-134">**glRasterPos3fv**</span><span class="sxs-lookup"><span data-stu-id="26b92-134">**glRasterPos3fv**</span></span>](glrasterpos3fv.md)
-   [<span data-ttu-id="26b92-135">**glRasterPos3iv**</span><span class="sxs-lookup"><span data-stu-id="26b92-135">**glRasterPos3iv**</span></span>](glrasterpos3iv.md)
-   [<span data-ttu-id="26b92-136">**glRasterPos3sv**</span><span class="sxs-lookup"><span data-stu-id="26b92-136">**glRasterPos3sv**</span></span>](glrasterpos3sv.md)
-   [<span data-ttu-id="26b92-137">**glRasterPos4dv**</span><span class="sxs-lookup"><span data-stu-id="26b92-137">**glRasterPos4dv**</span></span>](glrasterpos4dv.md)
-   [<span data-ttu-id="26b92-138">**glRasterPos4fv**</span><span class="sxs-lookup"><span data-stu-id="26b92-138">**glRasterPos4fv**</span></span>](glrasterpos4fv.md)
-   [<span data-ttu-id="26b92-139">**glRasterPos4iv**</span><span class="sxs-lookup"><span data-stu-id="26b92-139">**glRasterPos4iv**</span></span>](glrasterpos4iv.md)
-   [<span data-ttu-id="26b92-140">**glRasterPos4sv**</span><span class="sxs-lookup"><span data-stu-id="26b92-140">**glRasterPos4sv**</span></span>](glrasterpos4sv.md)

 

 




