---
title: 圖元作業
description: 圖元作業
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- 圖元運算 OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841159"
---
# <a name="pixel-operations"></a><span data-ttu-id="f90d9-104">圖元作業</span><span class="sxs-lookup"><span data-stu-id="f90d9-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="f90d9-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL \_ 剪式 \_ 測試</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-106">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-106">Description:</span></span>     | <span data-ttu-id="f90d9-107">Scissoring 已啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="f90d9-108">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-108">Attribute group:</span></span> | <span data-ttu-id="f90d9-109">剪式/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-109">scissor/enable</span></span>                     |
| <span data-ttu-id="f90d9-110">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-110">Initial value:</span></span>   | <span data-ttu-id="f90d9-111">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f90d9-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f90d9-112">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-112">Get command:</span></span>     | [<span data-ttu-id="f90d9-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL \_ 剪狀方塊 \_</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-115">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-115">Description:</span></span>     | <span data-ttu-id="f90d9-116">剪式方塊</span><span class="sxs-lookup"><span data-stu-id="f90d9-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="f90d9-117">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-117">Attribute group:</span></span> | <span data-ttu-id="f90d9-118">剪刀</span><span class="sxs-lookup"><span data-stu-id="f90d9-118">scissor</span></span>                                                                          |
| <span data-ttu-id="f90d9-119">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="f90d9-120">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-120">Get command:</span></span>     | [<span data-ttu-id="f90d9-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL \_ 樣板 \_ 測試</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-123">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-123">Description:</span></span>     | <span data-ttu-id="f90d9-124">Stenciling 已啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="f90d9-125">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-125">Attribute group:</span></span> | <span data-ttu-id="f90d9-126">樣板-緩衝區/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="f90d9-127">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-127">Initial value:</span></span>   | <span data-ttu-id="f90d9-128">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f90d9-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f90d9-129">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-129">Get command:</span></span>     | [<span data-ttu-id="f90d9-130">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL \_ 樣板 \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-132">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-132">Description:</span></span>     | <span data-ttu-id="f90d9-133">樣板函式</span><span class="sxs-lookup"><span data-stu-id="f90d9-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="f90d9-134">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-134">Attribute group:</span></span> | <span data-ttu-id="f90d9-135">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f90d9-136">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-136">Initial value:</span></span>   | <span data-ttu-id="f90d9-137">GL \_ 一律</span><span class="sxs-lookup"><span data-stu-id="f90d9-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="f90d9-138">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-138">Get command:</span></span>     | [<span data-ttu-id="f90d9-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL \_ 樣板 \_ 值 \_ 遮罩</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-141">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-141">Description:</span></span>     | <span data-ttu-id="f90d9-142">樣板遮罩</span><span class="sxs-lookup"><span data-stu-id="f90d9-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="f90d9-143">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-143">Attribute group:</span></span> | <span data-ttu-id="f90d9-144">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f90d9-145">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-145">Initial value:</span></span>   | <span data-ttu-id="f90d9-146">1</span><span class="sxs-lookup"><span data-stu-id="f90d9-146">1's</span></span>                                                                              |
| <span data-ttu-id="f90d9-147">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-147">Get command:</span></span>     | [<span data-ttu-id="f90d9-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ 樣板 \_ 參考</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-150">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-150">Description:</span></span>     | <span data-ttu-id="f90d9-151">樣板參考值</span><span class="sxs-lookup"><span data-stu-id="f90d9-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="f90d9-152">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-152">Attribute group:</span></span> | <span data-ttu-id="f90d9-153">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f90d9-154">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-154">Initial value:</span></span>   | <span data-ttu-id="f90d9-155">0</span><span class="sxs-lookup"><span data-stu-id="f90d9-155">0</span></span>                                                                                |
| <span data-ttu-id="f90d9-156">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-156">Get command:</span></span>     | [<span data-ttu-id="f90d9-157">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL \_ 樣板 \_ 失敗</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-159">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-159">Description:</span></span>     | <span data-ttu-id="f90d9-160">樣板失敗動作</span><span class="sxs-lookup"><span data-stu-id="f90d9-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="f90d9-161">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-161">Attribute group:</span></span> | <span data-ttu-id="f90d9-162">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f90d9-163">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-163">Initial value:</span></span>   | <span data-ttu-id="f90d9-164">GL \_ 保留</span><span class="sxs-lookup"><span data-stu-id="f90d9-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="f90d9-165">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-165">Get command:</span></span>     | [<span data-ttu-id="f90d9-166">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL \_ 樣板 \_ 通過 \_ 深度 \_ 失敗</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-168">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-168">Description:</span></span>     | <span data-ttu-id="f90d9-169">樣板深度緩衝區失敗動作</span><span class="sxs-lookup"><span data-stu-id="f90d9-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="f90d9-170">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-170">Attribute group:</span></span> | <span data-ttu-id="f90d9-171">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f90d9-172">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-172">Initial value:</span></span>   | <span data-ttu-id="f90d9-173">GL \_ 保留</span><span class="sxs-lookup"><span data-stu-id="f90d9-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="f90d9-174">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-174">Get command:</span></span>     | [<span data-ttu-id="f90d9-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL \_ 樣板 \_ 通過 \_ 深度 \_ 傳遞</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-177">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-177">Description:</span></span>     | <span data-ttu-id="f90d9-178">樣板深度緩衝區傳遞動作</span><span class="sxs-lookup"><span data-stu-id="f90d9-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="f90d9-179">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-179">Attribute group:</span></span> | <span data-ttu-id="f90d9-180">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="f90d9-181">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-181">Initial value:</span></span>   | <span data-ttu-id="f90d9-182">GL \_ 保留</span><span class="sxs-lookup"><span data-stu-id="f90d9-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="f90d9-183">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-183">Get command:</span></span>     | [<span data-ttu-id="f90d9-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL \_ ALPHA \_ 測試</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-186">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-186">Description:</span></span>     | <span data-ttu-id="f90d9-187">已啟用 Alpha 測試</span><span class="sxs-lookup"><span data-stu-id="f90d9-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="f90d9-188">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-188">Attribute group:</span></span> | <span data-ttu-id="f90d9-189">色彩緩衝區/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="f90d9-190">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-190">Initial value:</span></span>   | <span data-ttu-id="f90d9-191">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f90d9-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f90d9-192">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-192">Get command:</span></span>     | [<span data-ttu-id="f90d9-193">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL \_ ALPHA \_ 測試 \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-195">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-195">Description:</span></span>     | <span data-ttu-id="f90d9-196">Alpha 測試函式</span><span class="sxs-lookup"><span data-stu-id="f90d9-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="f90d9-197">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-197">Attribute group:</span></span> | <span data-ttu-id="f90d9-198">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f90d9-199">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-199">Initial value:</span></span>   | <span data-ttu-id="f90d9-200">GL \_ 一律</span><span class="sxs-lookup"><span data-stu-id="f90d9-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="f90d9-201">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-201">Get command:</span></span>     | [<span data-ttu-id="f90d9-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ 測試 \_ 參考</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-204">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-204">Description:</span></span>     | <span data-ttu-id="f90d9-205">Alpha 測試參考值</span><span class="sxs-lookup"><span data-stu-id="f90d9-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="f90d9-206">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-206">Attribute group:</span></span> | <span data-ttu-id="f90d9-207">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f90d9-208">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-208">Initial value:</span></span>   | <span data-ttu-id="f90d9-209">0</span><span class="sxs-lookup"><span data-stu-id="f90d9-209">0</span></span>                                                                                |
| <span data-ttu-id="f90d9-210">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-210">Get command:</span></span>     | [<span data-ttu-id="f90d9-211">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL \_ 深度 \_ 測試</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-213">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-213">Description:</span></span>     | <span data-ttu-id="f90d9-214">深度緩衝區已啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="f90d9-215">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-215">Attribute group:</span></span> | <span data-ttu-id="f90d9-216">深度-緩衝區/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="f90d9-217">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-217">Initial value:</span></span>   | <span data-ttu-id="f90d9-218">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f90d9-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f90d9-219">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-219">Get command:</span></span>     | [<span data-ttu-id="f90d9-220">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ 深度 \_ FUNC</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-222">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-222">Description:</span></span>     | <span data-ttu-id="f90d9-223">深度緩衝區測試函式</span><span class="sxs-lookup"><span data-stu-id="f90d9-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="f90d9-224">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-224">Attribute group:</span></span> | <span data-ttu-id="f90d9-225">深度-緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="f90d9-226">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-226">Initial value:</span></span>   | <span data-ttu-id="f90d9-227">GL \_ LESS</span><span class="sxs-lookup"><span data-stu-id="f90d9-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="f90d9-228">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-228">Get command:</span></span>     | [<span data-ttu-id="f90d9-229">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-231">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-231">Description:</span></span>     | <span data-ttu-id="f90d9-232">已啟用混合</span><span class="sxs-lookup"><span data-stu-id="f90d9-232">Blending enabled</span></span>                   |
| <span data-ttu-id="f90d9-233">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-233">Attribute group:</span></span> | <span data-ttu-id="f90d9-234">色彩緩衝區/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="f90d9-235">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-235">Initial value:</span></span>   | <span data-ttu-id="f90d9-236">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f90d9-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f90d9-237">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-237">Get command:</span></span>     | [<span data-ttu-id="f90d9-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-240">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-240">Description:</span></span>     | <span data-ttu-id="f90d9-241">混合來源函數</span><span class="sxs-lookup"><span data-stu-id="f90d9-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="f90d9-242">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-242">Attribute group:</span></span> | <span data-ttu-id="f90d9-243">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f90d9-244">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-244">Initial value:</span></span>   | <span data-ttu-id="f90d9-245">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="f90d9-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="f90d9-246">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-246">Get command:</span></span>     | [<span data-ttu-id="f90d9-247">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ BLEND \_ DST</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-249">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-249">Description:</span></span>     | <span data-ttu-id="f90d9-250">混色 destination 函數</span><span class="sxs-lookup"><span data-stu-id="f90d9-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="f90d9-251">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-251">Attribute group:</span></span> | <span data-ttu-id="f90d9-252">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f90d9-253">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-253">Initial value:</span></span>   | <span data-ttu-id="f90d9-254">GL \_ 零</span><span class="sxs-lookup"><span data-stu-id="f90d9-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="f90d9-255">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-255">Get command:</span></span>     | [<span data-ttu-id="f90d9-256">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="f90d9-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ 遞色</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-258">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-258">Description:</span></span>     | <span data-ttu-id="f90d9-259">已啟用遞色</span><span class="sxs-lookup"><span data-stu-id="f90d9-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="f90d9-260">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-260">Attribute group:</span></span> | <span data-ttu-id="f90d9-261">色彩緩衝區/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="f90d9-262">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-262">Initial value:</span></span>   | <span data-ttu-id="f90d9-263">GL \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="f90d9-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="f90d9-264">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-264">Get command:</span></span>     | [<span data-ttu-id="f90d9-265">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ 邏輯 \_ OP</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="f90d9-267">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-267">Description:</span></span>     | <span data-ttu-id="f90d9-268">邏輯運算已啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="f90d9-269">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-269">Attribute group:</span></span> | <span data-ttu-id="f90d9-270">色彩緩衝區/啟用</span><span class="sxs-lookup"><span data-stu-id="f90d9-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="f90d9-271">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-271">Initial value:</span></span>   | <span data-ttu-id="f90d9-272">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="f90d9-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="f90d9-273">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-273">Get command:</span></span>     | [<span data-ttu-id="f90d9-274">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f90d9-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="f90d9-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL \_ 邏輯 \_ OP \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="f90d9-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f90d9-276">描述：</span><span class="sxs-lookup"><span data-stu-id="f90d9-276">Description:</span></span>     | <span data-ttu-id="f90d9-277">邏輯運算函數</span><span class="sxs-lookup"><span data-stu-id="f90d9-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="f90d9-278">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="f90d9-278">Attribute group:</span></span> | <span data-ttu-id="f90d9-279">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="f90d9-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="f90d9-280">初始值：</span><span class="sxs-lookup"><span data-stu-id="f90d9-280">Initial value:</span></span>   | <span data-ttu-id="f90d9-281">GL \_ 複製</span><span class="sxs-lookup"><span data-stu-id="f90d9-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="f90d9-282">取得命令：</span><span class="sxs-lookup"><span data-stu-id="f90d9-282">Get command:</span></span>     | [<span data-ttu-id="f90d9-283">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="f90d9-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




