---
title: 紋理狀態變數
description: 紋理狀態變數
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- 紋理狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff468c701100cc598a519ed3aa290913016a559e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908646"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="608c1-104">紋理狀態變數</span><span class="sxs-lookup"><span data-stu-id="608c1-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="608c1-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ 材質 \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

| <span data-ttu-id="608c1-106">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-106">Property</span></span> | <span data-ttu-id="608c1-107">值</span><span class="sxs-lookup"><span data-stu-id="608c1-107">Value</span></span> |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="608c1-108">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-108">Description:</span></span>     | <span data-ttu-id="608c1-109">如果已啟用 *x* -d 紋理 (*x* 為 1-d 或 2-d) ，則為 True</span><span class="sxs-lookup"><span data-stu-id="608c1-109">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="608c1-110">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-110">Attribute group:</span></span> | <span data-ttu-id="608c1-111">材質/啟用</span><span class="sxs-lookup"><span data-stu-id="608c1-111">texture/enable</span></span>                                        |
| <span data-ttu-id="608c1-112">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-112">Initial value:</span></span>   | <span data-ttu-id="608c1-113">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="608c1-113">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="608c1-114">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-114">Get command:</span></span>     | [<span data-ttu-id="608c1-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="608c1-115">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="608c1-116"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL \_ 材質</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-116"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

| <span data-ttu-id="608c1-117">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-117">Property</span></span> | <span data-ttu-id="608c1-118">值</span><span class="sxs-lookup"><span data-stu-id="608c1-118">Value</span></span> |
|------------------|----------------------------------------------|
| <span data-ttu-id="608c1-119">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-119">Description:</span></span>     | <span data-ttu-id="608c1-120"> *詳細資料* 層級的立體材質影像</span><span class="sxs-lookup"><span data-stu-id="608c1-120">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="608c1-121">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-121">Attribute group:</span></span> |                                              |
| <span data-ttu-id="608c1-122">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-122">Initial value:</span></span>   |                                              |
| <span data-ttu-id="608c1-123">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-123">Get command:</span></span>     | [<span data-ttu-id="608c1-124">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="608c1-124">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="608c1-125"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL \_ 材質 \_ 寬度</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-125"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

| <span data-ttu-id="608c1-126">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-126">Property</span></span> | <span data-ttu-id="608c1-127">值</span><span class="sxs-lookup"><span data-stu-id="608c1-127">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="608c1-128">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-128">Description:</span></span>     | <span data-ttu-id="608c1-129">立體材質影像 *我* 的寬度</span><span class="sxs-lookup"><span data-stu-id="608c1-129">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="608c1-130">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-130">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="608c1-131">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-131">Initial value:</span></span>   | <span data-ttu-id="608c1-132">0</span><span class="sxs-lookup"><span data-stu-id="608c1-132">0</span></span>                                                        |
| <span data-ttu-id="608c1-133">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-133">Get command:</span></span>     | [<span data-ttu-id="608c1-134">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-134">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="608c1-135"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL \_ 材質 \_ 高度</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-135"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

| <span data-ttu-id="608c1-136">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-136">Property</span></span> | <span data-ttu-id="608c1-137">值</span><span class="sxs-lookup"><span data-stu-id="608c1-137">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="608c1-138">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-138">Description:</span></span>     | <span data-ttu-id="608c1-139">*x* -D 紋理影像 *我* 的高度</span><span class="sxs-lookup"><span data-stu-id="608c1-139">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="608c1-140">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="608c1-141">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-141">Initial value:</span></span>   | <span data-ttu-id="608c1-142">0</span><span class="sxs-lookup"><span data-stu-id="608c1-142">0</span></span>                                                        |
| <span data-ttu-id="608c1-143">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-143">Get command:</span></span>     | [<span data-ttu-id="608c1-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="608c1-145"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL \_ 材質 \_ 框線</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-145"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

| <span data-ttu-id="608c1-146">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-146">Property</span></span> | <span data-ttu-id="608c1-147">值</span><span class="sxs-lookup"><span data-stu-id="608c1-147">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="608c1-148">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-148">Description:</span></span>     | <span data-ttu-id="608c1-149">立體材質影像 *i* 框線</span><span class="sxs-lookup"><span data-stu-id="608c1-149">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="608c1-150">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-150">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="608c1-151">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-151">Initial value:</span></span>   | <span data-ttu-id="608c1-152">0</span><span class="sxs-lookup"><span data-stu-id="608c1-152">0</span></span>                                                        |
| <span data-ttu-id="608c1-153">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-153">Get command:</span></span>     | [<span data-ttu-id="608c1-154">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-154">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="608c1-155"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL \_ 材質 \_ 元件</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-155"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

| <span data-ttu-id="608c1-156">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-156">Property</span></span> | <span data-ttu-id="608c1-157">值</span><span class="sxs-lookup"><span data-stu-id="608c1-157">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="608c1-158">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-158">Description:</span></span>     | <span data-ttu-id="608c1-159">材質影像元件</span><span class="sxs-lookup"><span data-stu-id="608c1-159">Texture image components</span></span>                                 |
| <span data-ttu-id="608c1-160">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-160">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="608c1-161">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-161">Initial value:</span></span>   | <span data-ttu-id="608c1-162">1</span><span class="sxs-lookup"><span data-stu-id="608c1-162">1</span></span>                                                        |
| <span data-ttu-id="608c1-163">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-163">Get command:</span></span>     | [<span data-ttu-id="608c1-164">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-164">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="608c1-165"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL \_ 紋理 \_ 框線 \_ 色彩</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-165"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

| <span data-ttu-id="608c1-166">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-166">Property</span></span> | <span data-ttu-id="608c1-167">值</span><span class="sxs-lookup"><span data-stu-id="608c1-167">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="608c1-168">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-168">Description:</span></span>     | <span data-ttu-id="608c1-169">材質框線色彩</span><span class="sxs-lookup"><span data-stu-id="608c1-169">Texture border color</span></span>                           |
| <span data-ttu-id="608c1-170">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-170">Attribute group:</span></span> | <span data-ttu-id="608c1-171">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-171">texture</span></span>                                        |
| <span data-ttu-id="608c1-172">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-172">Initial value:</span></span>   | <span data-ttu-id="608c1-173">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="608c1-173">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="608c1-174">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-174">Get command:</span></span>     | [<span data-ttu-id="608c1-175">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-175">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="608c1-176"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL \_ 材質 \_ 最小 \_ 篩選</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-176"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

| <span data-ttu-id="608c1-177">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-177">Property</span></span> | <span data-ttu-id="608c1-178">值</span><span class="sxs-lookup"><span data-stu-id="608c1-178">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="608c1-179">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-179">Description:</span></span>     | <span data-ttu-id="608c1-180">紋理縮制函式</span><span class="sxs-lookup"><span data-stu-id="608c1-180">Texture minification function</span></span>                  |
| <span data-ttu-id="608c1-181">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-181">Attribute group:</span></span> | <span data-ttu-id="608c1-182">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-182">texture</span></span>                                        |
| <span data-ttu-id="608c1-183">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-183">Initial value:</span></span>   | <span data-ttu-id="608c1-184">GL \_ 最接近 \_ MIPMAP \_ 線性</span><span class="sxs-lookup"><span data-stu-id="608c1-184">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="608c1-185">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-185">Get command:</span></span>     | [<span data-ttu-id="608c1-186">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-186">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="608c1-187"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL \_ 紋理 \_ MAG \_ 篩選</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-187"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

| <span data-ttu-id="608c1-188">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-188">Property</span></span> | <span data-ttu-id="608c1-189">值</span><span class="sxs-lookup"><span data-stu-id="608c1-189">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="608c1-190">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-190">Description:</span></span>     | <span data-ttu-id="608c1-191">材質放大功能</span><span class="sxs-lookup"><span data-stu-id="608c1-191">Texture magnification function</span></span>                 |
| <span data-ttu-id="608c1-192">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-192">Attribute group:</span></span> | <span data-ttu-id="608c1-193">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-193">texture</span></span>                                        |
| <span data-ttu-id="608c1-194">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-194">Initial value:</span></span>   | <span data-ttu-id="608c1-195">GL \_ 線性</span><span class="sxs-lookup"><span data-stu-id="608c1-195">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="608c1-196">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-196">Get command:</span></span>     | [<span data-ttu-id="608c1-197">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-197">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="608c1-198"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ 材質 \_ 換行 \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-198"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

| <span data-ttu-id="608c1-199">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-199">Property</span></span> | <span data-ttu-id="608c1-200">值</span><span class="sxs-lookup"><span data-stu-id="608c1-200">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="608c1-201">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-201">Description:</span></span>     | <span data-ttu-id="608c1-202">材質 wrap 模式 (*x* 是 S 或 T) </span><span class="sxs-lookup"><span data-stu-id="608c1-202">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="608c1-203">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-203">Attribute group:</span></span> | <span data-ttu-id="608c1-204">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-204">texture</span></span>                                        |
| <span data-ttu-id="608c1-205">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-205">Initial value:</span></span>   | <span data-ttu-id="608c1-206">GL \_ 重複</span><span class="sxs-lookup"><span data-stu-id="608c1-206">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="608c1-207">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-207">Get command:</span></span>     | [<span data-ttu-id="608c1-208">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="608c1-208">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="608c1-209"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL \_ 紋理 \_ 環境 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-209"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="608c1-210">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-210">Property</span></span> | <span data-ttu-id="608c1-211">值</span><span class="sxs-lookup"><span data-stu-id="608c1-211">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="608c1-212">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-212">Description:</span></span>     | <span data-ttu-id="608c1-213">材質應用程式函式</span><span class="sxs-lookup"><span data-stu-id="608c1-213">Texture application function</span></span>         |
| <span data-ttu-id="608c1-214">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-214">Attribute group:</span></span> | <span data-ttu-id="608c1-215">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-215">texture</span></span>                              |
| <span data-ttu-id="608c1-216">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-216">Initial value:</span></span>   | <span data-ttu-id="608c1-217">GL \_ LAMBERT</span><span class="sxs-lookup"><span data-stu-id="608c1-217">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="608c1-218">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-218">Get command:</span></span>     | [<span data-ttu-id="608c1-219">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="608c1-219">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="608c1-220"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL \_ 紋理 \_ 環境 \_ 色彩</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-220"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

| <span data-ttu-id="608c1-221">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-221">Property</span></span> | <span data-ttu-id="608c1-222">值</span><span class="sxs-lookup"><span data-stu-id="608c1-222">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="608c1-223">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-223">Description:</span></span>     | <span data-ttu-id="608c1-224">材質環境色彩</span><span class="sxs-lookup"><span data-stu-id="608c1-224">Texture environment color</span></span>            |
| <span data-ttu-id="608c1-225">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-225">Attribute group:</span></span> | <span data-ttu-id="608c1-226">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-226">texture</span></span>                              |
| <span data-ttu-id="608c1-227">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-227">Initial value:</span></span>   | <span data-ttu-id="608c1-228">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="608c1-228">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="608c1-229">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-229">Get command:</span></span>     | [<span data-ttu-id="608c1-230">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="608c1-230">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="608c1-231"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ 材質 \_ GEN \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-231"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

| <span data-ttu-id="608c1-232">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-232">Property</span></span> | <span data-ttu-id="608c1-233">值</span><span class="sxs-lookup"><span data-stu-id="608c1-233">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="608c1-234">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-234">Description:</span></span>     | <span data-ttu-id="608c1-235">Texgen 已啟用 (*x* 是 S、T、R 或 Q) </span><span class="sxs-lookup"><span data-stu-id="608c1-235">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="608c1-236">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-236">Attribute group:</span></span> | <span data-ttu-id="608c1-237">材質/啟用</span><span class="sxs-lookup"><span data-stu-id="608c1-237">texture/enable</span></span>                           |
| <span data-ttu-id="608c1-238">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-238">Initial value:</span></span>   | <span data-ttu-id="608c1-239">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="608c1-239">GL\_FALSE</span></span>                                |
| <span data-ttu-id="608c1-240">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-240">Get command:</span></span>     | [<span data-ttu-id="608c1-241">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="608c1-241">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="608c1-242"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL \_ 眼 \_ 平面</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-242"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

| <span data-ttu-id="608c1-243">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-243">Property</span></span> | <span data-ttu-id="608c1-244">值</span><span class="sxs-lookup"><span data-stu-id="608c1-244">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="608c1-245">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-245">Description:</span></span>     | <span data-ttu-id="608c1-246">Texgen 平面方程式係數</span><span class="sxs-lookup"><span data-stu-id="608c1-246">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="608c1-247">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-247">Attribute group:</span></span> | <span data-ttu-id="608c1-248">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-248">texture</span></span>                              |
| <span data-ttu-id="608c1-249">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-249">Initial value:</span></span>   |                                      |
| <span data-ttu-id="608c1-250">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-250">Get command:</span></span>     | [<span data-ttu-id="608c1-251">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="608c1-251">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="608c1-252"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL \_ 物件 \_ 平面</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-252"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

| <span data-ttu-id="608c1-253">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-253">Property</span></span> | <span data-ttu-id="608c1-254">值</span><span class="sxs-lookup"><span data-stu-id="608c1-254">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="608c1-255">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-255">Description:</span></span>     | <span data-ttu-id="608c1-256">Texgen 物件線性係數</span><span class="sxs-lookup"><span data-stu-id="608c1-256">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="608c1-257">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-257">Attribute group:</span></span> | <span data-ttu-id="608c1-258">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-258">texture</span></span>                              |
| <span data-ttu-id="608c1-259">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-259">Initial value:</span></span>   |                                      |
| <span data-ttu-id="608c1-260">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-260">Get command:</span></span>     | [<span data-ttu-id="608c1-261">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="608c1-261">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="608c1-262"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL \_ 材質 \_ 產生 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="608c1-262"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="608c1-263">屬性</span><span class="sxs-lookup"><span data-stu-id="608c1-263">Property</span></span> | <span data-ttu-id="608c1-264">值</span><span class="sxs-lookup"><span data-stu-id="608c1-264">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="608c1-265">描述：</span><span class="sxs-lookup"><span data-stu-id="608c1-265">Description:</span></span>     | <span data-ttu-id="608c1-266">用於 texgen 的函式</span><span class="sxs-lookup"><span data-stu-id="608c1-266">Function used for texgen</span></span>             |
| <span data-ttu-id="608c1-267">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="608c1-267">Attribute group:</span></span> | <span data-ttu-id="608c1-268">紋理</span><span class="sxs-lookup"><span data-stu-id="608c1-268">texture</span></span>                              |
| <span data-ttu-id="608c1-269">初始值：</span><span class="sxs-lookup"><span data-stu-id="608c1-269">Initial value:</span></span>   | <span data-ttu-id="608c1-270">GL \_ 眼 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="608c1-270">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="608c1-271">取得命令：</span><span class="sxs-lookup"><span data-stu-id="608c1-271">Get command:</span></span>     | [<span data-ttu-id="608c1-272">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="608c1-272">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




