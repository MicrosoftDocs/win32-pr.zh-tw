---
title: 移植弧形和圓形
description: 使用 OpenGL，填滿的弧形和圓形會以與空心弧形和圓形相同的呼叫來繪製。 下表列出鳶尾花 GL arc 和 circle 函數，以及其對等的 OpenGL (X.GLU 隊) 函式。
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- 鳶尾花 GL 移植，弧形
- 從鳶尾花 GL、弧形移植
- 從鳶尾花 GL （弧形）移植至 OpenGL
- 從鳶尾花 GL、弧形移植的 OpenGL
- 繪製函數，弧形
- 鳶尾花 GL 移植，圓形
- 從鳶尾花 GL、圓形進行移植
- 從鳶尾花 GL 移植至 OpenGL，圓形
- 從鳶尾花 GL、圓形的 OpenGL 移植
- 繪圖函數、圓形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372615"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="6212a-114">移植弧形和圓形</span><span class="sxs-lookup"><span data-stu-id="6212a-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="6212a-115">使用 OpenGL，填滿的弧形和圓形會以與空心弧形和圓形相同的呼叫來繪製。</span><span class="sxs-lookup"><span data-stu-id="6212a-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="6212a-116">下表列出鳶尾花 GL arc 和 circle 函數，以及其對等的 OpenGL (X.GLU 隊) 函式。</span><span class="sxs-lookup"><span data-stu-id="6212a-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="6212a-117">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="6212a-117">IRIS GL function</span></span> | <span data-ttu-id="6212a-118">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="6212a-118">OpenGL function</span></span>                          | <span data-ttu-id="6212a-119">意義</span><span class="sxs-lookup"><span data-stu-id="6212a-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="6212a-120">**arcarcf**</span><span class="sxs-lookup"><span data-stu-id="6212a-120">**arcarcf**</span></span>      | [<span data-ttu-id="6212a-121">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="6212a-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="6212a-122">繪製弧形。</span><span class="sxs-lookup"><span data-stu-id="6212a-122">Draws an arc.</span></span>           |
| <span data-ttu-id="6212a-123">**circcircf**</span><span class="sxs-lookup"><span data-stu-id="6212a-123">**circcircf**</span></span>    | [<span data-ttu-id="6212a-124">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="6212a-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="6212a-125">繪製圓形或磁片。</span><span class="sxs-lookup"><span data-stu-id="6212a-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="6212a-126">您可以使用鳶尾花 GL 無法進行的 OpenGL 弧形和圓形來做一些事情。</span><span class="sxs-lookup"><span data-stu-id="6212a-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="6212a-127">OpenGL 會分別呼叫弧形和圓形、磁片和部分磁片。</span><span class="sxs-lookup"><span data-stu-id="6212a-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="6212a-128">移植弧形和圓形時，請記住下列關於 OpenGL 的重點：</span><span class="sxs-lookup"><span data-stu-id="6212a-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="6212a-129">角度是以度為單位，而不是以十分之一度為單位。</span><span class="sxs-lookup"><span data-stu-id="6212a-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="6212a-130">開始角度是從正 y 軸（而不是從 X 軸）來測量。</span><span class="sxs-lookup"><span data-stu-id="6212a-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="6212a-131">立即的掃描角度（而不是逆時針）。</span><span class="sxs-lookup"><span data-stu-id="6212a-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="6212a-132">??</span><span class="sxs-lookup"><span data-stu-id="6212a-132">??</span></span>

 

 




