---
title: 移植光源和材質函數
description: 適用于光源和材質的 OpenGL 函式與鳶尾花 GL 功能有明顯的差異。 不同于鳶尾花 GL，OpenGL 具有不同的功能，可用於設定燈光、淺色模型和材質。
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- 鳶尾花 GL 移植，光源
- 從鳶尾花 GL、光源移植
- 從鳶尾花 GL （光源）移植至 OpenGL
- 從鳶尾花 GL、光源移植的 OpenGL
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質進行移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL、材質移植的 OpenGL
- 光源
- 材質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840420"
---
# <a name="porting-lighting-and-materials-functions"></a><span data-ttu-id="c8e78-114">移植光源和材質函數</span><span class="sxs-lookup"><span data-stu-id="c8e78-114">Porting Lighting and Materials Functions</span></span>

<span data-ttu-id="c8e78-115">適用于光源和材質的 OpenGL 函式與鳶尾花 GL 功能有明顯的差異。</span><span class="sxs-lookup"><span data-stu-id="c8e78-115">OpenGL functions for lighting and materials differ substantially from the IRIS GL functions.</span></span> <span data-ttu-id="c8e78-116">不同于鳶尾花 GL，OpenGL 具有不同的功能，可用於設定燈光、淺色模型和材質。</span><span class="sxs-lookup"><span data-stu-id="c8e78-116">Unlike IRIS GL, OpenGL has separate functions for setting lights, light models and materials.</span></span>

<span data-ttu-id="c8e78-117">在移植光源和材質功能時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="c8e78-117">Keep the following points in mind when porting lighting and materials functions:</span></span>

-   <span data-ttu-id="c8e78-118">OpenGL 沒有任何已儲存定義的資料表。</span><span class="sxs-lookup"><span data-stu-id="c8e78-118">OpenGL has no table of stored definitions.</span></span> <span data-ttu-id="c8e78-119">您可以使用顯示清單來模仿鳶尾花 GL 定義/系結機制。</span><span class="sxs-lookup"><span data-stu-id="c8e78-119">You can use display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="c8e78-120">如需有關 defs 和系結的詳細資訊，請參閱 [移植 defs、系結和設定](porting-defs--binds--and-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="c8e78-120">For more information on defs and binds, see [Porting Defs, Binds, and Sets](porting-defs--binds--and-sets.md).</span></span>
-   <span data-ttu-id="c8e78-121">使用 OpenGL 時，衰減會與每個光源來源產生關聯，而不是與整體光源模型相關聯。</span><span class="sxs-lookup"><span data-stu-id="c8e78-121">With OpenGL, attenuation is associated with each light source, rather than the overall lighting model.</span></span>
-   <span data-ttu-id="c8e78-122">擴散和反射元件會以 OpenGL light 來源分隔。</span><span class="sxs-lookup"><span data-stu-id="c8e78-122">Diffuse and specular components are separated in OpenGL light sources.</span></span>
-   <span data-ttu-id="c8e78-123">OpenGL light 來源具有 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="c8e78-123">OpenGL light sources have an alpha component.</span></span> <span data-ttu-id="c8e78-124">移植您的鳶尾花 GL 程式碼時，請將此 Alpha 元件設為1.0，指出100% 不透明。</span><span class="sxs-lookup"><span data-stu-id="c8e78-124">When porting your IRIS GL code, set this alpha component to 1.0, indicating 100 percent opaque.</span></span> <span data-ttu-id="c8e78-125">Alpha 值接著會由材質的 Alpha 元件決定，因此場景中的物件看起來會像在鳶尾花 GL 中一樣。</span><span class="sxs-lookup"><span data-stu-id="c8e78-125">The alpha values are then determined by the alpha component of your materials only, so the objects in your scene will look the same as they did in IRIS GL.</span></span>

<span data-ttu-id="c8e78-126">下表列出鳶尾花 GL 光源和材質函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="c8e78-126">The following table lists IRIS GL lighting and materials functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c8e78-127">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="c8e78-127">IRIS GL function</span></span>                 | <span data-ttu-id="c8e78-128">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="c8e78-128">OpenGL function</span></span>                               | <span data-ttu-id="c8e78-129">意義</span><span class="sxs-lookup"><span data-stu-id="c8e78-129">Meaning</span></span>                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8e78-130">**Imdef (DEFLIGHT**，.。。 **)**</span><span class="sxs-lookup"><span data-stu-id="c8e78-130">**Imdef(DEFLIGHT**, ... **)**</span></span>    | [<span data-ttu-id="c8e78-131">glLight</span><span class="sxs-lookup"><span data-stu-id="c8e78-131">glLight</span></span>](gllight-functions.md)              | <span data-ttu-id="c8e78-132">定義燈光來源。</span><span class="sxs-lookup"><span data-stu-id="c8e78-132">Define a light source.</span></span>                                        |
| <span data-ttu-id="c8e78-133">**Imdef (DEFLMODEL**，.。。 **)**</span><span class="sxs-lookup"><span data-stu-id="c8e78-133">**Imdef(DEFLMODEL**, ... **)**</span></span>   | [<span data-ttu-id="c8e78-134">glLightModel</span><span class="sxs-lookup"><span data-stu-id="c8e78-134">glLightModel</span></span>](gllightmodel-functions.md)    | <span data-ttu-id="c8e78-135">定義光源模型。</span><span class="sxs-lookup"><span data-stu-id="c8e78-135">Define a lighting model.</span></span>                                      |
| <span data-ttu-id="c8e78-136">**Imbind**</span><span class="sxs-lookup"><span data-stu-id="c8e78-136">**Imbind**</span></span>                       | <span data-ttu-id="c8e78-137">[**glEnable**](glenable.md) ( GL \_ 燈) </span><span class="sxs-lookup"><span data-stu-id="c8e78-137">[**glEnable**](glenable.md) ( GL\_LIGHT *i*)</span></span> | <span data-ttu-id="c8e78-138">啟用 light *i*。</span><span class="sxs-lookup"><span data-stu-id="c8e78-138">Enable light *i*.</span></span>                                             |
| <span data-ttu-id="c8e78-139">**Imbind**</span><span class="sxs-lookup"><span data-stu-id="c8e78-139">**Imbind**</span></span>                       | <span data-ttu-id="c8e78-140">**glEnable** ( GL \_ 照明 ) </span><span class="sxs-lookup"><span data-stu-id="c8e78-140">**glEnable**( GL\_LIGHTING )</span></span>                  | <span data-ttu-id="c8e78-141">啟用光源。</span><span class="sxs-lookup"><span data-stu-id="c8e78-141">Enable lighting.</span></span>                                              |
| <span data-ttu-id="c8e78-142">**Imdef (DEFMATERIAL**，.。。 **)**</span><span class="sxs-lookup"><span data-stu-id="c8e78-142">**Imdef(DEFMATERIAL**, ... **)**</span></span> | [<span data-ttu-id="c8e78-143">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c8e78-143">**glMaterial**</span></span>](glmaterial-functions.md)    | <span data-ttu-id="c8e78-144">定義材質。</span><span class="sxs-lookup"><span data-stu-id="c8e78-144">Define a material.</span></span>                                            |
| <span data-ttu-id="c8e78-145">**Imcolor**</span><span class="sxs-lookup"><span data-stu-id="c8e78-145">**Imcolor**</span></span>                      | [<span data-ttu-id="c8e78-146">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="c8e78-146">**glColorMaterial**</span></span>](glcolormaterial.md)    | <span data-ttu-id="c8e78-147">變更使用中的色彩命令效果。</span><span class="sxs-lookup"><span data-stu-id="c8e78-147">Change the effect of color commands while lighting is active.</span></span> |
|                                  | [<span data-ttu-id="c8e78-148">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="c8e78-148">**glGetMaterial**</span></span>](glgetmaterial.md)        | <span data-ttu-id="c8e78-149">取得材質參數。</span><span class="sxs-lookup"><span data-stu-id="c8e78-149">Get material parameters.</span></span>                                      |



 

<span data-ttu-id="c8e78-150">下表列出各種鳶尾花 GL 材質參數及其對等的 OpenGL 參數。</span><span class="sxs-lookup"><span data-stu-id="c8e78-150">The following table lists various IRIS GL material parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="c8e78-151">Imdef 索引</span><span class="sxs-lookup"><span data-stu-id="c8e78-151">Imdef index</span></span>  | <span data-ttu-id="c8e78-152">glMaterial 參數</span><span class="sxs-lookup"><span data-stu-id="c8e78-152">glMaterial parameter</span></span>                              | <span data-ttu-id="c8e78-153">預設</span><span class="sxs-lookup"><span data-stu-id="c8e78-153">Default</span></span>              | <span data-ttu-id="c8e78-154">意義</span><span class="sxs-lookup"><span data-stu-id="c8e78-154">Meaning</span></span>                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e78-155">阿 爾 法</span><span class="sxs-lookup"><span data-stu-id="c8e78-155">ALPHA</span></span>        | <span data-ttu-id="c8e78-156">GL \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="c8e78-156">GL\_DIFFUSE</span></span>                                       |                      | <span data-ttu-id="c8e78-157">GL 擴散參數中的第四個值會 \_ 指定 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="c8e78-157">The fourth value in the GL\_DIFFUSE parameter specifies the alpha value.</span></span>                      |
| <span data-ttu-id="c8e78-158">環境</span><span class="sxs-lookup"><span data-stu-id="c8e78-158">AMBIENT</span></span>      | <span data-ttu-id="c8e78-159">GL \_ 環境</span><span class="sxs-lookup"><span data-stu-id="c8e78-159">GL\_AMBIENT</span></span>                                       | <span data-ttu-id="c8e78-160"> (0.2、0.2、0.2、1.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-160">(0.2, 0.2, 0.2, 1.0)</span></span> | <span data-ttu-id="c8e78-161">環境色彩。</span><span class="sxs-lookup"><span data-stu-id="c8e78-161">Ambient color.</span></span>                                                                                |
| <span data-ttu-id="c8e78-162">彌漫 性</span><span class="sxs-lookup"><span data-stu-id="c8e78-162">DIFFUSE</span></span>      | <span data-ttu-id="c8e78-163">GL \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="c8e78-163">GL\_DIFFUSE</span></span>                                       | <span data-ttu-id="c8e78-164"> (0.8、0.8、0.8、1.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-164">(0.8, 0.8, 0.8, 1.0)</span></span> | <span data-ttu-id="c8e78-165">擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="c8e78-165">Diffuse color.</span></span>                                                                                |
| <span data-ttu-id="c8e78-166">鏡面</span><span class="sxs-lookup"><span data-stu-id="c8e78-166">SPECULAR</span></span>     | <span data-ttu-id="c8e78-167">GL \_ 反射</span><span class="sxs-lookup"><span data-stu-id="c8e78-167">GL\_SPECULAR</span></span>                                      | <span data-ttu-id="c8e78-168"> (0.0、0.0、0.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-168">(0.0, 0.0, 0.0, 1.0)</span></span> | <span data-ttu-id="c8e78-169">放射色彩。</span><span class="sxs-lookup"><span data-stu-id="c8e78-169">Emissive color.</span></span>                                                                               |
| <span data-ttu-id="c8e78-170">增</span><span class="sxs-lookup"><span data-stu-id="c8e78-170">SHININESS</span></span>    | <span data-ttu-id="c8e78-171">GL \_ SHININESSGL \_ 環境 \_ 和 \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="c8e78-171">GL\_SHININESSGL\_AMBIENT\_AND\_DIFFUSE</span></span><br/> | <span data-ttu-id="c8e78-172">0.0</span><span class="sxs-lookup"><span data-stu-id="c8e78-172">0.0</span></span>                  | <span data-ttu-id="c8e78-173">反射指數。相當於呼叫具有相同值的 **glMaterial** 兩次。</span><span class="sxs-lookup"><span data-stu-id="c8e78-173">Specular exponent.Equivalent to calling **glMaterial** twice with the same values.</span></span><br/> |
| <span data-ttu-id="c8e78-174">COLORINDEXES</span><span class="sxs-lookup"><span data-stu-id="c8e78-174">COLORINDEXES</span></span> | <span data-ttu-id="c8e78-175">GL \_ 色彩 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="c8e78-175">GL\_COLOR\_INDEXES</span></span>                                |                      | <span data-ttu-id="c8e78-176">環境、擴散和反射光源的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="c8e78-176">Color indexes for ambient, diffuse, and specular lighting.</span></span>                                    |



 

<span data-ttu-id="c8e78-177">當 **Imdef** 的第一個參數為 DEFMODEL 時，對等的 OpenGL 轉譯是函數 [**glLightModel**](gllightmodel-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="c8e78-177">When the first parameter of **Imdef** is DEFMODEL, the equivalent OpenGL translation is the function [**glLightModel**](gllightmodel-functions.md).</span></span> <span data-ttu-id="c8e78-178">例外狀況是在 DEFMODEL 後面的參數是衰減時：接著會 [**glLight**](gllight-functions.md)對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="c8e78-178">The exception is when the parameter following DEFMODEL is ATTENUATION: then the equivalent OpenGL function is [**glLight**](gllight-functions.md).</span></span>

<span data-ttu-id="c8e78-179">下表列出鳶尾花 GL 和 OpenGL 的對等光源模型參數。</span><span class="sxs-lookup"><span data-stu-id="c8e78-179">The following table lists the equivalent lighting model parameters for IRIS GL and OpenGL.</span></span>



| <span data-ttu-id="c8e78-180">Imdef 索引</span><span class="sxs-lookup"><span data-stu-id="c8e78-180">Imdef index</span></span> | <span data-ttu-id="c8e78-181">glLightModel 參數</span><span class="sxs-lookup"><span data-stu-id="c8e78-181">glLightModel parameter</span></span>          | <span data-ttu-id="c8e78-182">預設</span><span class="sxs-lookup"><span data-stu-id="c8e78-182">Default</span></span>              | <span data-ttu-id="c8e78-183">意義</span><span class="sxs-lookup"><span data-stu-id="c8e78-183">Meaning</span></span>                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| <span data-ttu-id="c8e78-184">環境</span><span class="sxs-lookup"><span data-stu-id="c8e78-184">AMBIENT</span></span>     | <span data-ttu-id="c8e78-185">GL \_ LIGHT \_ 模型 \_ 環境</span><span class="sxs-lookup"><span data-stu-id="c8e78-185">GL\_LIGHT\_MODEL\_AMBIENT</span></span>       | <span data-ttu-id="c8e78-186"> (0.2、0.2、0.2、1.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-186">(0.2, 0.2, 0.2, 1.0)</span></span> | <span data-ttu-id="c8e78-187">場景的環境色彩。</span><span class="sxs-lookup"><span data-stu-id="c8e78-187">Ambient color of scene.</span></span>                          |
| <span data-ttu-id="c8e78-188">衰減</span><span class="sxs-lookup"><span data-stu-id="c8e78-188">ATTENUATION</span></span> |                                 |                      | <span data-ttu-id="c8e78-189">請參閱 [**glLight**](gllight-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="c8e78-189">See [**glLight**](gllight-functions.md).</span></span>        |
| <span data-ttu-id="c8e78-190">LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="c8e78-190">LOCALVIEWER</span></span> | <span data-ttu-id="c8e78-191">GL \_ 光 \_ 模型 \_ 本機 \_ 檢視器</span><span class="sxs-lookup"><span data-stu-id="c8e78-191">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span> | <span data-ttu-id="c8e78-192">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="c8e78-192">GL\_FALSE</span></span>            | <span data-ttu-id="c8e78-193">檢視器本機 (**TRUE**) 或無限 (**FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="c8e78-193">Viewer local (**TRUE**) or infinite (**FALSE**).</span></span> |
| <span data-ttu-id="c8e78-194">TWOSIDE</span><span class="sxs-lookup"><span data-stu-id="c8e78-194">TWOSIDE</span></span>     | <span data-ttu-id="c8e78-195">GL \_ LIGHTMODEL \_ 兩 \_ 端</span><span class="sxs-lookup"><span data-stu-id="c8e78-195">GL\_LIGHTMODEL\_TWO\_SIDE</span></span>       | <span data-ttu-id="c8e78-196">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="c8e78-196">GL\_FALSE</span></span>            | <span data-ttu-id="c8e78-197">當 **為 TRUE** 時，請使用雙面光源。</span><span class="sxs-lookup"><span data-stu-id="c8e78-197">Use two-sided lighting when **TRUE**.</span></span>            |



 

<span data-ttu-id="c8e78-198">當 **Imdef** 的第一個參數為 DEFLIGHT 時，對等的 OpenGL 轉譯為 [**glLight**](gllight-functions.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="c8e78-198">When the first parameter of **Imdef** is DEFLIGHT, the equivalent OpenGL translation is the [**glLight**](gllight-functions.md) function.</span></span>

<span data-ttu-id="c8e78-199">下表列出鳶尾花 GL 和 OpenGL 的對等光源參數。</span><span class="sxs-lookup"><span data-stu-id="c8e78-199">The following table lists the equivalent lighting parameters for IRIS GL and OpenGL.</span></span>



| <span data-ttu-id="c8e78-200">Imdef 索引</span><span class="sxs-lookup"><span data-stu-id="c8e78-200">Imdef index</span></span>           | <span data-ttu-id="c8e78-201">glLight 參數</span><span class="sxs-lookup"><span data-stu-id="c8e78-201">glLight parameter</span></span>                                                                                 | <span data-ttu-id="c8e78-202">預設</span><span class="sxs-lookup"><span data-stu-id="c8e78-202">Default</span></span>                                                                             | <span data-ttu-id="c8e78-203">意義</span><span class="sxs-lookup"><span data-stu-id="c8e78-203">Meaning</span></span>                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c8e78-204">環境</span><span class="sxs-lookup"><span data-stu-id="c8e78-204">AMBIENT</span></span>               | <span data-ttu-id="c8e78-205">GL \_ AMBIENTGL \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="c8e78-205">GL\_AMBIENTGL\_DIFFUSE</span></span><br/> <span data-ttu-id="c8e78-206">GL \_ 反射</span><span class="sxs-lookup"><span data-stu-id="c8e78-206">GL\_SPECULAR</span></span><br/>                                         | <span data-ttu-id="c8e78-207"> (0.0、0.0、0.0、1.0)  (1.0、1.0、1.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-207">(0.0, 0.0, 0.0, 1.0)(1.0, 1.0, 1.0, 1.0)</span></span><br/> <span data-ttu-id="c8e78-208"> (1.0、1.0、1.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-208">(1.0, 1.0, 1.0, 1.0)</span></span><br/> | <span data-ttu-id="c8e78-209">環境濃度。擴散濃度。</span><span class="sxs-lookup"><span data-stu-id="c8e78-209">Ambient intensity.Diffuse intensity.</span></span><br/> <span data-ttu-id="c8e78-210">反射濃度。</span><span class="sxs-lookup"><span data-stu-id="c8e78-210">Specular intensity.</span></span><br/> |
| <span data-ttu-id="c8e78-211">LCOLOR</span><span class="sxs-lookup"><span data-stu-id="c8e78-211">LCOLOR</span></span>                | <span data-ttu-id="c8e78-212">沒有同等項目。</span><span class="sxs-lookup"><span data-stu-id="c8e78-212">No equivalent.</span></span>                                                                                    |                                                                                     |                                                                                |
| <span data-ttu-id="c8e78-213">POSITION</span><span class="sxs-lookup"><span data-stu-id="c8e78-213">POSITION</span></span>              | <span data-ttu-id="c8e78-214">GL \_ 位置</span><span class="sxs-lookup"><span data-stu-id="c8e78-214">GL\_POSITION</span></span>                                                                                      | <span data-ttu-id="c8e78-215"> (0.0、0.0、1.0、0.0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-215">(0.0, 0.0, 1.0, 0.0)</span></span>                                                                | <span data-ttu-id="c8e78-216">光源的位置。</span><span class="sxs-lookup"><span data-stu-id="c8e78-216">Position of light.</span></span>                                                             |
| <span data-ttu-id="c8e78-217">SPOTDIRECTION</span><span class="sxs-lookup"><span data-stu-id="c8e78-217">SPOTDIRECTION</span></span>         | <span data-ttu-id="c8e78-218">GL \_ 點 \_ 方向</span><span class="sxs-lookup"><span data-stu-id="c8e78-218">GL\_SPOT\_DIRECTION</span></span>                                                                               | <span data-ttu-id="c8e78-219"> (0、0、1) </span><span class="sxs-lookup"><span data-stu-id="c8e78-219">(0, 0, 1)</span></span>                                                                           | <span data-ttu-id="c8e78-220">焦點方向。</span><span class="sxs-lookup"><span data-stu-id="c8e78-220">Direction of spotlight.</span></span>                                                        |
| <span data-ttu-id="c8e78-221">聚光燈</span><span class="sxs-lookup"><span data-stu-id="c8e78-221">SPOTLIGHT</span></span>             | <span data-ttu-id="c8e78-222">GL \_ 點 \_ EXPONENTGL \_ 點 \_ 截止</span><span class="sxs-lookup"><span data-stu-id="c8e78-222">GL\_SPOT\_EXPONENTGL\_SPOT\_CUTOFF</span></span><br/>                                                     | <span data-ttu-id="c8e78-223">0180</span><span class="sxs-lookup"><span data-stu-id="c8e78-223">0180</span></span><br/>                                                                     | <span data-ttu-id="c8e78-224">濃度分佈。光線來源的最大散佈角度。</span><span class="sxs-lookup"><span data-stu-id="c8e78-224">Intensity distribution.Maximum spread angle of light source.</span></span><br/>        |
| <span data-ttu-id="c8e78-225">DEFMODEL、衰減</span><span class="sxs-lookup"><span data-stu-id="c8e78-225">DEFMODEL, ATTENUATION</span></span> | <span data-ttu-id="c8e78-226">GL \_ 常數 \_ ATTENUATIONGL \_ 線性 \_ 衰減</span><span class="sxs-lookup"><span data-stu-id="c8e78-226">GL\_CONSTANT\_ATTENUATIONGL\_LINEAR\_ATTENUATION</span></span><br/> <span data-ttu-id="c8e78-227">GL \_ 二次 \_ 衰減</span><span class="sxs-lookup"><span data-stu-id="c8e78-227">GL\_QUADRATIC\_ATTENUATION</span></span><br/> | <span data-ttu-id="c8e78-228"> (1、0、0) </span><span class="sxs-lookup"><span data-stu-id="c8e78-228">(1, 0, 0)</span></span>                                                                           | <span data-ttu-id="c8e78-229">衰減因素。</span><span class="sxs-lookup"><span data-stu-id="c8e78-229">Attenuation factors.</span></span>                                                           |



 

 

 





