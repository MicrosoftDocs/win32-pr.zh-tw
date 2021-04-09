---
title: 移植圖元作業
description: 移植圖元作業
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- 鳶尾花 GL 移植，圖元
- 從鳶尾花 GL 進行移植，圖元
- 從鳶尾花 GL 移植至 OpenGL，圖元
- 從鳶尾花 GL 的 OpenGL 移植，圖元
- 從鳶尾花 GL 移植的圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674539"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="fe4cb-108">移植圖元作業</span><span class="sxs-lookup"><span data-stu-id="fe4cb-108">Porting Pixel Operations</span></span>

<span data-ttu-id="fe4cb-109">移植牽涉到圖元運算的程式碼時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="fe4cb-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="fe4cb-110">邏輯圖元作業不會套用到 RGBA 色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="fe4cb-111">如需詳細資訊，請參閱 [**glLogicOp**](gllogicop.md)。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="fe4cb-112">一般而言，鳶尾花 GL 會使用 ABGR 格式的圖元，而 OpenGL 則使用 RGBA。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="fe4cb-113">您可以使用 [**glPixelStore**](glpixelstore-functions.md)來變更格式。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="fe4cb-114">移植 **lrectwrite** 函式時，請注意 **lrectwrite** 正在撰寫的位置 (例如，它可能會寫入深度緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="fe4cb-115">OpenGL 可提供您一些額外的圖元運算彈性。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="fe4cb-116">下表列出圖元作業的鳶尾花 GL 函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="fe4cb-117">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="fe4cb-117">IRIS GL function</span></span>                                   | <span data-ttu-id="fe4cb-118">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="fe4cb-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="fe4cb-119">意義</span><span class="sxs-lookup"><span data-stu-id="fe4cb-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fe4cb-120">**lrectread**、 **rectread**、**readRGB**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="fe4cb-121">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="fe4cb-122">從畫面格緩衝區讀取圖元區塊。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="fe4cb-123">**lrectwrite**、 **rectwrite**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="fe4cb-124">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="fe4cb-125">將圖元區塊寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="fe4cb-126">**rectcopy**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="fe4cb-127">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="fe4cb-128">複製畫面格緩衝區中的圖元。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="fe4cb-129">**rectzoom**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="fe4cb-130">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="fe4cb-131">指定 **glDrawPixels** 和 **glCopyPixels** 的圖元縮放因數。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="fe4cb-132">**cmov**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-132">**cmov**</span></span>                                           | [<span data-ttu-id="fe4cb-133">glRasterPos</span><span class="sxs-lookup"><span data-stu-id="fe4cb-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="fe4cb-134">指定圖元作業的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="fe4cb-135">**readsource**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-135">**readsource**</span></span>                                     | [<span data-ttu-id="fe4cb-136">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="fe4cb-137">選取圖元的色彩緩衝區來源。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="fe4cb-138">**pixmode**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-138">**pixmode**</span></span>                                        | <span data-ttu-id="fe4cb-139">[**glPixelStore**](glpixelstore-functions.md)、[**glPixelTransfer**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="fe4cb-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="fe4cb-140">設定圖元儲存模式。設定圖元傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="fe4cb-141">**logicop**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-141">**logicop**</span></span>                                        | [<span data-ttu-id="fe4cb-142">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="fe4cb-143">指定圖元寫入的邏輯運算。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="fe4cb-144">[**glEnable**](glenable.md) ( GL \_ 邏輯 \_ OP ) </span><span class="sxs-lookup"><span data-stu-id="fe4cb-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="fe4cb-145">開啟圖元邏輯作業。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="fe4cb-146">如需可能邏輯作業的完整清單，請參閱 [**glLogicOp**](gllogicop.md)。</span><span class="sxs-lookup"><span data-stu-id="fe4cb-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="fe4cb-147">此鳶尾花 GL 程式碼範例顯示一般的圖元寫入：</span><span class="sxs-lookup"><span data-stu-id="fe4cb-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="fe4cb-148">上述程式碼在轉譯為 OpenGL 時看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="fe4cb-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





