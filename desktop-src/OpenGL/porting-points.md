---
title: 移植點
description: OpenGL 沒有可繪製單一點的命令。 否則，移植點函數很簡單。 下表列出繪製點的鳶尾花 GL 函式及其對等的 OpenGL 函數。
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- 鳶尾花 GL 移植，點
- 從鳶尾花 GL、點進行移植
- 從鳶尾花 GL 移植至 OpenGL，點
- 從鳶尾花 GL （點）移植的 OpenGL
- 繪圖函數、點
- 點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969053"
---
# <a name="porting-points"></a><span data-ttu-id="2775a-111">移植點</span><span class="sxs-lookup"><span data-stu-id="2775a-111">Porting Points</span></span>

<span data-ttu-id="2775a-112">OpenGL 沒有可繪製單一點的命令。</span><span class="sxs-lookup"><span data-stu-id="2775a-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="2775a-113">否則，移植點函數很簡單。</span><span class="sxs-lookup"><span data-stu-id="2775a-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="2775a-114">下表列出繪製點的鳶尾花 GL 函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="2775a-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="2775a-115">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="2775a-115">IRIS GL function</span></span>           | <span data-ttu-id="2775a-116">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="2775a-116">OpenGL function</span></span>                                                   | <span data-ttu-id="2775a-117">意義</span><span class="sxs-lookup"><span data-stu-id="2775a-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2775a-118">**pnt**</span><span class="sxs-lookup"><span data-stu-id="2775a-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="2775a-119">繪製單一點。</span><span class="sxs-lookup"><span data-stu-id="2775a-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="2775a-120">**bgnpoint**， **端點**</span><span class="sxs-lookup"><span data-stu-id="2775a-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="2775a-121">[**glBegin**](glbegin.md) ( GL \_ 點 ) 、 [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="2775a-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="2775a-122">將頂點解釋為點。</span><span class="sxs-lookup"><span data-stu-id="2775a-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="2775a-123">**pntsize**</span><span class="sxs-lookup"><span data-stu-id="2775a-123">**pntsize**</span></span>                | [<span data-ttu-id="2775a-124">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="2775a-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="2775a-125">設定點大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2775a-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="2775a-126">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="2775a-126">**pntsmooth**</span></span>              | <span data-ttu-id="2775a-127">[**glEnable**](glenable.md) ( GL \_ 點 \_ 平滑 ) </span><span class="sxs-lookup"><span data-stu-id="2775a-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="2775a-128">開啟點消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="2775a-128">Turns on point antialiasing.</span></span> <span data-ttu-id="2775a-129"> (如需點消除鋸齒的詳細資訊，請參閱 [移植消除鋸齒功能](porting-antialiasing-functions.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="2775a-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="2775a-130">如需相關 get 函數的詳細資訊，請參閱 [**glPointSize**](glpointsize.md)。</span><span class="sxs-lookup"><span data-stu-id="2775a-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="2775a-131">??</span><span class="sxs-lookup"><span data-stu-id="2775a-131">??</span></span>

 

 




