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
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967456"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="2ae34-104">紋理狀態變數</span><span class="sxs-lookup"><span data-stu-id="2ae34-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="2ae34-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ 材質 \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="2ae34-106">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-106">Description:</span></span>     | <span data-ttu-id="2ae34-107">如果   已啟用 x-d 紋理 (*x* 為 1-d 或 2-d) ，則為 True</span><span class="sxs-lookup"><span data-stu-id="2ae34-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="2ae34-108">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-108">Attribute group:</span></span> | <span data-ttu-id="2ae34-109">材質/啟用</span><span class="sxs-lookup"><span data-stu-id="2ae34-109">texture/enable</span></span>                                        |
| <span data-ttu-id="2ae34-110">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-110">Initial value:</span></span>   | <span data-ttu-id="2ae34-111">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="2ae34-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="2ae34-112">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-112">Get command:</span></span>     | [<span data-ttu-id="2ae34-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2ae34-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="2ae34-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL \_ 材質</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="2ae34-115">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-115">Description:</span></span>     | <span data-ttu-id="2ae34-116">*x*  - *D 詳細資料* 層級的-D 紋理影像</span><span class="sxs-lookup"><span data-stu-id="2ae34-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="2ae34-117">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="2ae34-118">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="2ae34-119">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-119">Get command:</span></span>     | [<span data-ttu-id="2ae34-120">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="2ae34-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="2ae34-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL \_ 材質 \_ 寬度</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="2ae34-122">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-122">Description:</span></span>     | <span data-ttu-id="2ae34-123">*x*  -D 紋理影像 *我*   的寬度</span><span class="sxs-lookup"><span data-stu-id="2ae34-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="2ae34-124">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="2ae34-125">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-125">Initial value:</span></span>   | <span data-ttu-id="2ae34-126">0</span><span class="sxs-lookup"><span data-stu-id="2ae34-126">0</span></span>                                                        |
| <span data-ttu-id="2ae34-127">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-127">Get command:</span></span>     | [<span data-ttu-id="2ae34-128">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="2ae34-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL \_ 材質 \_ 高度</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="2ae34-130">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-130">Description:</span></span>     | <span data-ttu-id="2ae34-131">*x*  -D 紋理影像 *我*   的高度</span><span class="sxs-lookup"><span data-stu-id="2ae34-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="2ae34-132">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="2ae34-133">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-133">Initial value:</span></span>   | <span data-ttu-id="2ae34-134">0</span><span class="sxs-lookup"><span data-stu-id="2ae34-134">0</span></span>                                                        |
| <span data-ttu-id="2ae34-135">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-135">Get command:</span></span>     | [<span data-ttu-id="2ae34-136">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="2ae34-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL \_ 材質 \_ 框線</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="2ae34-138">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-138">Description:</span></span>     | <span data-ttu-id="2ae34-139">*x*  -D 紋理影像 *i*   框線</span><span class="sxs-lookup"><span data-stu-id="2ae34-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="2ae34-140">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="2ae34-141">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-141">Initial value:</span></span>   | <span data-ttu-id="2ae34-142">0</span><span class="sxs-lookup"><span data-stu-id="2ae34-142">0</span></span>                                                        |
| <span data-ttu-id="2ae34-143">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-143">Get command:</span></span>     | [<span data-ttu-id="2ae34-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="2ae34-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL \_ 材質 \_ 元件</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="2ae34-146">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-146">Description:</span></span>     | <span data-ttu-id="2ae34-147">材質影像元件</span><span class="sxs-lookup"><span data-stu-id="2ae34-147">Texture image components</span></span>                                 |
| <span data-ttu-id="2ae34-148">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="2ae34-149">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-149">Initial value:</span></span>   | <span data-ttu-id="2ae34-150">1</span><span class="sxs-lookup"><span data-stu-id="2ae34-150">1</span></span>                                                        |
| <span data-ttu-id="2ae34-151">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-151">Get command:</span></span>     | [<span data-ttu-id="2ae34-152">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="2ae34-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL \_ 紋理 \_ 框線 \_ 色彩</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="2ae34-154">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-154">Description:</span></span>     | <span data-ttu-id="2ae34-155">材質框線色彩</span><span class="sxs-lookup"><span data-stu-id="2ae34-155">Texture border color</span></span>                           |
| <span data-ttu-id="2ae34-156">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-156">Attribute group:</span></span> | <span data-ttu-id="2ae34-157">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-157">texture</span></span>                                        |
| <span data-ttu-id="2ae34-158">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-158">Initial value:</span></span>   | <span data-ttu-id="2ae34-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="2ae34-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="2ae34-160">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-160">Get command:</span></span>     | [<span data-ttu-id="2ae34-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="2ae34-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL \_ 材質 \_ 最小 \_ 篩選</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="2ae34-163">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-163">Description:</span></span>     | <span data-ttu-id="2ae34-164">紋理縮制函式</span><span class="sxs-lookup"><span data-stu-id="2ae34-164">Texture minification function</span></span>                  |
| <span data-ttu-id="2ae34-165">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-165">Attribute group:</span></span> | <span data-ttu-id="2ae34-166">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-166">texture</span></span>                                        |
| <span data-ttu-id="2ae34-167">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-167">Initial value:</span></span>   | <span data-ttu-id="2ae34-168">GL \_ 最接近 \_ MIPMAP \_ 線性</span><span class="sxs-lookup"><span data-stu-id="2ae34-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="2ae34-169">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-169">Get command:</span></span>     | [<span data-ttu-id="2ae34-170">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="2ae34-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL \_ 紋理 \_ MAG \_ 篩選</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="2ae34-172">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-172">Description:</span></span>     | <span data-ttu-id="2ae34-173">材質放大功能</span><span class="sxs-lookup"><span data-stu-id="2ae34-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="2ae34-174">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-174">Attribute group:</span></span> | <span data-ttu-id="2ae34-175">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-175">texture</span></span>                                        |
| <span data-ttu-id="2ae34-176">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-176">Initial value:</span></span>   | <span data-ttu-id="2ae34-177">GL \_ 線性</span><span class="sxs-lookup"><span data-stu-id="2ae34-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="2ae34-178">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-178">Get command:</span></span>     | [<span data-ttu-id="2ae34-179">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="2ae34-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ 材質 \_ 換行 \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="2ae34-181">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-181">Description:</span></span>     | <span data-ttu-id="2ae34-182">材質 wrap 模式 (*x*   是 S 或 T) </span><span class="sxs-lookup"><span data-stu-id="2ae34-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="2ae34-183">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-183">Attribute group:</span></span> | <span data-ttu-id="2ae34-184">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-184">texture</span></span>                                        |
| <span data-ttu-id="2ae34-185">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-185">Initial value:</span></span>   | <span data-ttu-id="2ae34-186">GL \_ 重複</span><span class="sxs-lookup"><span data-stu-id="2ae34-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="2ae34-187">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-187">Get command:</span></span>     | [<span data-ttu-id="2ae34-188">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2ae34-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="2ae34-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL \_ 紋理 \_ 環境 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="2ae34-190">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-190">Description:</span></span>     | <span data-ttu-id="2ae34-191">材質應用程式函式</span><span class="sxs-lookup"><span data-stu-id="2ae34-191">Texture application function</span></span>         |
| <span data-ttu-id="2ae34-192">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-192">Attribute group:</span></span> | <span data-ttu-id="2ae34-193">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-193">texture</span></span>                              |
| <span data-ttu-id="2ae34-194">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-194">Initial value:</span></span>   | <span data-ttu-id="2ae34-195">GL \_ LAMBERT</span><span class="sxs-lookup"><span data-stu-id="2ae34-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="2ae34-196">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-196">Get command:</span></span>     | [<span data-ttu-id="2ae34-197">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="2ae34-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="2ae34-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL \_ 紋理 \_ 環境 \_ 色彩</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="2ae34-199">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-199">Description:</span></span>     | <span data-ttu-id="2ae34-200">材質環境色彩</span><span class="sxs-lookup"><span data-stu-id="2ae34-200">Texture environment color</span></span>            |
| <span data-ttu-id="2ae34-201">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-201">Attribute group:</span></span> | <span data-ttu-id="2ae34-202">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-202">texture</span></span>                              |
| <span data-ttu-id="2ae34-203">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-203">Initial value:</span></span>   | <span data-ttu-id="2ae34-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="2ae34-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="2ae34-205">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-205">Get command:</span></span>     | [<span data-ttu-id="2ae34-206">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="2ae34-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="2ae34-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ 材質 \_ GEN \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="2ae34-208">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-208">Description:</span></span>     | <span data-ttu-id="2ae34-209">Texgen 已啟用 (*x*   是 S、T、R 或 Q) </span><span class="sxs-lookup"><span data-stu-id="2ae34-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="2ae34-210">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-210">Attribute group:</span></span> | <span data-ttu-id="2ae34-211">材質/啟用</span><span class="sxs-lookup"><span data-stu-id="2ae34-211">texture/enable</span></span>                           |
| <span data-ttu-id="2ae34-212">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-212">Initial value:</span></span>   | <span data-ttu-id="2ae34-213">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="2ae34-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="2ae34-214">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-214">Get command:</span></span>     | [<span data-ttu-id="2ae34-215">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2ae34-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="2ae34-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL \_ 眼 \_ 平面</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="2ae34-217">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-217">Description:</span></span>     | <span data-ttu-id="2ae34-218">Texgen 平面方程式係數</span><span class="sxs-lookup"><span data-stu-id="2ae34-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="2ae34-219">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-219">Attribute group:</span></span> | <span data-ttu-id="2ae34-220">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-220">texture</span></span>                              |
| <span data-ttu-id="2ae34-221">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="2ae34-222">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-222">Get command:</span></span>     | [<span data-ttu-id="2ae34-223">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="2ae34-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="2ae34-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL \_ 物件 \_ 平面</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="2ae34-225">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-225">Description:</span></span>     | <span data-ttu-id="2ae34-226">Texgen 物件線性係數</span><span class="sxs-lookup"><span data-stu-id="2ae34-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="2ae34-227">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-227">Attribute group:</span></span> | <span data-ttu-id="2ae34-228">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-228">texture</span></span>                              |
| <span data-ttu-id="2ae34-229">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="2ae34-230">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-230">Get command:</span></span>     | [<span data-ttu-id="2ae34-231">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="2ae34-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="2ae34-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL \_ 材質 \_ 產生 \_ 模式</dt> </span><span class="sxs-lookup"><span data-stu-id="2ae34-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="2ae34-233">描述：</span><span class="sxs-lookup"><span data-stu-id="2ae34-233">Description:</span></span>     | <span data-ttu-id="2ae34-234">用於 texgen 的函式</span><span class="sxs-lookup"><span data-stu-id="2ae34-234">Function used for texgen</span></span>             |
| <span data-ttu-id="2ae34-235">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="2ae34-235">Attribute group:</span></span> | <span data-ttu-id="2ae34-236">紋理</span><span class="sxs-lookup"><span data-stu-id="2ae34-236">texture</span></span>                              |
| <span data-ttu-id="2ae34-237">初始值：</span><span class="sxs-lookup"><span data-stu-id="2ae34-237">Initial value:</span></span>   | <span data-ttu-id="2ae34-238">GL \_ 眼 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="2ae34-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="2ae34-239">取得命令：</span><span class="sxs-lookup"><span data-stu-id="2ae34-239">Get command:</span></span>     | [<span data-ttu-id="2ae34-240">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="2ae34-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




