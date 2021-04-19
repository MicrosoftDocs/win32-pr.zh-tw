---
title: 移植挑選函數
description: 所有鳶尾花 GL 挑選函式都有 OpenGL 對等專案，但 clearhitcode 除外。 下表列出鳶尾花 GL 挑選函數及其對等的 OpenGL 函數。
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- 鳶尾花 GL 移植，挑選
- 從鳶尾花 GL 進行移植，挑選
- 從鳶尾花 GL 移植至 OpenGL，挑選
- 鳶尾花 GL 的 OpenGL 移植，挑選
- 採摘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968241"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="378a4-109">移植挑選函數</span><span class="sxs-lookup"><span data-stu-id="378a4-109">Porting Picking Functions</span></span>

<span data-ttu-id="378a4-110">所有鳶尾花 GL 挑選函式都有 OpenGL 對等專案，但 **clearhitcode** 除外。</span><span class="sxs-lookup"><span data-stu-id="378a4-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="378a4-111">下表列出鳶尾花 GL 挑選函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="378a4-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="378a4-112">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="378a4-112">IRIS GL function</span></span>                | <span data-ttu-id="378a4-113">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="378a4-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="378a4-114">意義</span><span class="sxs-lookup"><span data-stu-id="378a4-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="378a4-115">**clearhitcode**</span><span class="sxs-lookup"><span data-stu-id="378a4-115">**clearhitcode**</span></span>                | <span data-ttu-id="378a4-116">不支援。</span><span class="sxs-lookup"><span data-stu-id="378a4-116">Not supported.</span></span>                                                                            | <span data-ttu-id="378a4-117">清除全域變數和 hitcode。</span><span class="sxs-lookup"><span data-stu-id="378a4-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="378a4-118">**pickselect**</span><span class="sxs-lookup"><span data-stu-id="378a4-118">**pickselect**</span></span><br/>       | <span data-ttu-id="378a4-119">[**glRenderMode**](glrendermode.md) ( GL \_ 選取 ) </span><span class="sxs-lookup"><span data-stu-id="378a4-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="378a4-120">切換至選取範圍或挑選模式。</span><span class="sxs-lookup"><span data-stu-id="378a4-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="378a4-121">**enDPIckendselect**</span><span class="sxs-lookup"><span data-stu-id="378a4-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="378a4-122">[**glRenderMode**](glrendermode.md) ( GL 轉譯 \_ ) </span><span class="sxs-lookup"><span data-stu-id="378a4-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="378a4-123">切換至轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="378a4-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="378a4-124">**picksize**</span><span class="sxs-lookup"><span data-stu-id="378a4-124">**picksize**</span></span>                    | <span data-ttu-id="378a4-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="378a4-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="378a4-126">設定傳回陣列。</span><span class="sxs-lookup"><span data-stu-id="378a4-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="378a4-127">**initnames**</span><span class="sxs-lookup"><span data-stu-id="378a4-127">**initnames**</span></span>                   | [<span data-ttu-id="378a4-128">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="378a4-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="378a4-129">**pushnamepopname**</span><span class="sxs-lookup"><span data-stu-id="378a4-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="378a4-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="378a4-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="378a4-131">**loadname**</span><span class="sxs-lookup"><span data-stu-id="378a4-131">**loadname**</span></span>                    | [<span data-ttu-id="378a4-132">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="378a4-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="378a4-133">如需有關挑選的詳細資訊，請參閱 [**gluPickMatrix**](glupickmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="378a4-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





