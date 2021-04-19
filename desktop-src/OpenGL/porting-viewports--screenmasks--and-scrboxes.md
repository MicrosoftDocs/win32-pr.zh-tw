---
title: 移植區、Screenmasks 和 Scrboxes
description: 下列鳶尾花 GL 視口函數沒有 OpenGL 對等函式
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- 鳶尾花 GL 移植，視口函數
- 從鳶尾花 GL、視口函數移植
- 從鳶尾花 GL （視口函式）移植至 OpenGL
- 從鳶尾花 GL、視口函式移植的 OpenGL
- 視口函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968214"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="91e01-108">移植區、Screenmasks 和 Scrboxes</span><span class="sxs-lookup"><span data-stu-id="91e01-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="91e01-109">下列鳶尾花 GL 視口函數沒有 OpenGL 對等專案：</span><span class="sxs-lookup"><span data-stu-id="91e01-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="91e01-110">**reshapeviewport**</span><span class="sxs-lookup"><span data-stu-id="91e01-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="91e01-111">**scrbox**</span><span class="sxs-lookup"><span data-stu-id="91e01-111">**scrbox**</span></span>
-   <span data-ttu-id="91e01-112">**getscrbox**</span><span class="sxs-lookup"><span data-stu-id="91e01-112">**getscrbox**</span></span>

<span data-ttu-id="91e01-113">使用鳶尾花 GL **視口** 函式時，您可以指定區座標的 x 座標 (（以圖元為單位），以及頂端和底部的 y 座標（以圖元為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="91e01-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="91e01-114">不過，使用 OpenGL [**glViewport**](glviewport.md) 函式時，您可以將的 x 和 y (座標（以圖元為單位）指定為以圖元) 為單位的矩形，以及其寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="91e01-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="91e01-115">下表列出鳶尾花 GL 視口函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="91e01-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="91e01-116">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="91e01-116">IRIS GL function</span></span>                          | <span data-ttu-id="91e01-117">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="91e01-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="91e01-118">意義</span><span class="sxs-lookup"><span data-stu-id="91e01-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="91e01-119">**視口** ( 左、右、下、頂端 ) </span><span class="sxs-lookup"><span data-stu-id="91e01-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="91e01-120">[**glViewport**](glviewport.md) ( x、y、寬度、高度 ) </span><span class="sxs-lookup"><span data-stu-id="91e01-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="91e01-121">設定 [區]。</span><span class="sxs-lookup"><span data-stu-id="91e01-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="91e01-122">**popviewportpushviewport**</span><span class="sxs-lookup"><span data-stu-id="91e01-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="91e01-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL \_ 區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="91e01-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="91e01-124">推送和 pop 堆疊。</span><span class="sxs-lookup"><span data-stu-id="91e01-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="91e01-125">**getviewport**</span><span class="sxs-lookup"><span data-stu-id="91e01-125">**getviewport**</span></span>                           | <span data-ttu-id="91e01-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 區 ) </span><span class="sxs-lookup"><span data-stu-id="91e01-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="91e01-127">傳回視口維度。</span><span class="sxs-lookup"><span data-stu-id="91e01-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="91e01-128">??</span><span class="sxs-lookup"><span data-stu-id="91e01-128">??</span></span>

 

 





