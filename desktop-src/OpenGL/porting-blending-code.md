---
title: 移植混合程式碼
description: 在鳶尾花 GL 中，當您同時繪製至前端和後端緩衝區時，會藉由讀取其中一個緩衝區、與該色彩混合，然後將結果寫入兩個緩衝區來進行混合。 但是在 OpenGL 中，每個緩衝區會依序讀取、混合式，然後寫入。
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- 鳶尾花 GL 移植，混合
- 從鳶尾花 GL 進行移植，混合
- 從鳶尾花 GL 移植至 OpenGL，混合
- 從鳶尾花 GL 進行 OpenGL 移植，混合
- 混色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969477"
---
# <a name="porting-blending-code"></a><span data-ttu-id="1e478-109">移植混合程式碼</span><span class="sxs-lookup"><span data-stu-id="1e478-109">Porting Blending Code</span></span>

<span data-ttu-id="1e478-110">在鳶尾花 GL 中，當您同時繪製至前端和後端緩衝區時，會藉由讀取其中一個緩衝區、與該色彩混合，然後將結果寫入兩個緩衝區來進行混合。</span><span class="sxs-lookup"><span data-stu-id="1e478-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="1e478-111">但是在 OpenGL 中，每個緩衝區會依序讀取、混合式，然後寫入。</span><span class="sxs-lookup"><span data-stu-id="1e478-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="1e478-112">下表列出鳶尾花 GL 混合函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="1e478-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="1e478-113">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="1e478-113">IRIS GL function</span></span>  | <span data-ttu-id="1e478-114">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="1e478-114">OpenGL function</span></span>                            | <span data-ttu-id="1e478-115">意義</span><span class="sxs-lookup"><span data-stu-id="1e478-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="1e478-116">[**glEnable**](glenable.md) ( GL \_ BLEND ) </span><span class="sxs-lookup"><span data-stu-id="1e478-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="1e478-117">開啟混色。</span><span class="sxs-lookup"><span data-stu-id="1e478-117">Turns on blending.</span></span>          |
| <span data-ttu-id="1e478-118">**blendfunction**</span><span class="sxs-lookup"><span data-stu-id="1e478-118">**blendfunction**</span></span> | [<span data-ttu-id="1e478-119">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="1e478-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="1e478-120">指定 blend 函數。</span><span class="sxs-lookup"><span data-stu-id="1e478-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="1e478-121">OpenGL **glBlendFunc** 函式和鳶尾花 GL **blendfunction** 函數幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="1e478-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="1e478-122">下表列出鳶尾花 GL blend 因數及其 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="1e478-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="1e478-123">鳶尾花 GL</span><span class="sxs-lookup"><span data-stu-id="1e478-123">IRIS GL</span></span>          | <span data-ttu-id="1e478-124">Opengl</span><span class="sxs-lookup"><span data-stu-id="1e478-124">OpenGL</span></span>                     | <span data-ttu-id="1e478-125">備註</span><span class="sxs-lookup"><span data-stu-id="1e478-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="1e478-126">BF \_ 零</span><span class="sxs-lookup"><span data-stu-id="1e478-126">BF\_ZERO</span></span>         | <span data-ttu-id="1e478-127">GL \_ 零</span><span class="sxs-lookup"><span data-stu-id="1e478-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="1e478-128">BF \_ 一</span><span class="sxs-lookup"><span data-stu-id="1e478-128">BF\_ONE</span></span>          | <span data-ttu-id="1e478-129">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="1e478-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="1e478-130">BF \_ SA</span><span class="sxs-lookup"><span data-stu-id="1e478-130">BF\_SA</span></span>           | <span data-ttu-id="1e478-131">GL \_ SRC \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="1e478-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="1e478-132">BF \_ MSA</span><span class="sxs-lookup"><span data-stu-id="1e478-132">BF\_MSA</span></span>          | <span data-ttu-id="1e478-133">GL \_ 1 \_ 減去 \_ SRC \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="1e478-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="1e478-134">BF \_ DA</span><span class="sxs-lookup"><span data-stu-id="1e478-134">BF\_DA</span></span>           | <span data-ttu-id="1e478-135">GL \_ DST \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="1e478-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="1e478-136">BF \_ MDA</span><span class="sxs-lookup"><span data-stu-id="1e478-136">BF\_MDA</span></span>          | <span data-ttu-id="1e478-137">GL \_ 1 \_ 減去 \_ DST \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="1e478-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="1e478-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="1e478-138">BF\_SC</span></span>           | <span data-ttu-id="1e478-139">GL \_ SRC \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="1e478-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="1e478-140">BF \_ SERVICES.MSC</span><span class="sxs-lookup"><span data-stu-id="1e478-140">BF\_MSC</span></span>          | <span data-ttu-id="1e478-141">GL \_ 1 \_ 減去 \_ SRC \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="1e478-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="1e478-142">僅限目的地。</span><span class="sxs-lookup"><span data-stu-id="1e478-142">Destination only.</span></span> |
| <span data-ttu-id="1e478-143">BF \_ DC</span><span class="sxs-lookup"><span data-stu-id="1e478-143">BF\_DC</span></span>           | <span data-ttu-id="1e478-144">GL \_ DST \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="1e478-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="1e478-145">僅限來源。</span><span class="sxs-lookup"><span data-stu-id="1e478-145">Source only.</span></span>      |
| <span data-ttu-id="1e478-146">BF \_ MDC</span><span class="sxs-lookup"><span data-stu-id="1e478-146">BF\_MDC</span></span>          | <span data-ttu-id="1e478-147">GL \_ 1 \_ 減去 \_ DST \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="1e478-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="1e478-148">僅限來源。</span><span class="sxs-lookup"><span data-stu-id="1e478-148">Source only.</span></span>      |
| <span data-ttu-id="1e478-149">BF \_ MIN \_ SA \_ MDA</span><span class="sxs-lookup"><span data-stu-id="1e478-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="1e478-150">GL \_ SRC \_ ALPHA \_ 飽和</span><span class="sxs-lookup"><span data-stu-id="1e478-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="1e478-151">??</span><span class="sxs-lookup"><span data-stu-id="1e478-151">??</span></span>

 

 




