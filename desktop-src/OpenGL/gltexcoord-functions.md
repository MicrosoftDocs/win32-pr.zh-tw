---
title: glTexCoord 函式
description: 這些函數會設定目前的材質座標。
ms.assetid: 71eb39f1-e1ad-4b97-83e0-d2670f5a7545
keywords:
- OpenGL、glTexCoord 函式
- OpenGL 參考，glTexCoord 函式
- OpenGL，glTexCoord 函式的參考
- glTexCoord 函式
- OpenGL、材質函數
- OpenGL 參考，材質函數
- OpenGL、材質函數的參考
- 材質函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e9db3aa5a8aa62ba1e581d8a005c1ea6fa72d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371946"
---
# <a name="gltexcoord-functions"></a><span data-ttu-id="bad21-111">glTexCoord 函式</span><span class="sxs-lookup"><span data-stu-id="bad21-111">glTexCoord Functions</span></span>

<span data-ttu-id="bad21-112">這些函數會設定目前的材質座標：</span><span class="sxs-lookup"><span data-stu-id="bad21-112">These functions set the current texture coordinates:</span></span>

-   [<span data-ttu-id="bad21-113">**glTexCoord1d**</span><span class="sxs-lookup"><span data-stu-id="bad21-113">**glTexCoord1d**</span></span>](gltexcoord1d.md)
-   [<span data-ttu-id="bad21-114">**glTexCoord1f**</span><span class="sxs-lookup"><span data-stu-id="bad21-114">**glTexCoord1f**</span></span>](gltexcoord1f.md)
-   [<span data-ttu-id="bad21-115">**glTexCoord1i**</span><span class="sxs-lookup"><span data-stu-id="bad21-115">**glTexCoord1i**</span></span>](gltexcoord1i.md)
-   [<span data-ttu-id="bad21-116">**glTexCoord1s**</span><span class="sxs-lookup"><span data-stu-id="bad21-116">**glTexCoord1s**</span></span>](gltexcoord1s.md)
-   [<span data-ttu-id="bad21-117">**glTexCoord2d**</span><span class="sxs-lookup"><span data-stu-id="bad21-117">**glTexCoord2d**</span></span>](gltexcoord2d.md)
-   [<span data-ttu-id="bad21-118">**glTexCoord2i**</span><span class="sxs-lookup"><span data-stu-id="bad21-118">**glTexCoord2i**</span></span>](gltexcoord2i.md)
-   [<span data-ttu-id="bad21-119">**glTexCoord2s**</span><span class="sxs-lookup"><span data-stu-id="bad21-119">**glTexCoord2s**</span></span>](gltexcoord2s.md)
-   [<span data-ttu-id="bad21-120">**glTexCoord3d**</span><span class="sxs-lookup"><span data-stu-id="bad21-120">**glTexCoord3d**</span></span>](gltexcoord3d.md)
-   [<span data-ttu-id="bad21-121">**glTexCoord3f**</span><span class="sxs-lookup"><span data-stu-id="bad21-121">**glTexCoord3f**</span></span>](gltexcoord3f.md)
-   [<span data-ttu-id="bad21-122">**glTexCoord3i**</span><span class="sxs-lookup"><span data-stu-id="bad21-122">**glTexCoord3i**</span></span>](gltexcoord3i.md)
-   [<span data-ttu-id="bad21-123">**glTexCoord3s**</span><span class="sxs-lookup"><span data-stu-id="bad21-123">**glTexCoord3s**</span></span>](gltexcoord3s.md)
-   [<span data-ttu-id="bad21-124">**glTexCoord4d**</span><span class="sxs-lookup"><span data-stu-id="bad21-124">**glTexCoord4d**</span></span>](gltexcoord4d.md)
-   [<span data-ttu-id="bad21-125">**glTexCoord4f**</span><span class="sxs-lookup"><span data-stu-id="bad21-125">**glTexCoord4f**</span></span>](gltexcoord4f.md)
-   [<span data-ttu-id="bad21-126">**glTexCoord4i**</span><span class="sxs-lookup"><span data-stu-id="bad21-126">**glTexCoord4i**</span></span>](gltexcoord4i.md)
-   [<span data-ttu-id="bad21-127">**glTexCoord4s**</span><span class="sxs-lookup"><span data-stu-id="bad21-127">**glTexCoord4s**</span></span>](gltexcoord4s.md)
-   [<span data-ttu-id="bad21-128">**glTexCoord1dv**</span><span class="sxs-lookup"><span data-stu-id="bad21-128">**glTexCoord1dv**</span></span>](gltexcoord1dv.md)
-   [<span data-ttu-id="bad21-129">**glTexCoord1fv**</span><span class="sxs-lookup"><span data-stu-id="bad21-129">**glTexCoord1fv**</span></span>](gltexcoord1fv.md)
-   [<span data-ttu-id="bad21-130">**glTexCoord1iv**</span><span class="sxs-lookup"><span data-stu-id="bad21-130">**glTexCoord1iv**</span></span>](gltexcoord1iv.md)
-   [<span data-ttu-id="bad21-131">**glTexCoord1sv**</span><span class="sxs-lookup"><span data-stu-id="bad21-131">**glTexCoord1sv**</span></span>](gltexcoord1sv.md)
-   [<span data-ttu-id="bad21-132">**glTexCoord2dv**</span><span class="sxs-lookup"><span data-stu-id="bad21-132">**glTexCoord2dv**</span></span>](gltexcoord2dv.md)
-   [<span data-ttu-id="bad21-133">**glTexCoord2fv**</span><span class="sxs-lookup"><span data-stu-id="bad21-133">**glTexCoord2fv**</span></span>](gltexcoord2fv.md)
-   [<span data-ttu-id="bad21-134">**glTexCoord2iv**</span><span class="sxs-lookup"><span data-stu-id="bad21-134">**glTexCoord2iv**</span></span>](gltexcoord2iv.md)
-   [<span data-ttu-id="bad21-135">**glTexCoord2sv**</span><span class="sxs-lookup"><span data-stu-id="bad21-135">**glTexCoord2sv**</span></span>](gltexcoord2sv.md)
-   [<span data-ttu-id="bad21-136">**glTexCoord3dv**</span><span class="sxs-lookup"><span data-stu-id="bad21-136">**glTexCoord3dv**</span></span>](gltexcoord3dv.md)
-   [<span data-ttu-id="bad21-137">**glTexCoord3fv**</span><span class="sxs-lookup"><span data-stu-id="bad21-137">**glTexCoord3fv**</span></span>](gltexcoord3fv.md)
-   [<span data-ttu-id="bad21-138">**glTexCoord3iv**</span><span class="sxs-lookup"><span data-stu-id="bad21-138">**glTexCoord3iv**</span></span>](gltexcoord3iv.md)
-   [<span data-ttu-id="bad21-139">**glTexCoord3sv**</span><span class="sxs-lookup"><span data-stu-id="bad21-139">**glTexCoord3sv**</span></span>](gltexcoord3sv.md)
-   [<span data-ttu-id="bad21-140">**glTexCoord4dv**</span><span class="sxs-lookup"><span data-stu-id="bad21-140">**glTexCoord4dv**</span></span>](gltexcoord4dv.md)
-   [<span data-ttu-id="bad21-141">**glTexCoord4fv**</span><span class="sxs-lookup"><span data-stu-id="bad21-141">**glTexCoord4fv**</span></span>](gltexcoord4fv.md)
-   [<span data-ttu-id="bad21-142">**glTexCoord4iv**</span><span class="sxs-lookup"><span data-stu-id="bad21-142">**glTexCoord4iv**</span></span>](gltexcoord4iv.md)
-   [<span data-ttu-id="bad21-143">**glTexCoord4sv**</span><span class="sxs-lookup"><span data-stu-id="bad21-143">**glTexCoord4sv**</span></span>](gltexcoord4sv.md)

 

 




