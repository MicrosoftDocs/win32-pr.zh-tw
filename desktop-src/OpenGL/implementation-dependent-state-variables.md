---
title: Implementation-Dependent 狀態變數
description: Implementation-Dependent 狀態變數
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent 狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645702c9ea91f21d0e3bce5233b8014fd8f86859
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909876"
---
# <a name="implementation-dependent-state-variables"></a><span data-ttu-id="20702-104">Implementation-Dependent 狀態變數</span><span class="sxs-lookup"><span data-stu-id="20702-104">Implementation-Dependent State Variables</span></span>

<dl> <span data-ttu-id="20702-105"><dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ 最大 \_ 燈光</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-105"><dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL\_MAX\_LIGHTS</dt> </span></span><dd> 

| <span data-ttu-id="20702-106">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-106">Property</span></span> | <span data-ttu-id="20702-107">值</span><span class="sxs-lookup"><span data-stu-id="20702-107">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="20702-108">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-108">Description:</span></span>     | <span data-ttu-id="20702-109">最大光線數目</span><span class="sxs-lookup"><span data-stu-id="20702-109">Maximum number of lights</span></span>               |
| <span data-ttu-id="20702-110">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-110">Attribute group:</span></span> |                                        |
| <span data-ttu-id="20702-111">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-111">Initial value:</span></span>   | <span data-ttu-id="20702-112">8</span><span class="sxs-lookup"><span data-stu-id="20702-112">8</span></span>                                      |
| <span data-ttu-id="20702-113">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-113">Get command:</span></span>     | [<span data-ttu-id="20702-114">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-114">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="20702-115"></dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL \_ 最大 \_ 剪輯 \_ 平面</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-115"></dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL\_MAX\_CLIP\_PLANES</dt> </span></span><dd> 

| <span data-ttu-id="20702-116">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-116">Property</span></span> | <span data-ttu-id="20702-117">值</span><span class="sxs-lookup"><span data-stu-id="20702-117">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-118">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-118">Description:</span></span>     | <span data-ttu-id="20702-119">使用者裁剪平面的最大數目</span><span class="sxs-lookup"><span data-stu-id="20702-119">Maximum number of user clipping planes</span></span>                                           |
| <span data-ttu-id="20702-120">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-120">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-121">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-121">Initial value:</span></span>   | <span data-ttu-id="20702-122">6</span><span class="sxs-lookup"><span data-stu-id="20702-122">6</span></span>                                                                                |
| <span data-ttu-id="20702-123">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-123">Get command:</span></span>     | [<span data-ttu-id="20702-124">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-124">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-125"></dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-125"></dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL\_MAX\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="20702-126">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-126">Property</span></span> | <span data-ttu-id="20702-127">值</span><span class="sxs-lookup"><span data-stu-id="20702-127">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-128">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-128">Description:</span></span>     | <span data-ttu-id="20702-129">最大模型-矩陣堆疊深度</span><span class="sxs-lookup"><span data-stu-id="20702-129">Maximum modelview-matrix stack depth</span></span>                                             |
| <span data-ttu-id="20702-130">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-130">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-131">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-131">Initial value:</span></span>   | <span data-ttu-id="20702-132">32</span><span class="sxs-lookup"><span data-stu-id="20702-132">32</span></span>                                                                               |
| <span data-ttu-id="20702-133">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-133">Get command:</span></span>     | [<span data-ttu-id="20702-134">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-134">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-135"></dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-135"></dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL\_MAX\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="20702-136">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-136">Property</span></span> | <span data-ttu-id="20702-137">值</span><span class="sxs-lookup"><span data-stu-id="20702-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-138">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-138">Description:</span></span>     | <span data-ttu-id="20702-139">最大投射矩陣堆疊深度</span><span class="sxs-lookup"><span data-stu-id="20702-139">Maximum projection-matrix stack depth</span></span>                                            |
| <span data-ttu-id="20702-140">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-140">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-141">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-141">Initial value:</span></span>   | <span data-ttu-id="20702-142">2</span><span class="sxs-lookup"><span data-stu-id="20702-142">2</span></span>                                                                                |
| <span data-ttu-id="20702-143">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-143">Get command:</span></span>     | [<span data-ttu-id="20702-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-145"></dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL \_ 最大 \_ 紋理 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-145"></dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL\_MAX\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="20702-146">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-146">Property</span></span> | <span data-ttu-id="20702-147">值</span><span class="sxs-lookup"><span data-stu-id="20702-147">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-148">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-148">Description:</span></span>     | <span data-ttu-id="20702-149">材質矩陣堆疊的深度上限</span><span class="sxs-lookup"><span data-stu-id="20702-149">Maximum depth of texture matrix stack</span></span>                                            |
| <span data-ttu-id="20702-150">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-150">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-151">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-151">Initial value:</span></span>   | <span data-ttu-id="20702-152">2</span><span class="sxs-lookup"><span data-stu-id="20702-152">2</span></span>                                                                                |
| <span data-ttu-id="20702-153">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-153">Get command:</span></span>     | [<span data-ttu-id="20702-154">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-154">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-155"></dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL \_ 子圖元 \_ 位</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-155"></dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL\_SUBPIXEL\_BITS</dt> </span></span><dd> 

| <span data-ttu-id="20702-156">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-156">Property</span></span> | <span data-ttu-id="20702-157">值</span><span class="sxs-lookup"><span data-stu-id="20702-157">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-158">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-158">Description:</span></span>     | <span data-ttu-id="20702-159">以 *x* 和 *y* 表示的子圖元精確度位數</span><span class="sxs-lookup"><span data-stu-id="20702-159">Number of bits of subpixel precision in *x* and *y*</span></span>                              |
| <span data-ttu-id="20702-160">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-160">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-161">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-161">Initial value:</span></span>   | <span data-ttu-id="20702-162">4</span><span class="sxs-lookup"><span data-stu-id="20702-162">4</span></span>                                                                                |
| <span data-ttu-id="20702-163">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-163">Get command:</span></span>     | [<span data-ttu-id="20702-164">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-164">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-165"></dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL \_ 最大 \_ 紋理 \_ 大小</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-165"></dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL\_MAX\_TEXTURE\_SIZE</dt> </span></span><dd> 

| <span data-ttu-id="20702-166">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-166">Property</span></span> | <span data-ttu-id="20702-167">值</span><span class="sxs-lookup"><span data-stu-id="20702-167">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-168">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-168">Description:</span></span>     | <span data-ttu-id="20702-169">材質影像的最大高度或寬度 (沒有框線) </span><span class="sxs-lookup"><span data-stu-id="20702-169">Maximum height or width of a texture image (without borders)</span></span>                     |
| <span data-ttu-id="20702-170">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-170">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-171">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-171">Initial value:</span></span>   | <span data-ttu-id="20702-172">64</span><span class="sxs-lookup"><span data-stu-id="20702-172">64</span></span>                                                                               |
| <span data-ttu-id="20702-173">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-173">Get command:</span></span>     | [<span data-ttu-id="20702-174">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-174">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-175"></dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL \_ 最大 \_ 圖元 \_ 映射 \_ 表</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-175"></dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL\_MAX\_PIXEL\_MAP\_TABLE</dt> </span></span><dd> 

| <span data-ttu-id="20702-176">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-176">Property</span></span> | <span data-ttu-id="20702-177">值</span><span class="sxs-lookup"><span data-stu-id="20702-177">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-178">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-178">Description:</span></span>     | <span data-ttu-id="20702-179">**GlPixelMap** 轉譯資料表的大小上限</span><span class="sxs-lookup"><span data-stu-id="20702-179">Maximum size of a **glPixelMap** translation table</span></span>                               |
| <span data-ttu-id="20702-180">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-180">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-181">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-181">Initial value:</span></span>   | <span data-ttu-id="20702-182">32</span><span class="sxs-lookup"><span data-stu-id="20702-182">32</span></span>                                                                               |
| <span data-ttu-id="20702-183">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-183">Get command:</span></span>     | [<span data-ttu-id="20702-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-185"></dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL \_ 最大 \_ 名稱 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-185"></dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL\_MAX\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="20702-186">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-186">Property</span></span> | <span data-ttu-id="20702-187">值</span><span class="sxs-lookup"><span data-stu-id="20702-187">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-188">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-188">Description:</span></span>     | <span data-ttu-id="20702-189">最大選取範圍-名稱堆疊深度</span><span class="sxs-lookup"><span data-stu-id="20702-189">Maximum selection-name stack depth</span></span>                                               |
| <span data-ttu-id="20702-190">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-190">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-191">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-191">Initial value:</span></span>   | <span data-ttu-id="20702-192">64</span><span class="sxs-lookup"><span data-stu-id="20702-192">64</span></span>                                                                               |
| <span data-ttu-id="20702-193">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-193">Get command:</span></span>     | [<span data-ttu-id="20702-194">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-194">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-195"></dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL \_ 最大 \_ 清單的 \_ 嵌套</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-195"></dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL\_MAX\_LIST\_NESTING</dt> </span></span><dd> 

| <span data-ttu-id="20702-196">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-196">Property</span></span> | <span data-ttu-id="20702-197">值</span><span class="sxs-lookup"><span data-stu-id="20702-197">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-198">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-198">Description:</span></span>     | <span data-ttu-id="20702-199">最大顯示清單呼叫嵌套</span><span class="sxs-lookup"><span data-stu-id="20702-199">Maximum display-list call nesting</span></span>                                                |
| <span data-ttu-id="20702-200">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-200">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-201">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-201">Initial value:</span></span>   | <span data-ttu-id="20702-202">64</span><span class="sxs-lookup"><span data-stu-id="20702-202">64</span></span>                                                                               |
| <span data-ttu-id="20702-203">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-203">Get command:</span></span>     | [<span data-ttu-id="20702-204">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-204">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-205"></dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ 最大 \_ EVAL \_ 順序</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-205"></dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL\_MAX\_EVAL\_ORDER</dt> </span></span><dd> 

| <span data-ttu-id="20702-206">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-206">Property</span></span> | <span data-ttu-id="20702-207">值</span><span class="sxs-lookup"><span data-stu-id="20702-207">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-208">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-208">Description:</span></span>     | <span data-ttu-id="20702-209">最大評估工具多項式順序</span><span class="sxs-lookup"><span data-stu-id="20702-209">Maximum evaluator polynomial order</span></span>                                               |
| <span data-ttu-id="20702-210">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-210">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-211">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-211">Initial value:</span></span>   | <span data-ttu-id="20702-212">8</span><span class="sxs-lookup"><span data-stu-id="20702-212">8</span></span>                                                                                |
| <span data-ttu-id="20702-213">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-213">Get command:</span></span>     | [<span data-ttu-id="20702-214">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-214">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-215"></dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ 最大 \_ 視窗區變 \_ 暗</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-215"></dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL\_MAX\_VIEWPORT\_DIMS</dt> </span></span><dd> 

| <span data-ttu-id="20702-216">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-216">Property</span></span> | <span data-ttu-id="20702-217">值</span><span class="sxs-lookup"><span data-stu-id="20702-217">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-218">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-218">Description:</span></span>     | <span data-ttu-id="20702-219">最大的視口維度</span><span class="sxs-lookup"><span data-stu-id="20702-219">Maximum viewport dimensions</span></span>                                                      |
| <span data-ttu-id="20702-220">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-220">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-221">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-221">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="20702-222">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-222">Get command:</span></span>     | [<span data-ttu-id="20702-223">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-223">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-224"></dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL \_ 最大的 \_ ATTRIB \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-224"></dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL\_MAX\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="20702-225">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-225">Property</span></span> | <span data-ttu-id="20702-226">值</span><span class="sxs-lookup"><span data-stu-id="20702-226">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-227">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-227">Description:</span></span>     | <span data-ttu-id="20702-228">屬性堆疊的最大深度</span><span class="sxs-lookup"><span data-stu-id="20702-228">Maximum depth of the attribute stack</span></span>                                             |
| <span data-ttu-id="20702-229">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-229">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-230">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-230">Initial value:</span></span>   | <span data-ttu-id="20702-231">16</span><span class="sxs-lookup"><span data-stu-id="20702-231">16</span></span>                                                                               |
| <span data-ttu-id="20702-232">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-232">Get command:</span></span>     | [<span data-ttu-id="20702-233">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="20702-233">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-234"></dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL \_ AUX \_ 緩衝區</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-234"></dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL\_AUX\_BUFFERS</dt> </span></span><dd> 

| <span data-ttu-id="20702-235">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-235">Property</span></span> | <span data-ttu-id="20702-236">值</span><span class="sxs-lookup"><span data-stu-id="20702-236">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-237">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-237">Description:</span></span>     | <span data-ttu-id="20702-238">輔助緩衝區數目</span><span class="sxs-lookup"><span data-stu-id="20702-238">Number of auxiliary buffers</span></span>                                                      |
| <span data-ttu-id="20702-239">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-239">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-240">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-240">Initial value:</span></span>   | <span data-ttu-id="20702-241">0</span><span class="sxs-lookup"><span data-stu-id="20702-241">0</span></span>                                                                                |
| <span data-ttu-id="20702-242">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-242">Get command:</span></span>     | [<span data-ttu-id="20702-243">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="20702-243">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-244"></dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL \_ RGBA \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-244"></dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL\_RGBA\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="20702-245">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-245">Property</span></span> | <span data-ttu-id="20702-246">值</span><span class="sxs-lookup"><span data-stu-id="20702-246">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-247">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-247">Description:</span></span>     | <span data-ttu-id="20702-248">如果色彩緩衝區儲存 RGBA，則為 True</span><span class="sxs-lookup"><span data-stu-id="20702-248">True if color buffers store RGBA</span></span>                                                 |
| <span data-ttu-id="20702-249">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-249">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-250">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-250">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="20702-251">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-251">Get command:</span></span>     | [<span data-ttu-id="20702-252">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="20702-252">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-253"></dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL \_ 索引 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-253"></dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL\_INDEX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="20702-254">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-254">Property</span></span> | <span data-ttu-id="20702-255">值</span><span class="sxs-lookup"><span data-stu-id="20702-255">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-256">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-256">Description:</span></span>     | <span data-ttu-id="20702-257">如果色彩緩衝區儲存索引，則為 True</span><span class="sxs-lookup"><span data-stu-id="20702-257">True if color buffers store indexes</span></span>                                              |
| <span data-ttu-id="20702-258">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-258">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-259">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-259">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="20702-260">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-260">Get command:</span></span>     | [<span data-ttu-id="20702-261">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="20702-261">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-262"></dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-262"></dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL\_DOUBLEBUFFER</dt> </span></span><dd> 

| <span data-ttu-id="20702-263">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-263">Property</span></span> | <span data-ttu-id="20702-264">值</span><span class="sxs-lookup"><span data-stu-id="20702-264">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20702-265">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-265">Description:</span></span>     | <span data-ttu-id="20702-266">如果有前端和背景緩衝區存在，則為 True</span><span class="sxs-lookup"><span data-stu-id="20702-266">True if front and back buffers exist</span></span>                                             |
| <span data-ttu-id="20702-267">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-267">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="20702-268">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-268">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="20702-269">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-269">Get command:</span></span>     | [<span data-ttu-id="20702-270">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="20702-270">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-271"></dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ 身歷聲</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-271"></dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL\_STEREO</dt> </span></span><dd> 

| <span data-ttu-id="20702-272">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-272">Property</span></span> | <span data-ttu-id="20702-273">值</span><span class="sxs-lookup"><span data-stu-id="20702-273">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="20702-274">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-274">Description:</span></span>     | <span data-ttu-id="20702-275">如果有左方和右緩衝區存在，則為 True</span><span class="sxs-lookup"><span data-stu-id="20702-275">True if left and right buffers exist</span></span>                                           |
| <span data-ttu-id="20702-276">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-276">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="20702-277">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-277">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="20702-278">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-278">Get command:</span></span>     | [<span data-ttu-id="20702-279">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="20702-279">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-280"></dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL \_ 點數 \_ 大小 \_ 範圍</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-280"></dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL\_POINT\_SIZE\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="20702-281">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-281">Property</span></span> | <span data-ttu-id="20702-282">值</span><span class="sxs-lookup"><span data-stu-id="20702-282">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="20702-283">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-283">Description:</span></span>     | <span data-ttu-id="20702-284">範圍 (低至高) 的反鋸齒點大小</span><span class="sxs-lookup"><span data-stu-id="20702-284">Range (low to high) of antialiased point sizes</span></span>                                 |
| <span data-ttu-id="20702-285">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-285">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="20702-286">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-286">Initial value:</span></span>   | <span data-ttu-id="20702-287">1，1</span><span class="sxs-lookup"><span data-stu-id="20702-287">1, 1</span></span>                                                                           |
| <span data-ttu-id="20702-288">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-288">Get command:</span></span>     | [<span data-ttu-id="20702-289">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="20702-289">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-290"></dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GL \_ 點 \_ 大小 \_ 細微性</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-290"></dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GL\_POINT\_SIZE\_GRANULARITY</dt> </span></span><dd> 

| <span data-ttu-id="20702-291">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-291">Property</span></span> | <span data-ttu-id="20702-292">值</span><span class="sxs-lookup"><span data-stu-id="20702-292">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="20702-293">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-293">Description:</span></span>     | <span data-ttu-id="20702-294">反鋸齒點大小的資料細微性</span><span class="sxs-lookup"><span data-stu-id="20702-294">Antialiased point size granularity</span></span>                                             |
| <span data-ttu-id="20702-295">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-295">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="20702-296">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-296">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="20702-297">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-297">Get command:</span></span>     | [<span data-ttu-id="20702-298">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="20702-298">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-299"></dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL \_ 線條 \_ 寬度 \_ 範圍</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-299"></dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL\_LINE\_WIDTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="20702-300">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-300">Property</span></span> | <span data-ttu-id="20702-301">值</span><span class="sxs-lookup"><span data-stu-id="20702-301">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="20702-302">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-302">Description:</span></span>     | <span data-ttu-id="20702-303">反鋸齒線條寬度的範圍 (低至高) </span><span class="sxs-lookup"><span data-stu-id="20702-303">Range (low to high) of antialiased line widths</span></span>                                 |
| <span data-ttu-id="20702-304">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-304">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="20702-305">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-305">Initial value:</span></span>   | <span data-ttu-id="20702-306">1，1</span><span class="sxs-lookup"><span data-stu-id="20702-306">1, 1</span></span>                                                                           |
| <span data-ttu-id="20702-307">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-307">Get command:</span></span>     | [<span data-ttu-id="20702-308">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="20702-308">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="20702-309"></dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL \_ 行 \_ 寬度 \_ 細微性</dt> </span><span class="sxs-lookup"><span data-stu-id="20702-309"></dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL\_LINE\_WIDTH\_GRANULARITY</dt> </span></span><dd> 

| <span data-ttu-id="20702-310">屬性</span><span class="sxs-lookup"><span data-stu-id="20702-310">Property</span></span> | <span data-ttu-id="20702-311">值</span><span class="sxs-lookup"><span data-stu-id="20702-311">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="20702-312">描述：</span><span class="sxs-lookup"><span data-stu-id="20702-312">Description:</span></span>     | <span data-ttu-id="20702-313">反鋸齒線條寬度的資料細微性</span><span class="sxs-lookup"><span data-stu-id="20702-313">Antialiased line-width granularity</span></span>                                             |
| <span data-ttu-id="20702-314">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="20702-314">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="20702-315">初始值：</span><span class="sxs-lookup"><span data-stu-id="20702-315">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="20702-316">取得命令：</span><span class="sxs-lookup"><span data-stu-id="20702-316">Get command:</span></span>     | [<span data-ttu-id="20702-317">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="20702-317">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




