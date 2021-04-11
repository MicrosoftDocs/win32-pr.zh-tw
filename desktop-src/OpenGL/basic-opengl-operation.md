---
title: 基本 OpenGL 操作
description: 基本 OpenGL 操作
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL，基本作業
- OpenGL，資料處理
- OpenGL，處理階段
- OpenGL、顯示清單
- 顯示清單 OpenGL
- OpenGL，評估工具
- 評估 OpenGL
- OpenGL、每個頂點作業
- 每個頂點的作業 OpenGL
- OpenGL、基本元件
- 基本元件 OpenGL
- OpenGL、點陣化
- 點陣化 OpenGL
- OpenGL、每個片段的作業
- 每個片段的作業 OpenGL
- framebuffers，基本作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103945568"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="5ea63-119">基本 OpenGL 操作</span><span class="sxs-lookup"><span data-stu-id="5ea63-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="5ea63-120">下圖說明 OpenGL 如何處理資料。</span><span class="sxs-lookup"><span data-stu-id="5ea63-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="5ea63-121">如所示，命令會從左邊進入，然後繼續處理管線。</span><span class="sxs-lookup"><span data-stu-id="5ea63-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="5ea63-122">有些命令會指定要繪製的幾何物件，而其他則會控制在不同處理階段處理物件的方式。</span><span class="sxs-lookup"><span data-stu-id="5ea63-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![顯示 OpenGL 資料處理管線階段的圖表。](images/basic01.png)

<span data-ttu-id="5ea63-124">基本 OpenGL 操作中的處理階段如下所示：</span><span class="sxs-lookup"><span data-stu-id="5ea63-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="5ea63-125">**顯示清單** 您可以選擇在顯示清單中累積某些命令，以供稍後處理，而不是讓所有的命令立即透過管線進行。</span><span class="sxs-lookup"><span data-stu-id="5ea63-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="5ea63-126">**評估** 工具處理的評估階段可透過評估輸入值的多項式命令，提供更有效率的方式來接近曲線和表面幾何。</span><span class="sxs-lookup"><span data-stu-id="5ea63-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="5ea63-127">**每個頂點的作業和基本元件** OpenGL 會處理幾何 primitivespoints、線段線段，以及由頂點描述的 polygonsall。</span><span class="sxs-lookup"><span data-stu-id="5ea63-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="5ea63-128">頂點會轉換並亮掉，而且會將基本專案裁剪至區，以準備進行點陣化。</span><span class="sxs-lookup"><span data-stu-id="5ea63-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="5ea63-129">**光柵** 化柵格化階段會使用點、線段或多邊形的二維描述，產生一系列的框架緩衝區位址和相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="5ea63-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="5ea63-130">產生的每個片段都會送入最後一個階段，也就是每個片段的作業。</span><span class="sxs-lookup"><span data-stu-id="5ea63-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="5ea63-131">**每個片段的作業** 這些是在資料儲存為畫面格緩衝區中的圖元之前，對資料執行的最後一項作業。</span><span class="sxs-lookup"><span data-stu-id="5ea63-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="5ea63-132">每個片段的作業包含畫面格緩衝區的條件式更新，會根據內送和先前儲存的 z 值 (z 緩衝) 和混合內送圖元色彩與儲存的色彩，以及遮罩和其他圖元值的邏輯運算。</span><span class="sxs-lookup"><span data-stu-id="5ea63-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="5ea63-133">資料可以輸入像素格式，而不是頂點。</span><span class="sxs-lookup"><span data-stu-id="5ea63-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="5ea63-134">像素格式的資料（例如，可能會描述用於材質對應的影像），會略過上述處理的第一個階段，並改為在圖元作業階段中處理為圖元。</span><span class="sxs-lookup"><span data-stu-id="5ea63-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="5ea63-135">以下是圖元運算，圖元資料是：</span><span class="sxs-lookup"><span data-stu-id="5ea63-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="5ea63-136">儲存為材質記憶體，以在點陣化階段中使用。</span><span class="sxs-lookup"><span data-stu-id="5ea63-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="5ea63-137">柵格化，並將產生的片段合併到畫面格緩衝區，就像是從幾何資料產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="5ea63-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




