---
title: 轉換座標
description: OpenGL 公用程式程式庫 (X.GLU 隊) 提供數個常用的矩陣轉換函數。
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- OpenGL 公用程式 (X.GLU 隊) 、矩陣轉換函式
- X.GLU 隊 (OpenGL 公用程式) ，矩陣轉換函式
- 矩陣轉換函式 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、轉換座標
- X.GLU 隊 (OpenGL 公用程式) ，轉換座標
- 轉換座標 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675491"
---
# <a name="transforming-coordinates"></a><span data-ttu-id="3783f-109">轉換座標</span><span class="sxs-lookup"><span data-stu-id="3783f-109">Transforming Coordinates</span></span>

<span data-ttu-id="3783f-110">OpenGL 公用程式程式庫 (X.GLU 隊) 提供數個常用的矩陣轉換函數。</span><span class="sxs-lookup"><span data-stu-id="3783f-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="3783f-111">您可以使用 GluOrtho2D、標準的透視圖磁片區（使用 [**gluPerspective**](gluperspective.md)），或以指定的 Eyepoint （ [**gluLookAt**](glulookat.md)）為中心的視圖磁片區，設定一個具有 [](gluortho2d.md)的二維正向查看區域。</span><span class="sxs-lookup"><span data-stu-id="3783f-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="3783f-112">這些函式中的每一個都會建立想要的矩陣，並使用 [**glMultMatrix**](glmultmatrix.md)將它套用至目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="3783f-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="3783f-113">[**GluPickMatrix**](glupickmatrix.md)函式會藉由建立矩陣，將繪圖限制在區域的小型區域，以簡化挑選矩陣的選取。</span><span class="sxs-lookup"><span data-stu-id="3783f-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="3783f-114">如果您在套用這個矩陣之後，以選取模式重新轉譯場景，則會選取所有將繪製在游標附近的物件，而這些物件的相關資訊將會儲存在選取範圍緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="3783f-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="3783f-115">如需選取模式的詳細資訊，請參閱 [執行選取](performing-selection-and-feedback.md)專案和意見反應。</span><span class="sxs-lookup"><span data-stu-id="3783f-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="3783f-116">若要判斷要在視窗中繪製物件的位置，請使用 [**gluProject**](gluproject.md)，它會將指定的物件座標 *objx*、 *Objy* 和 *objz* 為使用 *modelMatrix*、 *projMatrix* 和 *視口* 的視窗座標。</span><span class="sxs-lookup"><span data-stu-id="3783f-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="3783f-117">結果會儲存在 *winx*、 *winy* 和 *winz* 中。</span><span class="sxs-lookup"><span data-stu-id="3783f-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="3783f-118">如果函式成功，則傳回值為 GL \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="3783f-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="3783f-119">如果函式失敗，則傳回值為 GL \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="3783f-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="3783f-120">[**GluUnProject**](gluunproject.md)函式會執行反向轉換：它會使用 *modelMatrix*、 *projMatrix* 和 *視口* 來將指定的視窗座標 *winx*、 *winy* 和 *winz* 轉換成物件座標。</span><span class="sxs-lookup"><span data-stu-id="3783f-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="3783f-121">結果會儲存在 *objx*、 *objy* 和 *objz* 中。</span><span class="sxs-lookup"><span data-stu-id="3783f-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="3783f-122">如果函式成功，則傳回值為 GL \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="3783f-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="3783f-123">如果函式失敗，則傳回值為 GL \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="3783f-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 




