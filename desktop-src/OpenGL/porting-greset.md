---
title: 移植 greset
description: OpenGL 將鳶尾花 GL 函數 greset 取代為函數 glPushAttrib 和 glPopAttrib。
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- 鳶尾花 GL 移植，狀態變數
- 從鳶尾花 GL、狀態變數移植
- 從鳶尾花 GL、狀態變數移植至 OpenGL
- 從鳶尾花 GL、狀態變數移植的 OpenGL
- 狀態變數
- 鳶尾花 GL 移植，greset 函式
- 從鳶尾花 GL、greset 函式移植
- 從鳶尾花 GL、greset 函式移植至 OpenGL
- 從鳶尾花 GL、greset 函式移植的 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372371"
---
# <a name="porting-greset"></a><span data-ttu-id="de0a3-112">移植 greset</span><span class="sxs-lookup"><span data-stu-id="de0a3-112">Porting greset</span></span>

<span data-ttu-id="de0a3-113">OpenGL 將鳶尾花 GL 函數 **greset** 取代為函數 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)。</span><span class="sxs-lookup"><span data-stu-id="de0a3-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="de0a3-114">使用這些函式來儲存及還原狀態變數的群組。</span><span class="sxs-lookup"><span data-stu-id="de0a3-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="de0a3-115">例如，</span><span class="sxs-lookup"><span data-stu-id="de0a3-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="de0a3-116">這個範例會採用位 OR 的符號常數，指出要推送至屬性堆疊的狀態變數群組。</span><span class="sxs-lookup"><span data-stu-id="de0a3-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="de0a3-117">每個常數都會參考一組狀態變數。</span><span class="sxs-lookup"><span data-stu-id="de0a3-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="de0a3-118">下表顯示具有對等符號常數名稱的屬性群組。</span><span class="sxs-lookup"><span data-stu-id="de0a3-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="de0a3-119">如需與每個常數相關聯之 OpenGL 狀態變數的完整清單，請參閱 [**glPushAttrib**](glpushattrib.md)。</span><span class="sxs-lookup"><span data-stu-id="de0a3-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="de0a3-120">屬性</span><span class="sxs-lookup"><span data-stu-id="de0a3-120">Attribute</span></span>                       | <span data-ttu-id="de0a3-121">常數</span><span class="sxs-lookup"><span data-stu-id="de0a3-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="de0a3-122">累積緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="de0a3-122">accumulation buffer clear value</span></span> | <span data-ttu-id="de0a3-123">GL \_ ACCUM \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="de0a3-124">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="de0a3-124">color buffer</span></span>                    | <span data-ttu-id="de0a3-125">GL \_ 色彩 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="de0a3-126">目前的</span><span class="sxs-lookup"><span data-stu-id="de0a3-126">current</span></span>                         | <span data-ttu-id="de0a3-127">GL \_ 目前 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="de0a3-128">深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="de0a3-128">depth buffer</span></span>                    | <span data-ttu-id="de0a3-129">GL \_ 深度 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="de0a3-130">enable</span><span class="sxs-lookup"><span data-stu-id="de0a3-130">enable</span></span>                          | <span data-ttu-id="de0a3-131">GL \_ 啟用 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="de0a3-132">評估工具</span><span class="sxs-lookup"><span data-stu-id="de0a3-132">evaluators</span></span>                      | <span data-ttu-id="de0a3-133">EGL \_ VAL \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="de0a3-134">霧</span><span class="sxs-lookup"><span data-stu-id="de0a3-134">fog</span></span>                             | <span data-ttu-id="de0a3-135">GL \_ 霧化 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="de0a3-136">GL \_ 清單 \_ 基礎設定</span><span class="sxs-lookup"><span data-stu-id="de0a3-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="de0a3-137">GL \_ 清單 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="de0a3-138">提示變數</span><span class="sxs-lookup"><span data-stu-id="de0a3-138">hint variables</span></span>                  | <span data-ttu-id="de0a3-139">GL \_ 提示 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="de0a3-140">光源變數</span><span class="sxs-lookup"><span data-stu-id="de0a3-140">lighting variables</span></span>              | <span data-ttu-id="de0a3-141">GL \_ 照明 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="de0a3-142">線條繪圖模式</span><span class="sxs-lookup"><span data-stu-id="de0a3-142">line drawing mode</span></span>               | <span data-ttu-id="de0a3-143">GL \_ 行 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="de0a3-144">圖元模式變數</span><span class="sxs-lookup"><span data-stu-id="de0a3-144">pixel mode variables</span></span>            | <span data-ttu-id="de0a3-145">GL \_ 圖元 \_ 模式 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="de0a3-146">點變數</span><span class="sxs-lookup"><span data-stu-id="de0a3-146">point variables</span></span>                 | <span data-ttu-id="de0a3-147">GL \_ 點 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="de0a3-148">多邊形</span><span class="sxs-lookup"><span data-stu-id="de0a3-148">polygon</span></span>                         | <span data-ttu-id="de0a3-149">GL \_ 多邊形 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="de0a3-150">多邊形 stipple</span><span class="sxs-lookup"><span data-stu-id="de0a3-150">polygon stipple</span></span>                 | <span data-ttu-id="de0a3-151">GL \_ 多邊形 \_ STIPPLE \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="de0a3-152">剪刀</span><span class="sxs-lookup"><span data-stu-id="de0a3-152">scissor</span></span>                         | <span data-ttu-id="de0a3-153">GL \_ 剪式 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="de0a3-154">樣板緩衝區</span><span class="sxs-lookup"><span data-stu-id="de0a3-154">stencil buffer</span></span>                  | <span data-ttu-id="de0a3-155">GL \_ 樣板 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="de0a3-156">紋理</span><span class="sxs-lookup"><span data-stu-id="de0a3-156">texture</span></span>                         | <span data-ttu-id="de0a3-157">GL \_ 材質 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="de0a3-158">Transform - 轉換</span><span class="sxs-lookup"><span data-stu-id="de0a3-158">transform</span></span>                       | <span data-ttu-id="de0a3-159">GL \_ 轉換 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="de0a3-160">Viewport - 檢視區</span><span class="sxs-lookup"><span data-stu-id="de0a3-160">viewport</span></span>                        | <span data-ttu-id="de0a3-161">GL \_ 區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="de0a3-162">GL \_ 所有 \_ ATTRIB \_ 位</span><span class="sxs-lookup"><span data-stu-id="de0a3-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="de0a3-163">若要將狀態變數的值還原為與最後一個 [**glPushAttrib**](glpushattrib.md)儲存的值，只需呼叫 [**glPopAttrib**](glpopattrib.md)。</span><span class="sxs-lookup"><span data-stu-id="de0a3-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="de0a3-164">您未儲存的變數將保持不變。</span><span class="sxs-lookup"><span data-stu-id="de0a3-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="de0a3-165">屬性堆疊的有限深度至少為16。</span><span class="sxs-lookup"><span data-stu-id="de0a3-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




