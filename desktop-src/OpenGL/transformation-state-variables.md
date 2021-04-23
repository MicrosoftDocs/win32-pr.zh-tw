---
title: 轉換狀態變數
description: 轉換狀態變數
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- 轉換狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908826"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="8e237-104">轉換狀態變數</span><span class="sxs-lookup"><span data-stu-id="8e237-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="8e237-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ 模型 \_ 矩陣</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="8e237-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-106">Property</span></span> | <span data-ttu-id="8e237-107">值</span><span class="sxs-lookup"><span data-stu-id="8e237-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="8e237-108">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-108">Description:</span></span>     | <span data-ttu-id="8e237-109">模型矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="8e237-109">Modelview matrix stack</span></span>             |
| <span data-ttu-id="8e237-110">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-110">Attribute group:</span></span> |                                    |
| <span data-ttu-id="8e237-111">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-111">Initial value:</span></span>   | <span data-ttu-id="8e237-112">身分識別</span><span class="sxs-lookup"><span data-stu-id="8e237-112">Identity</span></span>                           |
| <span data-ttu-id="8e237-113">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-113">Get command:</span></span>     | [<span data-ttu-id="8e237-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="8e237-114">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="8e237-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL \_ 投射 \_ 矩陣</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="8e237-116">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-116">Property</span></span> | <span data-ttu-id="8e237-117">值</span><span class="sxs-lookup"><span data-stu-id="8e237-117">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-118">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-118">Description:</span></span>     | <span data-ttu-id="8e237-119">投射矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="8e237-119">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="8e237-120">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-120">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="8e237-121">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-121">Initial value:</span></span>   | <span data-ttu-id="8e237-122">身分識別</span><span class="sxs-lookup"><span data-stu-id="8e237-122">Identity</span></span>                                                                       |
| <span data-ttu-id="8e237-123">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-123">Get command:</span></span>     | [<span data-ttu-id="8e237-124">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="8e237-124">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL \_ 材質 \_ 矩陣</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="8e237-126">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-126">Property</span></span> | <span data-ttu-id="8e237-127">值</span><span class="sxs-lookup"><span data-stu-id="8e237-127">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-128">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-128">Description:</span></span>     | <span data-ttu-id="8e237-129">材質矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="8e237-129">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="8e237-130">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-130">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="8e237-131">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-131">Initial value:</span></span>   | <span data-ttu-id="8e237-132">身分識別</span><span class="sxs-lookup"><span data-stu-id="8e237-132">Identity</span></span>                                                                       |
| <span data-ttu-id="8e237-133">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-133">Get command:</span></span>     | [<span data-ttu-id="8e237-134">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="8e237-134">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ 區</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

| <span data-ttu-id="8e237-136">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-136">Property</span></span> | <span data-ttu-id="8e237-137">值</span><span class="sxs-lookup"><span data-stu-id="8e237-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-138">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-138">Description:</span></span>     | <span data-ttu-id="8e237-139">視口原點和範圍</span><span class="sxs-lookup"><span data-stu-id="8e237-139">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="8e237-140">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-140">Attribute group:</span></span> | <span data-ttu-id="8e237-141">Viewport - 檢視區</span><span class="sxs-lookup"><span data-stu-id="8e237-141">viewport</span></span>                                                                         |
| <span data-ttu-id="8e237-142">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-142">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="8e237-143">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-143">Get command:</span></span>     | [<span data-ttu-id="8e237-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8e237-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL \_ 深度 \_ 範圍</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="8e237-146">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-146">Property</span></span> | <span data-ttu-id="8e237-147">值</span><span class="sxs-lookup"><span data-stu-id="8e237-147">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-148">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-148">Description:</span></span>     | <span data-ttu-id="8e237-149">深度範圍接近或遠</span><span class="sxs-lookup"><span data-stu-id="8e237-149">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="8e237-150">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-150">Attribute group:</span></span> | <span data-ttu-id="8e237-151">Viewport - 檢視區</span><span class="sxs-lookup"><span data-stu-id="8e237-151">viewport</span></span>                                                                       |
| <span data-ttu-id="8e237-152">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-152">Initial value:</span></span>   | <span data-ttu-id="8e237-153">0、1</span><span class="sxs-lookup"><span data-stu-id="8e237-153">0, 1</span></span>                                                                           |
| <span data-ttu-id="8e237-154">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-154">Get command:</span></span>     | [<span data-ttu-id="8e237-155">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="8e237-155">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ 模型 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="8e237-157">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-157">Property</span></span> | <span data-ttu-id="8e237-158">值</span><span class="sxs-lookup"><span data-stu-id="8e237-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-159">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-159">Description:</span></span>     | <span data-ttu-id="8e237-160">模型矩陣堆疊指標</span><span class="sxs-lookup"><span data-stu-id="8e237-160">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="8e237-161">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8e237-162">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-162">Initial value:</span></span>   | <span data-ttu-id="8e237-163">1</span><span class="sxs-lookup"><span data-stu-id="8e237-163">1</span></span>                                                                                |
| <span data-ttu-id="8e237-164">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-164">Get command:</span></span>     | [<span data-ttu-id="8e237-165">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8e237-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL \_ 投射 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="8e237-167">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-167">Property</span></span> | <span data-ttu-id="8e237-168">值</span><span class="sxs-lookup"><span data-stu-id="8e237-168">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-169">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-169">Description:</span></span>     | <span data-ttu-id="8e237-170">投射矩陣堆疊指標</span><span class="sxs-lookup"><span data-stu-id="8e237-170">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="8e237-171">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-171">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8e237-172">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-172">Initial value:</span></span>   | <span data-ttu-id="8e237-173">1</span><span class="sxs-lookup"><span data-stu-id="8e237-173">1</span></span>                                                                                |
| <span data-ttu-id="8e237-174">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-174">Get command:</span></span>     | [<span data-ttu-id="8e237-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8e237-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL \_ 紋理 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="8e237-177">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-177">Property</span></span> | <span data-ttu-id="8e237-178">值</span><span class="sxs-lookup"><span data-stu-id="8e237-178">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-179">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-179">Description:</span></span>     | <span data-ttu-id="8e237-180">材質矩陣堆疊指標</span><span class="sxs-lookup"><span data-stu-id="8e237-180">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="8e237-181">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-181">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="8e237-182">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-182">Initial value:</span></span>   | <span data-ttu-id="8e237-183">1</span><span class="sxs-lookup"><span data-stu-id="8e237-183">1</span></span>                                                                                |
| <span data-ttu-id="8e237-184">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-184">Get command:</span></span>     | [<span data-ttu-id="8e237-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8e237-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL \_ 矩陣 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="8e237-187">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-187">Property</span></span> | <span data-ttu-id="8e237-188">值</span><span class="sxs-lookup"><span data-stu-id="8e237-188">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e237-189">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-189">Description:</span></span>     | <span data-ttu-id="8e237-190">目前的矩陣模式</span><span class="sxs-lookup"><span data-stu-id="8e237-190">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="8e237-191">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-191">Attribute group:</span></span> | <span data-ttu-id="8e237-192">Transform - 轉換</span><span class="sxs-lookup"><span data-stu-id="8e237-192">transform</span></span>                                                                        |
| <span data-ttu-id="8e237-193">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-193">Initial value:</span></span>   | <span data-ttu-id="8e237-194">GL \_ 模型</span><span class="sxs-lookup"><span data-stu-id="8e237-194">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="8e237-195">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-195">Get command:</span></span>     | [<span data-ttu-id="8e237-196">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8e237-196">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="8e237-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ 標準化</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

| <span data-ttu-id="8e237-198">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-198">Property</span></span> | <span data-ttu-id="8e237-199">值</span><span class="sxs-lookup"><span data-stu-id="8e237-199">Value</span></span> |
|------------------|-------------------------------------|
| <span data-ttu-id="8e237-200">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-200">Description:</span></span>     | <span data-ttu-id="8e237-201">目前的一般正規化開啟/關閉</span><span class="sxs-lookup"><span data-stu-id="8e237-201">Current normal normalization on/off</span></span> |
| <span data-ttu-id="8e237-202">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-202">Attribute group:</span></span> | <span data-ttu-id="8e237-203">轉換/啟用</span><span class="sxs-lookup"><span data-stu-id="8e237-203">transform/enable</span></span>                    |
| <span data-ttu-id="8e237-204">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-204">Initial value:</span></span>   | <span data-ttu-id="8e237-205">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="8e237-205">GL\_FALSE</span></span>                           |
| <span data-ttu-id="8e237-206">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-206">Get command:</span></span>     | [<span data-ttu-id="8e237-207">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8e237-207">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="8e237-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ 剪輯 \_ 平面 *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="8e237-209">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-209">Property</span></span> | <span data-ttu-id="8e237-210">值</span><span class="sxs-lookup"><span data-stu-id="8e237-210">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="8e237-211">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-211">Description:</span></span>     | <span data-ttu-id="8e237-212">使用者裁剪平面係數</span><span class="sxs-lookup"><span data-stu-id="8e237-212">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="8e237-213">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-213">Attribute group:</span></span> | <span data-ttu-id="8e237-214">Transform - 轉換</span><span class="sxs-lookup"><span data-stu-id="8e237-214">transform</span></span>                                |
| <span data-ttu-id="8e237-215">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-215">Initial value:</span></span>   | <span data-ttu-id="8e237-216">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="8e237-216">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="8e237-217">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-217">Get command:</span></span>     | [<span data-ttu-id="8e237-218">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="8e237-218">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="8e237-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ 剪輯 \_ 平面 *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="8e237-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="8e237-220">屬性</span><span class="sxs-lookup"><span data-stu-id="8e237-220">Property</span></span> | <span data-ttu-id="8e237-221">值</span><span class="sxs-lookup"><span data-stu-id="8e237-221">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="8e237-222">描述：</span><span class="sxs-lookup"><span data-stu-id="8e237-222">Description:</span></span>     | <span data-ttu-id="8e237-223">*我* 已啟用使用者裁剪平面</span><span class="sxs-lookup"><span data-stu-id="8e237-223">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="8e237-224">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="8e237-224">Attribute group:</span></span> | <span data-ttu-id="8e237-225">轉換/啟用</span><span class="sxs-lookup"><span data-stu-id="8e237-225">transform/enable</span></span>                   |
| <span data-ttu-id="8e237-226">初始值：</span><span class="sxs-lookup"><span data-stu-id="8e237-226">Initial value:</span></span>   | <span data-ttu-id="8e237-227">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="8e237-227">GL\_FALSE</span></span>                          |
| <span data-ttu-id="8e237-228">取得命令：</span><span class="sxs-lookup"><span data-stu-id="8e237-228">Get command:</span></span>     | [<span data-ttu-id="8e237-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8e237-229">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




