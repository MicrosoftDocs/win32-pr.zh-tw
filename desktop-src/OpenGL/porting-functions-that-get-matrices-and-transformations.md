---
title: 移植可取得矩陣和轉換的函式
description: 下表列出的鳶尾花 GL 函數會取得矩陣和轉換的狀態，以及其 OpenGL 對等專案。
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- 鳶尾花 GL 移植，矩陣
- 從鳶尾花 GL （矩陣）移植
- 從鳶尾花 GL （矩陣）移植至 OpenGL
- 從鳶尾花 GL （矩陣）進行 OpenGL 移植
- 矩陣
- 鳶尾花 GL 移植，轉換
- 從鳶尾花 GL 進行移植，轉換
- 從鳶尾花 GL 移植至 OpenGL，轉換
- 從鳶尾花 GL 的 OpenGL 移植，轉換
- 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932320"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="0ed14-113">移植可取得矩陣和轉換的函式</span><span class="sxs-lookup"><span data-stu-id="0ed14-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="0ed14-114">下表列出的鳶尾花 GL 函數會取得矩陣和轉換的狀態，以及其 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="0ed14-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="0ed14-115">鳶尾花 GL 矩陣查詢</span><span class="sxs-lookup"><span data-stu-id="0ed14-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="0ed14-116">OpenGL glGet 矩陣查詢</span><span class="sxs-lookup"><span data-stu-id="0ed14-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="0ed14-117">意義</span><span class="sxs-lookup"><span data-stu-id="0ed14-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0ed14-118">**getmmode**</span><span class="sxs-lookup"><span data-stu-id="0ed14-118">**getmmode**</span></span>                          | <span data-ttu-id="0ed14-119">GL \_ 矩陣 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="0ed14-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="0ed14-120">傳回目前的矩陣模式。</span><span class="sxs-lookup"><span data-stu-id="0ed14-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="0ed14-121">在 **MVIEWING** 模式中 **getmatrix**</span><span class="sxs-lookup"><span data-stu-id="0ed14-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="0ed14-122">GL \_ 模型 \_ 矩陣</span><span class="sxs-lookup"><span data-stu-id="0ed14-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="0ed14-123">傳回目前模型視圖矩陣的複本。</span><span class="sxs-lookup"><span data-stu-id="0ed14-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="0ed14-124">在 **MPROJECTION** 模式中 **getmatrix**</span><span class="sxs-lookup"><span data-stu-id="0ed14-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="0ed14-125">GL \_ 投射 \_ 矩陣</span><span class="sxs-lookup"><span data-stu-id="0ed14-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="0ed14-126">傳回目前投射矩陣的複本。</span><span class="sxs-lookup"><span data-stu-id="0ed14-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="0ed14-127">在 **MTEXTURE** 模式中 **getmatrix**</span><span class="sxs-lookup"><span data-stu-id="0ed14-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="0ed14-128">GL \_ 材質 \_ 矩陣</span><span class="sxs-lookup"><span data-stu-id="0ed14-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="0ed14-129">傳回目前材質矩陣的複本。</span><span class="sxs-lookup"><span data-stu-id="0ed14-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="0ed14-130">不適用。</span><span class="sxs-lookup"><span data-stu-id="0ed14-130">Not applicable.</span></span>                       | <span data-ttu-id="0ed14-131">GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="0ed14-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="0ed14-132">傳回模型視圖矩陣堆疊支援的最大深度。</span><span class="sxs-lookup"><span data-stu-id="0ed14-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="0ed14-133">不適用。</span><span class="sxs-lookup"><span data-stu-id="0ed14-133">Not applicable.</span></span>                       | <span data-ttu-id="0ed14-134">GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="0ed14-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="0ed14-135">傳回投影矩陣堆疊支援的最大深度。</span><span class="sxs-lookup"><span data-stu-id="0ed14-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="0ed14-136">不適用。</span><span class="sxs-lookup"><span data-stu-id="0ed14-136">Not applicable.</span></span>                       | <span data-ttu-id="0ed14-137">GL \_ 最大 \_ 紋理 \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="0ed14-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="0ed14-138">傳回材質矩陣堆疊支援的最大深度。</span><span class="sxs-lookup"><span data-stu-id="0ed14-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="0ed14-139">不適用。</span><span class="sxs-lookup"><span data-stu-id="0ed14-139">Not applicable.</span></span>                       | <span data-ttu-id="0ed14-140">GL \_ 模型 \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="0ed14-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="0ed14-141">傳回模型視圖堆疊上的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="0ed14-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="0ed14-142">不適用。</span><span class="sxs-lookup"><span data-stu-id="0ed14-142">Not applicable.</span></span>                       | <span data-ttu-id="0ed14-143">GL \_ 投射 \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="0ed14-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="0ed14-144">傳回投射堆疊上的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="0ed14-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="0ed14-145">不適用。</span><span class="sxs-lookup"><span data-stu-id="0ed14-145">Not applicable.</span></span>                       | <span data-ttu-id="0ed14-146">GL \_ 紋理 \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="0ed14-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="0ed14-147">傳回紋理堆疊上的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="0ed14-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="0ed14-148">??</span><span class="sxs-lookup"><span data-stu-id="0ed14-148">??</span></span>

 

 




