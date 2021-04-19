---
title: 翻譯 texgen
description: 鳶尾花 GL 函數 texgen 會轉譯為適用于 OpenGL 的 glTexGen。
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
- 鳶尾花 GL 移植，texgen
- 從鳶尾花 GL、texgen 移植
- 從鳶尾花 GL （texgen）移植至 OpenGL
- 從鳶尾花 GL texgen 的 OpenGL 移植
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999786"
---
# <a name="translating-texgen"></a><span data-ttu-id="7c60f-113">翻譯 texgen</span><span class="sxs-lookup"><span data-stu-id="7c60f-113">Translating texgen</span></span>

<span data-ttu-id="7c60f-114">鳶尾花 GL 函數 **texgen** 會轉譯為適用于 OpenGL 的 [glTexGen](gltexgen-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="7c60f-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="7c60f-115">使用鳶尾花 GL，您可以呼叫 **texgen** 兩次：一次設定模式和平面方程式，以及啟用紋理座標產生。</span><span class="sxs-lookup"><span data-stu-id="7c60f-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="7c60f-116">例如：</span><span class="sxs-lookup"><span data-stu-id="7c60f-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="7c60f-117">使用 OpenGL 時，您會進行三次呼叫：兩個到 **glTexGen** (一次設定模式，一次是設定平面方程式) ，另一次則是 [**glEnable**](glenable.md)。</span><span class="sxs-lookup"><span data-stu-id="7c60f-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="7c60f-118">例如，與上述鳶尾花 GL 程式碼相等的 OpenGL 為：</span><span class="sxs-lookup"><span data-stu-id="7c60f-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="7c60f-119">下表列出鳶尾花 GL 紋理座標名稱及其 OpenGL 對應專案。</span><span class="sxs-lookup"><span data-stu-id="7c60f-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="7c60f-120">鳶尾花 GL 紋理座標</span><span class="sxs-lookup"><span data-stu-id="7c60f-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="7c60f-121">OpenGL 材質座標</span><span class="sxs-lookup"><span data-stu-id="7c60f-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="7c60f-122">glEnable 引數</span><span class="sxs-lookup"><span data-stu-id="7c60f-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="7c60f-123">德克薩斯 \_ 州</span><span class="sxs-lookup"><span data-stu-id="7c60f-123">TX\_S</span></span>                      | <span data-ttu-id="7c60f-124">GL \_ S</span><span class="sxs-lookup"><span data-stu-id="7c60f-124">GL\_S</span></span>                     | <span data-ttu-id="7c60f-125">GL \_ 材質 \_ GEN \_ S</span><span class="sxs-lookup"><span data-stu-id="7c60f-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="7c60f-126">TX \_ T</span><span class="sxs-lookup"><span data-stu-id="7c60f-126">TX\_T</span></span>                      | <span data-ttu-id="7c60f-127">GL \_ T</span><span class="sxs-lookup"><span data-stu-id="7c60f-127">GL\_T</span></span>                     | <span data-ttu-id="7c60f-128">GL \_ 材質 \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="7c60f-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="7c60f-129">TX \_ R</span><span class="sxs-lookup"><span data-stu-id="7c60f-129">TX\_R</span></span>                      | <span data-ttu-id="7c60f-130">GL \_ R</span><span class="sxs-lookup"><span data-stu-id="7c60f-130">GL\_R</span></span>                     | <span data-ttu-id="7c60f-131">GL \_ 材質 \_ GEN \_ R</span><span class="sxs-lookup"><span data-stu-id="7c60f-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="7c60f-132">德克薩斯州 \_ Q</span><span class="sxs-lookup"><span data-stu-id="7c60f-132">TX\_Q</span></span>                      | <span data-ttu-id="7c60f-133">GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="7c60f-133">GL\_Q</span></span>                     | <span data-ttu-id="7c60f-134">GL \_ 材質 \_ GEN \_ Q</span><span class="sxs-lookup"><span data-stu-id="7c60f-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="7c60f-135">下表列出鳶尾花 GL 材質產生模式及其對等的 OpenGL 材質模式和平面名稱。</span><span class="sxs-lookup"><span data-stu-id="7c60f-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="7c60f-136">鳶尾花 GL 材質模式</span><span class="sxs-lookup"><span data-stu-id="7c60f-136">IRIS GL texture mode</span></span> | <span data-ttu-id="7c60f-137">OpenGL 材質模式</span><span class="sxs-lookup"><span data-stu-id="7c60f-137">OpenGL texture mode</span></span> | <span data-ttu-id="7c60f-138">OpenGL 平面名稱</span><span class="sxs-lookup"><span data-stu-id="7c60f-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="7c60f-139">TG \_ 線性</span><span class="sxs-lookup"><span data-stu-id="7c60f-139">TG\_LINEAR</span></span>           | <span data-ttu-id="7c60f-140">GL \_ 物件 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="7c60f-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="7c60f-141">GL \_ 物件 \_ 平面</span><span class="sxs-lookup"><span data-stu-id="7c60f-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="7c60f-142">TG \_ 輪廓</span><span class="sxs-lookup"><span data-stu-id="7c60f-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="7c60f-143">GL \_ 眼 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="7c60f-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="7c60f-144">GL \_ 眼 \_ 平面</span><span class="sxs-lookup"><span data-stu-id="7c60f-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="7c60f-145">TG \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="7c60f-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="7c60f-146">GL \_ 球體 \_ 地圖</span><span class="sxs-lookup"><span data-stu-id="7c60f-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




