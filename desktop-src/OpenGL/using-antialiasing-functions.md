---
title: 使用消除鋸齒功能
description: 下表列出鳶尾花 GL 消除鋸齒函式及其對等的 OpenGL 函數。
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- 鳶尾花 GL 移植，消除鋸齒
- 從鳶尾花 GL 移植，消除鋸齒
- 從鳶尾花 GL 移植至 OpenGL，消除鋸齒
- 從鳶尾花 GL 的 OpenGL 移植，消除鋸齒
- 消除鋸齒 (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183308"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="22325-108">使用消除鋸齒功能</span><span class="sxs-lookup"><span data-stu-id="22325-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="22325-109">下表列出鳶尾花 GL 消除鋸齒函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="22325-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="22325-110">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="22325-110">IRIS GL function</span></span> | <span data-ttu-id="22325-111">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="22325-111">OpenGL function</span></span>                                      | <span data-ttu-id="22325-112">意義</span><span class="sxs-lookup"><span data-stu-id="22325-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="22325-113">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="22325-113">**pntsmooth**</span></span>    | <span data-ttu-id="22325-114">[**glEnable**](glenable.md) ( GL \_ 點 \_ 平滑 ) </span><span class="sxs-lookup"><span data-stu-id="22325-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="22325-115">啟用點的消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="22325-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="22325-116">**linesmooth**</span><span class="sxs-lookup"><span data-stu-id="22325-116">**linesmooth**</span></span>   | <span data-ttu-id="22325-117">**glEnable** ( GL \_ 行 \_ 平滑 ) </span><span class="sxs-lookup"><span data-stu-id="22325-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="22325-118">啟用線條的消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="22325-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="22325-119">**polysmooth**</span><span class="sxs-lookup"><span data-stu-id="22325-119">**polysmooth**</span></span>   | <span data-ttu-id="22325-120">[**glEnable**](glenable.md) ( GL \_ 多邊形 \_ 平滑 ) </span><span class="sxs-lookup"><span data-stu-id="22325-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="22325-121">啟用多邊形的消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="22325-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="22325-122">使用對等的 [**glDisable**](gldisable.md) 呼叫來關閉消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="22325-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="22325-123">在鳶尾花 GL 中，您可以藉由呼叫下列方法來控制消除鋸齒的品質：</span><span class="sxs-lookup"><span data-stu-id="22325-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="22325-124">OpenGL 提供類似的 controluse [**glHint**](glhint.md)：</span><span class="sxs-lookup"><span data-stu-id="22325-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="22325-125">其中 *hintMode* 是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="22325-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="22325-126">GL \_ 最好 (使用最高品質的平滑處理。 ) </span><span class="sxs-lookup"><span data-stu-id="22325-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="22325-127">GL 最 \_ 快速 (使用最有效率的凹凸貼圖 ) </span><span class="sxs-lookup"><span data-stu-id="22325-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="22325-128">GL \_ 別 \_ 在意</span><span class="sxs-lookup"><span data-stu-id="22325-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="22325-129">鳶尾花 GL 也會藉由呼叫下列內容來允許結束修正：</span><span class="sxs-lookup"><span data-stu-id="22325-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="22325-130">OpenGL 對此函式沒有對等專案。</span><span class="sxs-lookup"><span data-stu-id="22325-130">OpenGL has no equivalent for this function.</span></span>

 

 




