---
title: 畫面格緩衝區控制項狀態變數
description: 畫面格緩衝區控制項狀態變數
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- 畫面格緩衝區控制項狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103840956"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="ec8e9-104">畫面格緩衝區控制項狀態變數</span><span class="sxs-lookup"><span data-stu-id="ec8e9-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="ec8e9-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL \_ 繪圖 \_ 緩衝區</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="ec8e9-106">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-106">Description:</span></span>     | <span data-ttu-id="ec8e9-107">為繪圖選取的緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="ec8e9-108">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-108">Attribute group:</span></span> | <span data-ttu-id="ec8e9-109">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-109">color-buffer</span></span>                           |
| <span data-ttu-id="ec8e9-110">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="ec8e9-111">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-111">Get command:</span></span>     | [<span data-ttu-id="ec8e9-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL \_ 索引 \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-114">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-114">Description:</span></span>     | <span data-ttu-id="ec8e9-115">色彩索引 writemask</span><span class="sxs-lookup"><span data-stu-id="ec8e9-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="ec8e9-116">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-116">Attribute group:</span></span> | <span data-ttu-id="ec8e9-117">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ec8e9-118">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-118">Initial value:</span></span>   | <span data-ttu-id="ec8e9-119">1</span><span class="sxs-lookup"><span data-stu-id="ec8e9-119">1's</span></span>                                                                              |
| <span data-ttu-id="ec8e9-120">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-120">Get command:</span></span>     | [<span data-ttu-id="ec8e9-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL \_ 色彩 \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-123">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-123">Description:</span></span>     | <span data-ttu-id="ec8e9-124">色彩寫入可啟用;R、G、B 或</span><span class="sxs-lookup"><span data-stu-id="ec8e9-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="ec8e9-125">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-125">Attribute group:</span></span> | <span data-ttu-id="ec8e9-126">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="ec8e9-127">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-127">Initial value:</span></span>   | <span data-ttu-id="ec8e9-128">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="ec8e9-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="ec8e9-129">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-129">Get command:</span></span>     | [<span data-ttu-id="ec8e9-130">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL \_ 深度 \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-132">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-132">Description:</span></span>     | <span data-ttu-id="ec8e9-133">已啟用深度緩衝區以進行寫入</span><span class="sxs-lookup"><span data-stu-id="ec8e9-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="ec8e9-134">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-134">Attribute group:</span></span> | <span data-ttu-id="ec8e9-135">深度-緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="ec8e9-136">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-136">Initial value:</span></span>   | <span data-ttu-id="ec8e9-137">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="ec8e9-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="ec8e9-138">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-138">Get command:</span></span>     | [<span data-ttu-id="ec8e9-139">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL \_ 樣板 \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-141">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-141">Description:</span></span>     | <span data-ttu-id="ec8e9-142">樣板-緩衝區 writemask</span><span class="sxs-lookup"><span data-stu-id="ec8e9-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="ec8e9-143">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-143">Attribute group:</span></span> | <span data-ttu-id="ec8e9-144">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ec8e9-145">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-145">Initial value:</span></span>   | <span data-ttu-id="ec8e9-146">1</span><span class="sxs-lookup"><span data-stu-id="ec8e9-146">1's</span></span>                                                                              |
| <span data-ttu-id="ec8e9-147">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-147">Get command:</span></span>     | [<span data-ttu-id="ec8e9-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL \_ 色彩 \_ 清除 \_ 值</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-150">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-150">Description:</span></span>     | <span data-ttu-id="ec8e9-151">色彩緩衝區清除值 (RGBA 模式) </span><span class="sxs-lookup"><span data-stu-id="ec8e9-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="ec8e9-152">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-152">Attribute group:</span></span> | <span data-ttu-id="ec8e9-153">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="ec8e9-154">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-154">Initial value:</span></span>   | <span data-ttu-id="ec8e9-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="ec8e9-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="ec8e9-156">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-156">Get command:</span></span>     | [<span data-ttu-id="ec8e9-157">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL \_ 索引 \_ 清除 \_ 值</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-159">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-159">Description:</span></span>     | <span data-ttu-id="ec8e9-160">色彩緩衝區清除值 (色彩索引模式) </span><span class="sxs-lookup"><span data-stu-id="ec8e9-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="ec8e9-161">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-161">Attribute group:</span></span> | <span data-ttu-id="ec8e9-162">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="ec8e9-163">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-163">Initial value:</span></span>   | <span data-ttu-id="ec8e9-164">0</span><span class="sxs-lookup"><span data-stu-id="ec8e9-164">0</span></span>                                                                              |
| <span data-ttu-id="ec8e9-165">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-165">Get command:</span></span>     | [<span data-ttu-id="ec8e9-166">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL \_ 深度 \_ 清除 \_ 值</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-168">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-168">Description:</span></span>     | <span data-ttu-id="ec8e9-169">深度緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="ec8e9-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="ec8e9-170">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-170">Attribute group:</span></span> | <span data-ttu-id="ec8e9-171">深度-緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="ec8e9-172">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-172">Initial value:</span></span>   | <span data-ttu-id="ec8e9-173">1</span><span class="sxs-lookup"><span data-stu-id="ec8e9-173">1</span></span>                                                                                |
| <span data-ttu-id="ec8e9-174">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-174">Get command:</span></span>     | [<span data-ttu-id="ec8e9-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL \_ 樣板 \_ 清除 \_ 值</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-177">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-177">Description:</span></span>     | <span data-ttu-id="ec8e9-178">樣板-緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="ec8e9-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="ec8e9-179">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-179">Attribute group:</span></span> | <span data-ttu-id="ec8e9-180">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="ec8e9-181">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-181">Initial value:</span></span>   | <span data-ttu-id="ec8e9-182">0</span><span class="sxs-lookup"><span data-stu-id="ec8e9-182">0</span></span>                                                                                |
| <span data-ttu-id="ec8e9-183">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-183">Get command:</span></span>     | [<span data-ttu-id="ec8e9-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="ec8e9-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL \_ ACCUM \_ 清除 \_ 值</dt> </span><span class="sxs-lookup"><span data-stu-id="ec8e9-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e9-186">描述：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-186">Description:</span></span>     | <span data-ttu-id="ec8e9-187">累積緩衝區清除值</span><span class="sxs-lookup"><span data-stu-id="ec8e9-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="ec8e9-188">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-188">Attribute group:</span></span> | <span data-ttu-id="ec8e9-189">accum-緩衝區</span><span class="sxs-lookup"><span data-stu-id="ec8e9-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="ec8e9-190">初始值：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-190">Initial value:</span></span>   | <span data-ttu-id="ec8e9-191">0</span><span class="sxs-lookup"><span data-stu-id="ec8e9-191">0</span></span>                                                                              |
| <span data-ttu-id="ec8e9-192">取得命令：</span><span class="sxs-lookup"><span data-stu-id="ec8e9-192">Get command:</span></span>     | [<span data-ttu-id="ec8e9-193">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="ec8e9-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




