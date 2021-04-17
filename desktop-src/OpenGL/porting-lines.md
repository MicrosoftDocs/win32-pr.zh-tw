---
title: 移植線
description: 移植鳶尾花 GL 程式碼來繪製線條相當簡單，不過您應該注意 OpenGL stipples 方式的差異。 下表列出用來繪製線條的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- 鳶尾花 GL 移植，線路
- 從鳶尾花 GL 進行移植，行
- 從鳶尾花 GL 移植至 OpenGL，行
- 從鳶尾花 GL 的 OpenGL 移植，行
- 繪製函數，線條
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183896"
---
# <a name="porting-lines"></a><span data-ttu-id="46652-110">移植線</span><span class="sxs-lookup"><span data-stu-id="46652-110">Porting Lines</span></span>

<span data-ttu-id="46652-111">移植鳶尾花 GL 程式碼來繪製線條相當簡單，不過您應該注意 OpenGL stipples 方式的差異。</span><span class="sxs-lookup"><span data-stu-id="46652-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="46652-112">下表列出用來繪製線條的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="46652-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="46652-113">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="46652-113">IRIS GL function</span></span>                               | <span data-ttu-id="46652-114">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="46652-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="46652-115">意義</span><span class="sxs-lookup"><span data-stu-id="46652-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46652-116">**bgnclosedline**、**endclosedline**</span><span class="sxs-lookup"><span data-stu-id="46652-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="46652-117">[**glBegin**](glbegin.md) ( GL \_ 線路 \_ 迴圈 ) [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="46652-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="46652-118">繪製封閉線。</span><span class="sxs-lookup"><span data-stu-id="46652-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="46652-119">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="46652-119">**bgnline**</span></span>                                    | <span data-ttu-id="46652-120">[**glBegin**](glbegin.md) ( GL \_ 行 \_ 帶 ) </span><span class="sxs-lookup"><span data-stu-id="46652-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="46652-121">繪製線段。</span><span class="sxs-lookup"><span data-stu-id="46652-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="46652-122">**寬**</span><span class="sxs-lookup"><span data-stu-id="46652-122">**linewidth**</span></span>                                  | [<span data-ttu-id="46652-123">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="46652-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="46652-124">設定線條寬度。</span><span class="sxs-lookup"><span data-stu-id="46652-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="46652-125">**getlwidth**</span><span class="sxs-lookup"><span data-stu-id="46652-125">**getlwidth**</span></span>                                  | <span data-ttu-id="46652-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 行 \_ 寬度 ) </span><span class="sxs-lookup"><span data-stu-id="46652-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="46652-127">傳回目前的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="46652-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="46652-128">**deflinestyle**、**setlinestyle**</span><span class="sxs-lookup"><span data-stu-id="46652-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="46652-129">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="46652-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="46652-130">指定行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="46652-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="46652-131">**lsrepeat**</span><span class="sxs-lookup"><span data-stu-id="46652-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="46652-132">**glLineStipple** 的因數引數</span><span class="sxs-lookup"><span data-stu-id="46652-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="46652-133">設定線條樣式的重複因數。</span><span class="sxs-lookup"><span data-stu-id="46652-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="46652-134">**getlstyle**</span><span class="sxs-lookup"><span data-stu-id="46652-134">**getlstyle**</span></span>                                  | <span data-ttu-id="46652-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ 模式 ) </span><span class="sxs-lookup"><span data-stu-id="46652-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="46652-136">傳回 line stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="46652-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="46652-137">**getlsrepeat**</span><span class="sxs-lookup"><span data-stu-id="46652-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="46652-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 行 \_ STIPPLE \_ 重複 ) </span><span class="sxs-lookup"><span data-stu-id="46652-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="46652-139">傳回重複因數。</span><span class="sxs-lookup"><span data-stu-id="46652-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="46652-140">**linesmooth**、 **smoothline**</span><span class="sxs-lookup"><span data-stu-id="46652-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="46652-141">[**glEnable**](glenable.md) ( GL \_ 行 \_ 平滑 ) </span><span class="sxs-lookup"><span data-stu-id="46652-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="46652-142">開啟線條消除鋸齒 (如需消除鋸齒的詳細資訊，請參閱 [移植消除鋸齒功能](porting-antialiasing-functions.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="46652-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="46652-143">OpenGL 不會使用表格進行行 stipples;它只會維護一個行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="46652-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="46652-144">您可以使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 在不同的 stipple 模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="46652-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="46652-145">舊版的鳶尾花 GL 線條樣式函式 (例如 **draw**、 **lsbackup**、 **Getlsbackup** 等等) 不受 OpenGL 支援。</span><span class="sxs-lookup"><span data-stu-id="46652-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="46652-146">如需繪製反鋸齒線條的詳細資訊，請參閱 [移植消除鋸齒功能](porting-antialiasing-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="46652-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="46652-147">??</span><span class="sxs-lookup"><span data-stu-id="46652-147">??</span></span>

 

 





