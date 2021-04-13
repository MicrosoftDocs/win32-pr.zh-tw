---
title: 移植三角形
description: 您可以在 OpenGL 個別三角形、三角形條紋和三角形風扇中繪製三種類型的三角形。
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- 鳶尾花 GL 移植，三角形
- 從鳶尾花 GL、三角形進行移植
- 從鳶尾花 GL （三角形）移植至 OpenGL
- 從鳶尾花 GL （三角形）進行 OpenGL 移植
- 繪圖函數、三角形
- 三角形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301372"
---
# <a name="porting-triangles"></a><span data-ttu-id="0092b-109">移植三角形</span><span class="sxs-lookup"><span data-stu-id="0092b-109">Porting Triangles</span></span>

<span data-ttu-id="0092b-110">您可以在 OpenGL 中繪製三種類型的三角形：個別三角形、三角形條紋和三角形風扇。</span><span class="sxs-lookup"><span data-stu-id="0092b-110">You can draw three types of triangles in OpenGL: separate triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="0092b-111">OpenGL 對鳶尾花 GL **swaptmesh** 函數沒有對等專案。</span><span class="sxs-lookup"><span data-stu-id="0092b-111">OpenGL has no equivalent for the IRIS GL **swaptmesh** function.</span></span> <span data-ttu-id="0092b-112">您可以使用三角形、三角形條紋和三角形風扇的組合來達成相同的效果。</span><span class="sxs-lookup"><span data-stu-id="0092b-112">You can achieve the same effect using a combination of triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="0092b-113">下表列出用來繪製三角形的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="0092b-113">The following table lists the IRIS GL functions for drawing triangles and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0092b-114">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="0092b-114">IRIS GL function</span></span>           | <span data-ttu-id="0092b-115">對等的 glBegin 參數</span><span class="sxs-lookup"><span data-stu-id="0092b-115">Equivalent glBegin parameter</span></span> | <span data-ttu-id="0092b-116">意義</span><span class="sxs-lookup"><span data-stu-id="0092b-116">Meaning</span></span>                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | <span data-ttu-id="0092b-117">GL \_ 三角形</span><span class="sxs-lookup"><span data-stu-id="0092b-117">GL\_TRIANGLES</span></span>                | <span data-ttu-id="0092b-118">被解釋為三角形的三倍頂點。</span><span class="sxs-lookup"><span data-stu-id="0092b-118">Triples of vertices interpreted as triangles.</span></span> |
| <span data-ttu-id="0092b-119">**bgntmesh**、 **endtmesh**</span><span class="sxs-lookup"><span data-stu-id="0092b-119">**bgntmesh**, **endtmesh**</span></span> | <span data-ttu-id="0092b-120">GL \_ 三角形 \_ 條紋</span><span class="sxs-lookup"><span data-stu-id="0092b-120">GL\_TRIANGLE\_STRIP</span></span>          | <span data-ttu-id="0092b-121">三角形的連結去除。</span><span class="sxs-lookup"><span data-stu-id="0092b-121">Linked strips of triangles.</span></span>                   |
|                            | <span data-ttu-id="0092b-122">GL \_ 三角形 \_ 風扇</span><span class="sxs-lookup"><span data-stu-id="0092b-122">GL\_TRIANGLE\_FAN</span></span>            | <span data-ttu-id="0092b-123">三角形的連結風扇。</span><span class="sxs-lookup"><span data-stu-id="0092b-123">Linked fans of triangles.</span></span>                     |



 

<span data-ttu-id="0092b-124">??</span><span class="sxs-lookup"><span data-stu-id="0092b-124">??</span></span>

 

 




