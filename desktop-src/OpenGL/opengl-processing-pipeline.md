---
title: OpenGL 處理管線
description: OpenGL 處理管線
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL，處理管線
- 處理管線 OpenGL
- 管線 OpenGL
- framebuffers，處理管線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104563406"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="4b791-107">OpenGL 處理管線</span><span class="sxs-lookup"><span data-stu-id="4b791-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="4b791-108">許多 OpenGL 函數專門用來繪製物件，例如點、線條、多邊形和點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4b791-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="4b791-109">某些函式控制這種繪圖的發生方式 (例如啟用消除鋸齒或紋理) 的方式。</span><span class="sxs-lookup"><span data-stu-id="4b791-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="4b791-110">其他函式特別關心畫面格緩衝區操作。</span><span class="sxs-lookup"><span data-stu-id="4b791-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="4b791-111">本節中的主題描述所有 OpenGL 函數如何一起運作，以建立 OpenGL 處理管線。</span><span class="sxs-lookup"><span data-stu-id="4b791-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="4b791-112">本節也會進一步探討實際處理資料的階段，並將這些階段系結至 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="4b791-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="4b791-113">下圖詳細說明 OpenGL 處理管線。</span><span class="sxs-lookup"><span data-stu-id="4b791-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="4b791-114">針對大部分的管線，您可以看到主要階段之間的三個垂直箭號。</span><span class="sxs-lookup"><span data-stu-id="4b791-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="4b791-115">這些箭號代表頂點，以及可以與頂點相關聯的兩個主要資料類型：色彩值和材質座標。</span><span class="sxs-lookup"><span data-stu-id="4b791-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="4b791-116">另請注意，頂點會組合成基本專案，然後放入片段，最後變成畫面格緩衝區中的圖元。</span><span class="sxs-lookup"><span data-stu-id="4b791-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="4b791-117">這項進展會在 [頂點](vertices.md)、 [基本](primitives.md)、 [片段](fragments.md)和 [圖元](pixels.md)中更詳細地討論。</span><span class="sxs-lookup"><span data-stu-id="4b791-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![顯示 OpenGL 處理管線的圖表。](images/proc01.png)

 

 




