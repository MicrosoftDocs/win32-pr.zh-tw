---
title: 移植修剪曲線
description: OpenGL 修剪曲線與鳶尾花 GL 修剪曲線非常類似。 下表列出用來定義修剪曲線和其相等 OpenGL 函數的鳶尾花 GL 函數。
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- 鳶尾花 GL 移植，修剪曲線
- 從鳶尾花 GL （修剪曲線）進行移植
- 從鳶尾花 GL 移植至 OpenGL，修剪曲線
- 從鳶尾花 GL （修剪曲線）進行 OpenGL 移植
- 修剪曲線
- 曲線
- 鳶尾花 GL 移植，曲線
- 從鳶尾花 GL、曲線移植
- 從鳶尾花 GL （曲線）移植至 OpenGL
- 從鳶尾花 GL、曲線移植的 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183894"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="c0638-114">移植修剪曲線</span><span class="sxs-lookup"><span data-stu-id="c0638-114">Porting Trimming Curves</span></span>

<span data-ttu-id="c0638-115">OpenGL 修剪曲線與鳶尾花 GL 修剪曲線非常類似。</span><span class="sxs-lookup"><span data-stu-id="c0638-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="c0638-116">下表列出用來定義修剪曲線和其相等 OpenGL 函數的鳶尾花 GL 函數。</span><span class="sxs-lookup"><span data-stu-id="c0638-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c0638-117">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="c0638-117">IRIS GL function</span></span> | <span data-ttu-id="c0638-118">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="c0638-118">OpenGL function</span></span>                        | <span data-ttu-id="c0638-119">意義</span><span class="sxs-lookup"><span data-stu-id="c0638-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="c0638-120">**bgntrim**</span><span class="sxs-lookup"><span data-stu-id="c0638-120">**bgntrim**</span></span>      | [<span data-ttu-id="c0638-121">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="c0638-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="c0638-122">開始修剪曲線的定義。</span><span class="sxs-lookup"><span data-stu-id="c0638-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="c0638-123">**pwlcurve**</span><span class="sxs-lookup"><span data-stu-id="c0638-123">**pwlcurve**</span></span>     | [<span data-ttu-id="c0638-124">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="c0638-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="c0638-125">定義分段線性曲線。</span><span class="sxs-lookup"><span data-stu-id="c0638-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="c0638-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="c0638-126">**nurbscurve**</span></span>   | [<span data-ttu-id="c0638-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="c0638-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="c0638-128">指定修剪曲線屬性。</span><span class="sxs-lookup"><span data-stu-id="c0638-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="c0638-129">**endtrim**</span><span class="sxs-lookup"><span data-stu-id="c0638-129">**endtrim**</span></span>      | [<span data-ttu-id="c0638-130">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="c0638-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="c0638-131">結束修剪曲線的定義。</span><span class="sxs-lookup"><span data-stu-id="c0638-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="c0638-132">??</span><span class="sxs-lookup"><span data-stu-id="c0638-132">??</span></span>

 

 




