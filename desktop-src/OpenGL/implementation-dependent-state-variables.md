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
ms.openlocfilehash: afb42c13765678218efcaf58f2b02a01d2f0e160
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022490"
---
# <a name="implementation-dependent-state-variables"></a><span data-ttu-id="0cc04-104">Implementation-Dependent 狀態變數</span><span class="sxs-lookup"><span data-stu-id="0cc04-104">Implementation-Dependent State Variables</span></span>

<dl> <span data-ttu-id="0cc04-105"><dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ 最大 \_ 燈光</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-105"><dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL\_MAX\_LIGHTS</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="0cc04-106">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-106">Description:</span></span>     | <span data-ttu-id="0cc04-107">最大光線數目</span><span class="sxs-lookup"><span data-stu-id="0cc04-107">Maximum number of lights</span></span>               |
| <span data-ttu-id="0cc04-108">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-108">Attribute group:</span></span> |                                        |
| <span data-ttu-id="0cc04-109">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-109">Initial value:</span></span>   | <span data-ttu-id="0cc04-110">8</span><span class="sxs-lookup"><span data-stu-id="0cc04-110">8</span></span>                                      |
| <span data-ttu-id="0cc04-111">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-111">Get command:</span></span>     | [<span data-ttu-id="0cc04-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="0cc04-113"></dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL \_ 最大 \_ 剪輯 \_ 平面</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-113"></dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL\_MAX\_CLIP\_PLANES</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-114">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-114">Description:</span></span>     | <span data-ttu-id="0cc04-115">使用者裁剪平面的最大數目</span><span class="sxs-lookup"><span data-stu-id="0cc04-115">Maximum number of user clipping planes</span></span>                                           |
| <span data-ttu-id="0cc04-116">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-116">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-117">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-117">Initial value:</span></span>   | <span data-ttu-id="0cc04-118">6</span><span class="sxs-lookup"><span data-stu-id="0cc04-118">6</span></span>                                                                                |
| <span data-ttu-id="0cc04-119">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-119">Get command:</span></span>     | [<span data-ttu-id="0cc04-120">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-120">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-121"></dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-121"></dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL\_MAX\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-122">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-122">Description:</span></span>     | <span data-ttu-id="0cc04-123">最大模型-矩陣堆疊深度</span><span class="sxs-lookup"><span data-stu-id="0cc04-123">Maximum modelview-matrix stack depth</span></span>                                             |
| <span data-ttu-id="0cc04-124">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-124">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-125">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-125">Initial value:</span></span>   | <span data-ttu-id="0cc04-126">32</span><span class="sxs-lookup"><span data-stu-id="0cc04-126">32</span></span>                                                                               |
| <span data-ttu-id="0cc04-127">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-127">Get command:</span></span>     | [<span data-ttu-id="0cc04-128">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-128">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-129"></dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-129"></dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL\_MAX\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-130">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-130">Description:</span></span>     | <span data-ttu-id="0cc04-131">最大投射矩陣堆疊深度</span><span class="sxs-lookup"><span data-stu-id="0cc04-131">Maximum projection-matrix stack depth</span></span>                                            |
| <span data-ttu-id="0cc04-132">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-132">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-133">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-133">Initial value:</span></span>   | <span data-ttu-id="0cc04-134">2</span><span class="sxs-lookup"><span data-stu-id="0cc04-134">2</span></span>                                                                                |
| <span data-ttu-id="0cc04-135">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-135">Get command:</span></span>     | [<span data-ttu-id="0cc04-136">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-136">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-137"></dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL \_ 最大 \_ 紋理 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-137"></dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL\_MAX\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-138">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-138">Description:</span></span>     | <span data-ttu-id="0cc04-139">材質矩陣堆疊的深度上限</span><span class="sxs-lookup"><span data-stu-id="0cc04-139">Maximum depth of texture matrix stack</span></span>                                            |
| <span data-ttu-id="0cc04-140">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-140">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-141">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-141">Initial value:</span></span>   | <span data-ttu-id="0cc04-142">2</span><span class="sxs-lookup"><span data-stu-id="0cc04-142">2</span></span>                                                                                |
| <span data-ttu-id="0cc04-143">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-143">Get command:</span></span>     | [<span data-ttu-id="0cc04-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-145"></dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL \_ 子圖元 \_ 位</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-145"></dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL\_SUBPIXEL\_BITS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-146">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-146">Description:</span></span>     | <span data-ttu-id="0cc04-147">以 *x*   和 *y* 表示的子圖元精確度位數</span><span class="sxs-lookup"><span data-stu-id="0cc04-147">Number of bits of subpixel precision in *x* and *y*</span></span>                              |
| <span data-ttu-id="0cc04-148">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-148">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-149">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-149">Initial value:</span></span>   | <span data-ttu-id="0cc04-150">4</span><span class="sxs-lookup"><span data-stu-id="0cc04-150">4</span></span>                                                                                |
| <span data-ttu-id="0cc04-151">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-151">Get command:</span></span>     | [<span data-ttu-id="0cc04-152">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-152">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-153"></dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL \_ 最大 \_ 紋理 \_ 大小</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-153"></dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL\_MAX\_TEXTURE\_SIZE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-154">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-154">Description:</span></span>     | <span data-ttu-id="0cc04-155">材質影像的最大高度或寬度 (沒有框線) </span><span class="sxs-lookup"><span data-stu-id="0cc04-155">Maximum height or width of a texture image (without borders)</span></span>                     |
| <span data-ttu-id="0cc04-156">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-156">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-157">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-157">Initial value:</span></span>   | <span data-ttu-id="0cc04-158">64</span><span class="sxs-lookup"><span data-stu-id="0cc04-158">64</span></span>                                                                               |
| <span data-ttu-id="0cc04-159">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-159">Get command:</span></span>     | [<span data-ttu-id="0cc04-160">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-160">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-161"></dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL \_ 最大 \_ 圖元 \_ 映射 \_ 表</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-161"></dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL\_MAX\_PIXEL\_MAP\_TABLE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-162">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-162">Description:</span></span>     | <span data-ttu-id="0cc04-163">**GlPixelMap** 轉譯資料表的大小上限</span><span class="sxs-lookup"><span data-stu-id="0cc04-163">Maximum size of a **glPixelMap** translation table</span></span>                               |
| <span data-ttu-id="0cc04-164">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-164">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-165">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-165">Initial value:</span></span>   | <span data-ttu-id="0cc04-166">32</span><span class="sxs-lookup"><span data-stu-id="0cc04-166">32</span></span>                                                                               |
| <span data-ttu-id="0cc04-167">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-167">Get command:</span></span>     | [<span data-ttu-id="0cc04-168">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-168">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-169"></dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL \_ 最大 \_ 名稱 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-169"></dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL\_MAX\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-170">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-170">Description:</span></span>     | <span data-ttu-id="0cc04-171">最大選取範圍-名稱堆疊深度</span><span class="sxs-lookup"><span data-stu-id="0cc04-171">Maximum selection-name stack depth</span></span>                                               |
| <span data-ttu-id="0cc04-172">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-172">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-173">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-173">Initial value:</span></span>   | <span data-ttu-id="0cc04-174">64</span><span class="sxs-lookup"><span data-stu-id="0cc04-174">64</span></span>                                                                               |
| <span data-ttu-id="0cc04-175">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-175">Get command:</span></span>     | [<span data-ttu-id="0cc04-176">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-176">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-177"></dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL \_ 最大 \_ 清單的 \_ 嵌套</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-177"></dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL\_MAX\_LIST\_NESTING</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-178">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-178">Description:</span></span>     | <span data-ttu-id="0cc04-179">最大顯示清單呼叫嵌套</span><span class="sxs-lookup"><span data-stu-id="0cc04-179">Maximum display-list call nesting</span></span>                                                |
| <span data-ttu-id="0cc04-180">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-180">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-181">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-181">Initial value:</span></span>   | <span data-ttu-id="0cc04-182">64</span><span class="sxs-lookup"><span data-stu-id="0cc04-182">64</span></span>                                                                               |
| <span data-ttu-id="0cc04-183">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-183">Get command:</span></span>     | [<span data-ttu-id="0cc04-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-185"></dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ 最大 \_ EVAL \_ 順序</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-185"></dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL\_MAX\_EVAL\_ORDER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-186">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-186">Description:</span></span>     | <span data-ttu-id="0cc04-187">最大評估工具多項式順序</span><span class="sxs-lookup"><span data-stu-id="0cc04-187">Maximum evaluator polynomial order</span></span>                                               |
| <span data-ttu-id="0cc04-188">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-188">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-189">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-189">Initial value:</span></span>   | <span data-ttu-id="0cc04-190">8</span><span class="sxs-lookup"><span data-stu-id="0cc04-190">8</span></span>                                                                                |
| <span data-ttu-id="0cc04-191">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-191">Get command:</span></span>     | [<span data-ttu-id="0cc04-192">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-192">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-193"></dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ 最大 \_ 視窗區變 \_ 暗</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-193"></dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL\_MAX\_VIEWPORT\_DIMS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-194">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-194">Description:</span></span>     | <span data-ttu-id="0cc04-195">最大的視口維度</span><span class="sxs-lookup"><span data-stu-id="0cc04-195">Maximum viewport dimensions</span></span>                                                      |
| <span data-ttu-id="0cc04-196">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-196">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-197">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-197">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="0cc04-198">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-198">Get command:</span></span>     | [<span data-ttu-id="0cc04-199">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-199">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-200"></dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL \_ 最大的 \_ ATTRIB \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-200"></dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL\_MAX\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-201">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-201">Description:</span></span>     | <span data-ttu-id="0cc04-202">屬性堆疊的最大深度</span><span class="sxs-lookup"><span data-stu-id="0cc04-202">Maximum depth of the attribute stack</span></span>                                             |
| <span data-ttu-id="0cc04-203">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-203">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-204">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-204">Initial value:</span></span>   | <span data-ttu-id="0cc04-205">16</span><span class="sxs-lookup"><span data-stu-id="0cc04-205">16</span></span>                                                                               |
| <span data-ttu-id="0cc04-206">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-206">Get command:</span></span>     | [<span data-ttu-id="0cc04-207">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-207">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-208"></dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL \_ AUX \_ 緩衝區</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-208"></dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL\_AUX\_BUFFERS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-209">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-209">Description:</span></span>     | <span data-ttu-id="0cc04-210">輔助緩衝區數目</span><span class="sxs-lookup"><span data-stu-id="0cc04-210">Number of auxiliary buffers</span></span>                                                      |
| <span data-ttu-id="0cc04-211">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-211">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-212">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-212">Initial value:</span></span>   | <span data-ttu-id="0cc04-213">0</span><span class="sxs-lookup"><span data-stu-id="0cc04-213">0</span></span>                                                                                |
| <span data-ttu-id="0cc04-214">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-214">Get command:</span></span>     | [<span data-ttu-id="0cc04-215">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-215">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-216"></dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL \_ RGBA \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-216"></dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL\_RGBA\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-217">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-217">Description:</span></span>     | <span data-ttu-id="0cc04-218">如果色彩緩衝區儲存 RGBA，則為 True</span><span class="sxs-lookup"><span data-stu-id="0cc04-218">True if color buffers store RGBA</span></span>                                                 |
| <span data-ttu-id="0cc04-219">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-219">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-220">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-220">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="0cc04-221">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-221">Get command:</span></span>     | [<span data-ttu-id="0cc04-222">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-222">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-223"></dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL \_ 索引 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-223"></dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL\_INDEX\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-224">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-224">Description:</span></span>     | <span data-ttu-id="0cc04-225">如果色彩緩衝區儲存索引，則為 True</span><span class="sxs-lookup"><span data-stu-id="0cc04-225">True if color buffers store indexes</span></span>                                              |
| <span data-ttu-id="0cc04-226">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-226">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-227">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-227">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="0cc04-228">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-228">Get command:</span></span>     | [<span data-ttu-id="0cc04-229">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-229">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-230"></dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-230"></dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL\_DOUBLEBUFFER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-231">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-231">Description:</span></span>     | <span data-ttu-id="0cc04-232">如果有前端和背景緩衝區存在，則為 True</span><span class="sxs-lookup"><span data-stu-id="0cc04-232">True if front and back buffers exist</span></span>                                             |
| <span data-ttu-id="0cc04-233">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-233">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="0cc04-234">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-234">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="0cc04-235">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-235">Get command:</span></span>     | [<span data-ttu-id="0cc04-236">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-236">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-237"></dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ 身歷聲</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-237"></dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL\_STEREO</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-238">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-238">Description:</span></span>     | <span data-ttu-id="0cc04-239">如果有左方和右緩衝區存在，則為 True</span><span class="sxs-lookup"><span data-stu-id="0cc04-239">True if left and right buffers exist</span></span>                                           |
| <span data-ttu-id="0cc04-240">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-240">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="0cc04-241">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-241">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="0cc04-242">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-242">Get command:</span></span>     | [<span data-ttu-id="0cc04-243">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-243">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-244"></dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL \_ 點數 \_ 大小 \_ 範圍</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-244"></dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL\_POINT\_SIZE\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-245">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-245">Description:</span></span>     | <span data-ttu-id="0cc04-246">範圍 (低至高) 的反鋸齒點大小</span><span class="sxs-lookup"><span data-stu-id="0cc04-246">Range (low to high) of antialiased point sizes</span></span>                                 |
| <span data-ttu-id="0cc04-247">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-247">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="0cc04-248">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-248">Initial value:</span></span>   | <span data-ttu-id="0cc04-249">1，1</span><span class="sxs-lookup"><span data-stu-id="0cc04-249">1, 1</span></span>                                                                           |
| <span data-ttu-id="0cc04-250">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-250">Get command:</span></span>     | [<span data-ttu-id="0cc04-251">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-251">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-252"></dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GL \_ 點 \_ 大小 \_ 細微性</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-252"></dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GL\_POINT\_SIZE\_GRANULARITY</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-253">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-253">Description:</span></span>     | <span data-ttu-id="0cc04-254">反鋸齒點大小的資料細微性</span><span class="sxs-lookup"><span data-stu-id="0cc04-254">Antialiased point size granularity</span></span>                                             |
| <span data-ttu-id="0cc04-255">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-255">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="0cc04-256">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-256">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="0cc04-257">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-257">Get command:</span></span>     | [<span data-ttu-id="0cc04-258">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-258">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-259"></dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL \_ 線條 \_ 寬度 \_ 範圍</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-259"></dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL\_LINE\_WIDTH\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-260">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-260">Description:</span></span>     | <span data-ttu-id="0cc04-261">反鋸齒線條寬度的範圍 (低至高) </span><span class="sxs-lookup"><span data-stu-id="0cc04-261">Range (low to high) of antialiased line widths</span></span>                                 |
| <span data-ttu-id="0cc04-262">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-262">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="0cc04-263">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-263">Initial value:</span></span>   | <span data-ttu-id="0cc04-264">1，1</span><span class="sxs-lookup"><span data-stu-id="0cc04-264">1, 1</span></span>                                                                           |
| <span data-ttu-id="0cc04-265">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-265">Get command:</span></span>     | [<span data-ttu-id="0cc04-266">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-266">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0cc04-267"></dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL \_ 行 \_ 寬度 \_ 細微性</dt> </span><span class="sxs-lookup"><span data-stu-id="0cc04-267"></dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL\_LINE\_WIDTH\_GRANULARITY</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0cc04-268">描述：</span><span class="sxs-lookup"><span data-stu-id="0cc04-268">Description:</span></span>     | <span data-ttu-id="0cc04-269">反鋸齒線條寬度的資料細微性</span><span class="sxs-lookup"><span data-stu-id="0cc04-269">Antialiased line-width granularity</span></span>                                             |
| <span data-ttu-id="0cc04-270">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="0cc04-270">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="0cc04-271">初始值：</span><span class="sxs-lookup"><span data-stu-id="0cc04-271">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="0cc04-272">取得命令：</span><span class="sxs-lookup"><span data-stu-id="0cc04-272">Get command:</span></span>     | [<span data-ttu-id="0cc04-273">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0cc04-273">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




