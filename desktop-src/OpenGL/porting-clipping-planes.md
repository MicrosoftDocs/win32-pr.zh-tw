---
title: 移植裁剪平面
description: OpenGL 會以類似鳶尾花 GL 的方式來實行裁剪平面。 此外，您可以在 OpenGL 中查詢裁剪平面。 下表列出鳶尾花 GL 裁剪平面函式及其對等的 OpenGL 函數。
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- 鳶尾花 GL 移植，裁剪平面
- 從鳶尾花 GL 進行移植，裁剪平面
- 從鳶尾花 GL 移植至 OpenGL，裁剪平面
- 從鳶尾花 GL 進行 OpenGL 移植，裁剪平面
- 裁剪平面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675255"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="a3263-110">移植裁剪平面</span><span class="sxs-lookup"><span data-stu-id="a3263-110">Porting Clipping Planes</span></span>

<span data-ttu-id="a3263-111">OpenGL 會以類似鳶尾花 GL 的方式來實行裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="a3263-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="a3263-112">此外，您可以在 OpenGL 中查詢裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="a3263-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="a3263-113">下表列出鳶尾花 GL 裁剪平面函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="a3263-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a3263-114">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="a3263-114">IRIS GL function</span></span>                          | <span data-ttu-id="a3263-115">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="a3263-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="a3263-116">意義</span><span class="sxs-lookup"><span data-stu-id="a3263-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="a3263-117">**clipplane** (i、 **CP \_ ON**、params) </span><span class="sxs-lookup"><span data-stu-id="a3263-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="a3263-118">[**glEnable**](glenable.md) ( GL \_ 剪輯 \_ PLANEi ) </span><span class="sxs-lookup"><span data-stu-id="a3263-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="a3263-119">啟用平面 i 的剪輯。</span><span class="sxs-lookup"><span data-stu-id="a3263-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="a3263-120">**clipplane** ( i、 **CP \_ 定義**、平面 ) </span><span class="sxs-lookup"><span data-stu-id="a3263-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="a3263-121">[**glClipPlane**](glclipplane.md) ( GL \_ 剪輯 \_ PLANEi，平面 ) </span><span class="sxs-lookup"><span data-stu-id="a3263-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="a3263-122">定義裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="a3263-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="a3263-123">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="a3263-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="a3263-124">傳回剪式平面方程式。</span><span class="sxs-lookup"><span data-stu-id="a3263-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="a3263-125">[**glIsEnabled**](glisenabled.md) ( GL \_ 剪輯 \_ PLANEi ) </span><span class="sxs-lookup"><span data-stu-id="a3263-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="a3263-126">如果已啟用剪切平面，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a3263-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="a3263-127">**scrmask**</span><span class="sxs-lookup"><span data-stu-id="a3263-127">**scrmask**</span></span>                               | [<span data-ttu-id="a3263-128">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="a3263-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="a3263-129">定義剪式方塊。</span><span class="sxs-lookup"><span data-stu-id="a3263-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="a3263-130">**getscrmask**</span><span class="sxs-lookup"><span data-stu-id="a3263-130">**getscrmask**</span></span>                            | <span data-ttu-id="a3263-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 剪狀方塊 \_ ) </span><span class="sxs-lookup"><span data-stu-id="a3263-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="a3263-132">傳回目前的剪剪方塊。</span><span class="sxs-lookup"><span data-stu-id="a3263-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="a3263-133">若要開啟剪式測試，請使用 GL 剪下方塊 \_ 作為參數來呼叫 glEnable \_ 。</span><span class="sxs-lookup"><span data-stu-id="a3263-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="a3263-134">??</span><span class="sxs-lookup"><span data-stu-id="a3263-134">??</span></span>

 

 




