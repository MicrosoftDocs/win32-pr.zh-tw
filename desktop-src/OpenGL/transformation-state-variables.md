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
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312735"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="7852a-104">轉換狀態變數</span><span class="sxs-lookup"><span data-stu-id="7852a-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="7852a-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ 模型 \_ 矩陣</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="7852a-106">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-106">Description:</span></span>     | <span data-ttu-id="7852a-107">模型矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="7852a-107">Modelview matrix stack</span></span>             |
| <span data-ttu-id="7852a-108">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-108">Attribute group:</span></span> |                                    |
| <span data-ttu-id="7852a-109">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-109">Initial value:</span></span>   | <span data-ttu-id="7852a-110">身分識別</span><span class="sxs-lookup"><span data-stu-id="7852a-110">Identity</span></span>                           |
| <span data-ttu-id="7852a-111">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-111">Get command:</span></span>     | [<span data-ttu-id="7852a-112">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="7852a-112">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="7852a-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL \_ 投射 \_ 矩陣</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-114">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-114">Description:</span></span>     | <span data-ttu-id="7852a-115">投射矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="7852a-115">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="7852a-116">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-116">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="7852a-117">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-117">Initial value:</span></span>   | <span data-ttu-id="7852a-118">身分識別</span><span class="sxs-lookup"><span data-stu-id="7852a-118">Identity</span></span>                                                                       |
| <span data-ttu-id="7852a-119">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-119">Get command:</span></span>     | [<span data-ttu-id="7852a-120">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="7852a-120">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL \_ 材質 \_ 矩陣</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-122">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-122">Description:</span></span>     | <span data-ttu-id="7852a-123">材質矩陣堆疊</span><span class="sxs-lookup"><span data-stu-id="7852a-123">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="7852a-124">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-124">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="7852a-125">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-125">Initial value:</span></span>   | <span data-ttu-id="7852a-126">身分識別</span><span class="sxs-lookup"><span data-stu-id="7852a-126">Identity</span></span>                                                                       |
| <span data-ttu-id="7852a-127">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-127">Get command:</span></span>     | [<span data-ttu-id="7852a-128">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="7852a-128">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ 區</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-130">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-130">Description:</span></span>     | <span data-ttu-id="7852a-131">視口原點和範圍</span><span class="sxs-lookup"><span data-stu-id="7852a-131">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="7852a-132">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-132">Attribute group:</span></span> | <span data-ttu-id="7852a-133">Viewport - 檢視區</span><span class="sxs-lookup"><span data-stu-id="7852a-133">viewport</span></span>                                                                         |
| <span data-ttu-id="7852a-134">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-134">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="7852a-135">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-135">Get command:</span></span>     | [<span data-ttu-id="7852a-136">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7852a-136">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL \_ 深度 \_ 範圍</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-138">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-138">Description:</span></span>     | <span data-ttu-id="7852a-139">深度範圍接近或遠</span><span class="sxs-lookup"><span data-stu-id="7852a-139">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="7852a-140">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-140">Attribute group:</span></span> | <span data-ttu-id="7852a-141">Viewport - 檢視區</span><span class="sxs-lookup"><span data-stu-id="7852a-141">viewport</span></span>                                                                       |
| <span data-ttu-id="7852a-142">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-142">Initial value:</span></span>   | <span data-ttu-id="7852a-143">0、1</span><span class="sxs-lookup"><span data-stu-id="7852a-143">0, 1</span></span>                                                                           |
| <span data-ttu-id="7852a-144">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-144">Get command:</span></span>     | [<span data-ttu-id="7852a-145">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="7852a-145">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ 模型 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-147">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-147">Description:</span></span>     | <span data-ttu-id="7852a-148">模型矩陣堆疊指標</span><span class="sxs-lookup"><span data-stu-id="7852a-148">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="7852a-149">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="7852a-150">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-150">Initial value:</span></span>   | <span data-ttu-id="7852a-151">1</span><span class="sxs-lookup"><span data-stu-id="7852a-151">1</span></span>                                                                                |
| <span data-ttu-id="7852a-152">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-152">Get command:</span></span>     | [<span data-ttu-id="7852a-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7852a-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL \_ 投射 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-155">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-155">Description:</span></span>     | <span data-ttu-id="7852a-156">投射矩陣堆疊指標</span><span class="sxs-lookup"><span data-stu-id="7852a-156">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="7852a-157">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-157">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="7852a-158">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-158">Initial value:</span></span>   | <span data-ttu-id="7852a-159">1</span><span class="sxs-lookup"><span data-stu-id="7852a-159">1</span></span>                                                                                |
| <span data-ttu-id="7852a-160">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-160">Get command:</span></span>     | [<span data-ttu-id="7852a-161">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7852a-161">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL \_ 紋理 \_ 堆疊 \_ 深度</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-163">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-163">Description:</span></span>     | <span data-ttu-id="7852a-164">材質矩陣堆疊指標</span><span class="sxs-lookup"><span data-stu-id="7852a-164">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="7852a-165">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-165">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="7852a-166">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-166">Initial value:</span></span>   | <span data-ttu-id="7852a-167">1</span><span class="sxs-lookup"><span data-stu-id="7852a-167">1</span></span>                                                                                |
| <span data-ttu-id="7852a-168">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-168">Get command:</span></span>     | [<span data-ttu-id="7852a-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7852a-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL \_ 矩陣 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7852a-171">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-171">Description:</span></span>     | <span data-ttu-id="7852a-172">目前的矩陣模式</span><span class="sxs-lookup"><span data-stu-id="7852a-172">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="7852a-173">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-173">Attribute group:</span></span> | <span data-ttu-id="7852a-174">Transform - 轉換</span><span class="sxs-lookup"><span data-stu-id="7852a-174">transform</span></span>                                                                        |
| <span data-ttu-id="7852a-175">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-175">Initial value:</span></span>   | <span data-ttu-id="7852a-176">GL \_ 模型</span><span class="sxs-lookup"><span data-stu-id="7852a-176">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="7852a-177">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-177">Get command:</span></span>     | [<span data-ttu-id="7852a-178">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7852a-178">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7852a-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ 標準化</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

|                  |                                     |
|------------------|-------------------------------------|
| <span data-ttu-id="7852a-180">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-180">Description:</span></span>     | <span data-ttu-id="7852a-181">目前的一般正規化開啟/關閉</span><span class="sxs-lookup"><span data-stu-id="7852a-181">Current normal normalization on/off</span></span> |
| <span data-ttu-id="7852a-182">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-182">Attribute group:</span></span> | <span data-ttu-id="7852a-183">轉換/啟用</span><span class="sxs-lookup"><span data-stu-id="7852a-183">transform/enable</span></span>                    |
| <span data-ttu-id="7852a-184">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-184">Initial value:</span></span>   | <span data-ttu-id="7852a-185">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7852a-185">GL\_FALSE</span></span>                           |
| <span data-ttu-id="7852a-186">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-186">Get command:</span></span>     | [<span data-ttu-id="7852a-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7852a-187">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="7852a-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ 剪輯 \_ 平面 *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="7852a-189">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-189">Description:</span></span>     | <span data-ttu-id="7852a-190">使用者裁剪平面係數</span><span class="sxs-lookup"><span data-stu-id="7852a-190">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="7852a-191">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-191">Attribute group:</span></span> | <span data-ttu-id="7852a-192">Transform - 轉換</span><span class="sxs-lookup"><span data-stu-id="7852a-192">transform</span></span>                                |
| <span data-ttu-id="7852a-193">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-193">Initial value:</span></span>   | <span data-ttu-id="7852a-194">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="7852a-194">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="7852a-195">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-195">Get command:</span></span>     | [<span data-ttu-id="7852a-196">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="7852a-196">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="7852a-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ 剪輯 \_ 平面 *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="7852a-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="7852a-198">描述：</span><span class="sxs-lookup"><span data-stu-id="7852a-198">Description:</span></span>     | <span data-ttu-id="7852a-199">*我* 已啟用使用者裁剪平面</span><span class="sxs-lookup"><span data-stu-id="7852a-199">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="7852a-200">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="7852a-200">Attribute group:</span></span> | <span data-ttu-id="7852a-201">轉換/啟用</span><span class="sxs-lookup"><span data-stu-id="7852a-201">transform/enable</span></span>                   |
| <span data-ttu-id="7852a-202">初始值：</span><span class="sxs-lookup"><span data-stu-id="7852a-202">Initial value:</span></span>   | <span data-ttu-id="7852a-203">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7852a-203">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7852a-204">取得命令：</span><span class="sxs-lookup"><span data-stu-id="7852a-204">Get command:</span></span>     | [<span data-ttu-id="7852a-205">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7852a-205">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




