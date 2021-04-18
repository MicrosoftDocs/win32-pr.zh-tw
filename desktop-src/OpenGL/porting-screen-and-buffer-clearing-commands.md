---
title: 移植螢幕和緩衝區清除命令
description: OpenGL 以單一函式 glClear 來取代各種鳶尾花 GL clear 函式 (例如 zclear、aclear、sclear 等) 。 藉由將遮罩傳遞給 glClear，指定您想要清除的內容。
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- 鳶尾花 GL 移植，清除功能
- 從鳶尾花 GL 進行移植，清除函式
- 從鳶尾花 GL 移植至 OpenGL，清除函式
- 從鳶尾花 GL 的 OpenGL 移植，清除函式
- 清除函式
- 鳶尾花 GL 移植，螢幕清除命令
- 從鳶尾花 GL 進行移植，螢幕清除命令
- 從鳶尾花 GL 移植至 OpenGL，螢幕清除命令
- 從鳶尾花 GL、螢幕清除命令的 OpenGL 移植
- 螢幕清除命令
- 鳶尾花 GL 移植，緩衝區清除命令
- 從鳶尾花 GL 進行移植，緩衝區清除命令
- 從鳶尾花 GL 移植至 OpenGL，緩衝區清除命令
- 從鳶尾花 GL 進行 OpenGL 移植，緩衝區清除命令
- 緩衝區清除命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965596"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="bb3e4-119">移植螢幕和緩衝區清除命令</span><span class="sxs-lookup"><span data-stu-id="bb3e4-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="bb3e4-120">OpenGL 以單一函式 [**glClear**](glclear.md)來取代各種鳶尾花 GL **clear** 函式 (例如 **zclear**、 **aclear**、 **sclear** 等) 。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="bb3e4-121">藉由將遮罩傳遞給 **glClear**，指定您想要清除的內容。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="bb3e4-122">移植螢幕和緩衝區命令時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="bb3e4-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="bb3e4-123">OpenGL 會以 [**glClearColor**](glclearcolor.md) 和 [**glClearIndex**](glclearindex.md)之類的呼叫，與繪製色彩分開維護清除色彩。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="bb3e4-124">清除之前，請務必為每個緩衝區設定 clear 色彩。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="bb3e4-125">您現在不需要使用數種不同的命名明確呼叫，而是使用一個呼叫、 [**glClear**](glclear.md)、 **or** 等的緩衝區遮罩來清除數個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="bb3e4-126">例如， **czclear** 會取代為：</span><span class="sxs-lookup"><span data-stu-id="bb3e4-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="bb3e4-127">鳶尾花 GL 參考多邊形 stipple 和色彩 writemask。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="bb3e4-128">OpenGL 會忽略多邊形 stipple，但會參考色彩 writemask。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="bb3e4-129"> (**czclear** 函式會忽略多邊形 stipple 和色彩 writemask。 ) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="bb3e4-130">下表列出各種鳶尾花 GL clear 函式與其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="bb3e4-131">鳶尾花 GL 通話</span><span class="sxs-lookup"><span data-stu-id="bb3e4-131">IRIS GL call</span></span>         | <span data-ttu-id="bb3e4-132">OpenGL 呼叫</span><span class="sxs-lookup"><span data-stu-id="bb3e4-132">OpenGL call</span></span>                                                               | <span data-ttu-id="bb3e4-133">意義</span><span class="sxs-lookup"><span data-stu-id="bb3e4-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="bb3e4-134">**acbuf** (AC \_ CLEAR) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="bb3e4-135">**glClear** ( GL \_ ACCUM \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="bb3e4-136">清除累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="bb3e4-137">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="bb3e4-138">設定 RGBA 清除色彩。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="bb3e4-139">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="bb3e4-140">設定清除色彩索引。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="bb3e4-141">**清除**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-141">**clear**</span></span>            | <span data-ttu-id="bb3e4-142">**glClear** ( GL \_ 色彩 \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="bb3e4-143">清除色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="bb3e4-144">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="bb3e4-145">指定深度緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="bb3e4-146">**zclear**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-146">**zclear**</span></span>           | <span data-ttu-id="bb3e4-147">**glClear** ( GL \_ 深度 \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="bb3e4-148">清除深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="bb3e4-149">**czclear**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-149">**czclear**</span></span>          | <span data-ttu-id="bb3e4-150">**glClear** ( GL \_ 色彩 \_ 緩衝區 \_ 位 \| GL \_ 深度 \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="bb3e4-151">清除色彩緩衝區和深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="bb3e4-152">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="bb3e4-153">指定累積緩衝區的明確值。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="bb3e4-154">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="bb3e4-155">指定樣板緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="bb3e4-156">**sclear**</span><span class="sxs-lookup"><span data-stu-id="bb3e4-156">**sclear**</span></span>           | <span data-ttu-id="bb3e4-157">**glClear** ( GL \_ 樣板 \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="bb3e4-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="bb3e4-158">清除樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="bb3e4-159">當您的鳶尾花 GL 程式碼同時使用 **gclear** 和 **sclear** 時，您可以將它們結合成單一 **glClear** 呼叫;可以改善您的程式效能。</span><span class="sxs-lookup"><span data-stu-id="bb3e4-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





