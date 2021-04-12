---
title: 移植球體
description: 將球體移植至 OpenGL 時，請記住下列幾點
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- 鳶尾花 GL 移植，球體
- 從鳶尾花 GL、球體進行移植
- 從鳶尾花 GL （球體）移植至 OpenGL
- 從鳶尾花 GL （球體）進行 OpenGL 移植
- 繪圖函數，球體
- 領域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372361"
---
# <a name="porting-spheres"></a><span data-ttu-id="edc2f-109">移植球體</span><span class="sxs-lookup"><span data-stu-id="edc2f-109">Porting Spheres</span></span>

<span data-ttu-id="edc2f-110">將球體移植至 OpenGL 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="edc2f-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="edc2f-111">您無法控制用來繪製球體的基本類型。</span><span class="sxs-lookup"><span data-stu-id="edc2f-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="edc2f-112">您可以用另一種方式控制繪圖精確度：使用配量和堆疊參數。</span><span class="sxs-lookup"><span data-stu-id="edc2f-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="edc2f-113">配量為 longitudinal;堆疊為 latitudinal。</span><span class="sxs-lookup"><span data-stu-id="edc2f-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="edc2f-114">球體繪製于原點中央。</span><span class="sxs-lookup"><span data-stu-id="edc2f-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="edc2f-115">與其使用鳶尾花 GL **sphdraw** 函式來指定位置，請在 x.glu 隊 [**gluSphere**](glusphere.md) 函式的呼叫之前加上翻譯。</span><span class="sxs-lookup"><span data-stu-id="edc2f-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="edc2f-116">此球體程式庫尚未適用于 OpenGL。</span><span class="sxs-lookup"><span data-stu-id="edc2f-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="edc2f-117">下表列出用來繪製球體的鳶尾花 GL 函式，以及其對等的 X.GLU 隊函式（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="edc2f-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="edc2f-118">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="edc2f-118">IRIS GL function</span></span> | <span data-ttu-id="edc2f-119">X.GLU 隊函式</span><span class="sxs-lookup"><span data-stu-id="edc2f-119">GLU function</span></span>                                 | <span data-ttu-id="edc2f-120">意義</span><span class="sxs-lookup"><span data-stu-id="edc2f-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="edc2f-121">**sphobj**</span><span class="sxs-lookup"><span data-stu-id="edc2f-121">**sphobj**</span></span>       | [<span data-ttu-id="edc2f-122">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="edc2f-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="edc2f-123">建立新的球體物件。</span><span class="sxs-lookup"><span data-stu-id="edc2f-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="edc2f-124">**sphfree**</span><span class="sxs-lookup"><span data-stu-id="edc2f-124">**sphfree**</span></span>      | [<span data-ttu-id="edc2f-125">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="edc2f-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="edc2f-126">刪除球體物件和使用的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="edc2f-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="edc2f-127">**sphdraw**</span><span class="sxs-lookup"><span data-stu-id="edc2f-127">**sphdraw**</span></span>      | [<span data-ttu-id="edc2f-128">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="edc2f-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="edc2f-129">繪製球體。</span><span class="sxs-lookup"><span data-stu-id="edc2f-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="edc2f-130">**sphmode**</span><span class="sxs-lookup"><span data-stu-id="edc2f-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="edc2f-131">設定球體屬性。</span><span class="sxs-lookup"><span data-stu-id="edc2f-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="edc2f-132">**sphrotmatrix**</span><span class="sxs-lookup"><span data-stu-id="edc2f-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="edc2f-133">控制球體方向。</span><span class="sxs-lookup"><span data-stu-id="edc2f-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="edc2f-134">**sphgnpolys**</span><span class="sxs-lookup"><span data-stu-id="edc2f-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="edc2f-135">傳回目前球體中的多邊形數目。</span><span class="sxs-lookup"><span data-stu-id="edc2f-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="edc2f-136">??</span><span class="sxs-lookup"><span data-stu-id="edc2f-136">??</span></span>

 

 




