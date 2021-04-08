---
title: 需要目前圖形位置的埠程式碼
description: OpenGL 不會維護目前的圖形位置。 相依于目前圖形位置的鳶尾花 GL 函式（例如 move、draw 和 rmv）在 OpenGL 中沒有對等專案。
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- 鳶尾花 GL 移植，目前圖形位置
- 從鳶尾花 GL、目前的圖形位置進行移植
- 從鳶尾花 GL 移植至 OpenGL，目前的圖形位置
- 從鳶尾花 GL、目前圖形位置的 OpenGL 移植
- 目前的圖形位置
- 點陣位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "103679264"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="eb08a-110">需要目前圖形位置的埠程式碼</span><span class="sxs-lookup"><span data-stu-id="eb08a-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="eb08a-111">OpenGL 不會維護目前的圖形位置。</span><span class="sxs-lookup"><span data-stu-id="eb08a-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="eb08a-112">相依于目前圖形位置的鳶尾花 GL 函式（例如 **move**、 **draw** 和 **rmv**）在 OpenGL 中沒有對等專案。</span><span class="sxs-lookup"><span data-stu-id="eb08a-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="eb08a-113">較舊版本的鳶尾花 GL 包含依賴目前圖形位置的繪圖命令，但不建議使用它們。</span><span class="sxs-lookup"><span data-stu-id="eb08a-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="eb08a-114">如果您以任何方式使用目前的圖形位置，或使用下列任何常式，您將需要重寫程式碼：</span><span class="sxs-lookup"><span data-stu-id="eb08a-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="eb08a-115">**繪製** 和 **移動**</span><span class="sxs-lookup"><span data-stu-id="eb08a-115">**draw** and **move**</span></span>
-   <span data-ttu-id="eb08a-116">**pmv**、 **寮國** 和 **pclos**</span><span class="sxs-lookup"><span data-stu-id="eb08a-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="eb08a-117">**rdr**、 **rmv**、 **rpdr** 和 **rpmv**</span><span class="sxs-lookup"><span data-stu-id="eb08a-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="eb08a-118">**getgpos**</span><span class="sxs-lookup"><span data-stu-id="eb08a-118">**getgpos**</span></span>

<span data-ttu-id="eb08a-119">OpenGL 具有對應至鳶尾花 GL 目前字元位置的點陣位置概念。</span><span class="sxs-lookup"><span data-stu-id="eb08a-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="eb08a-120">如需有關點陣定位的詳細資訊，請參閱 [移植圖元作業](porting-pixel-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="eb08a-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="eb08a-121">本主題包含下列各項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb08a-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="eb08a-122">移植螢幕和緩衝區清除命令</span><span class="sxs-lookup"><span data-stu-id="eb08a-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="eb08a-123">移植矩陣和轉換函數</span><span class="sxs-lookup"><span data-stu-id="eb08a-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="eb08a-124">移植 MSINGLE 模式程式碼</span><span class="sxs-lookup"><span data-stu-id="eb08a-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="eb08a-125">移植可取得矩陣和轉換的函式</span><span class="sxs-lookup"><span data-stu-id="eb08a-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="eb08a-126">移植區、Screenmasks 和 Scrboxes</span><span class="sxs-lookup"><span data-stu-id="eb08a-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="eb08a-127">移植裁剪平面</span><span class="sxs-lookup"><span data-stu-id="eb08a-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




