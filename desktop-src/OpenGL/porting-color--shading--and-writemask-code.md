---
title: 移植色彩、陰影和 Writemask 程式碼
description: 移植色彩、陰影和 Writemask 程式碼
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- 鳶尾花 GL 移植，色彩
- 從鳶尾花 GL 進行移植，色彩
- 從鳶尾花 GL 移植至 OpenGL，色彩
- 從鳶尾花 GL 的 OpenGL 移植，色彩
- 鳶尾花 GL 移植，網底
- 從鳶尾花 GL 進行移植，網底
- 從鳶尾花 GL 移植至 OpenGL，網底
- 從鳶尾花 GL 的 OpenGL 移植，網底
- 鳶尾花 GL 移植，writemask
- 從鳶尾花 GL、writemask 移植
- 從鳶尾花 GL （writemask）移植至 OpenGL
- 從鳶尾花 GL writemask 的 OpenGL 移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671844"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="eac61-115">移植色彩、陰影和 Writemask 程式碼</span><span class="sxs-lookup"><span data-stu-id="eac61-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="eac61-116">將色彩、陰影和 writemask 程式碼移植至 OpenGL 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="eac61-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="eac61-117">雖然您可以使用 OpenGL [glIndex](glindex-functions.md) 函式來設定色彩對應索引，但 opengl 沒有載入色彩對應索引的函式。</span><span class="sxs-lookup"><span data-stu-id="eac61-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="eac61-118">色彩值會正規化為其資料類型。</span><span class="sxs-lookup"><span data-stu-id="eac61-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="eac61-119"> (需色彩值的相關資訊，請參閱 [glColor](glcolor-functions.md)) 。</span><span class="sxs-lookup"><span data-stu-id="eac61-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="eac61-120">**Cpack** 沒有很簡單的對等用法。</span><span class="sxs-lookup"><span data-stu-id="eac61-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="eac61-121">您可能必須將包含 **c** 或 **color** 函數的程式碼轉譯為 [**glClearColor**](glclearcolor.md) 或 [**GlClearIndex**](glclearindex.md) ，而不是 **glColor** 或 **glIndex**。</span><span class="sxs-lookup"><span data-stu-id="eac61-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="eac61-122">RGBA writemask 適用于每個元件，但不適用每個位。</span><span class="sxs-lookup"><span data-stu-id="eac61-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="eac61-123">鳶尾花 GL 提供定義的色彩常數：黑色、藍色、紅色、綠色、洋紅、青色、黃色和白色。</span><span class="sxs-lookup"><span data-stu-id="eac61-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="eac61-124">OpenGL 不提供這些常數。</span><span class="sxs-lookup"><span data-stu-id="eac61-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="eac61-125">本主題包含下列各項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eac61-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="eac61-126">移植色彩呼叫</span><span class="sxs-lookup"><span data-stu-id="eac61-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="eac61-127">移植網底模型</span><span class="sxs-lookup"><span data-stu-id="eac61-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




