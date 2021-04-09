---
title: 光源狀態變數
description: 光源狀態變數
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- 燈光狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841283"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="5cde8-104">光源狀態變數</span><span class="sxs-lookup"><span data-stu-id="5cde8-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="5cde8-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL \_ 照明</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-106">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-106">Description:</span></span>     | <span data-ttu-id="5cde8-107">如果已啟用光源則為 True</span><span class="sxs-lookup"><span data-stu-id="5cde8-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="5cde8-108">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-108">Attribute group:</span></span> | <span data-ttu-id="5cde8-109">光源/啟用</span><span class="sxs-lookup"><span data-stu-id="5cde8-109">lighting/enable</span></span>                    |
| <span data-ttu-id="5cde8-110">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-110">Initial value:</span></span>   | <span data-ttu-id="5cde8-111">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="5cde8-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="5cde8-112">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-112">Get command:</span></span>     | [<span data-ttu-id="5cde8-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5cde8-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="5cde8-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL \_ 色彩 \_ 材質</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-115">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-115">Description:</span></span>     | <span data-ttu-id="5cde8-116">如果已啟用色彩追蹤，則為 True</span><span class="sxs-lookup"><span data-stu-id="5cde8-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="5cde8-117">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-117">Attribute group:</span></span> | <span data-ttu-id="5cde8-118">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-118">lighting</span></span>                           |
| <span data-ttu-id="5cde8-119">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-119">Initial value:</span></span>   | <span data-ttu-id="5cde8-120">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="5cde8-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="5cde8-121">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-121">Get command:</span></span>     | [<span data-ttu-id="5cde8-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5cde8-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="5cde8-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL \_ 色彩 \_ 材質 \_ 參數</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5cde8-124">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-124">Description:</span></span>     | <span data-ttu-id="5cde8-125">材質屬性追蹤目前的色彩</span><span class="sxs-lookup"><span data-stu-id="5cde8-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="5cde8-126">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-126">Attribute group:</span></span> | <span data-ttu-id="5cde8-127">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-127">lighting</span></span>                                                                         |
| <span data-ttu-id="5cde8-128">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-128">Initial value:</span></span>   | <span data-ttu-id="5cde8-129">GL \_ 環境 \_ 和 \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="5cde8-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="5cde8-130">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-130">Get command:</span></span>     | [<span data-ttu-id="5cde8-131">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5cde8-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL \_ 色 \_ 材質 \_ 臉部</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5cde8-133">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-133">Description:</span></span>     | <span data-ttu-id="5cde8-134">受色彩追蹤影響的臉部</span><span class="sxs-lookup"><span data-stu-id="5cde8-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="5cde8-135">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-135">Attribute group:</span></span> | <span data-ttu-id="5cde8-136">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-136">lighting</span></span>                                                                         |
| <span data-ttu-id="5cde8-137">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-137">Initial value:</span></span>   | <span data-ttu-id="5cde8-138">GL \_ 正面 \_ 和 \_ 背面</span><span class="sxs-lookup"><span data-stu-id="5cde8-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="5cde8-139">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-139">Get command:</span></span>     | [<span data-ttu-id="5cde8-140">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5cde8-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ 環境</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="5cde8-142">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-142">Description:</span></span>     | <span data-ttu-id="5cde8-143">環境材質色彩</span><span class="sxs-lookup"><span data-stu-id="5cde8-143">Ambient material color</span></span>                   |
| <span data-ttu-id="5cde8-144">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-144">Attribute group:</span></span> | <span data-ttu-id="5cde8-145">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-145">lighting</span></span>                                 |
| <span data-ttu-id="5cde8-146">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-146">Initial value:</span></span>   | <span data-ttu-id="5cde8-147"> (0.2、0.2、0.2、1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="5cde8-148">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-148">Get command:</span></span>     | [<span data-ttu-id="5cde8-149">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="5cde8-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ 擴散</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="5cde8-151">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-151">Description:</span></span>     | <span data-ttu-id="5cde8-152">擴散材質色彩</span><span class="sxs-lookup"><span data-stu-id="5cde8-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="5cde8-153">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-153">Attribute group:</span></span> | <span data-ttu-id="5cde8-154">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-154">lighting</span></span>                                 |
| <span data-ttu-id="5cde8-155">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-155">Initial value:</span></span>   | <span data-ttu-id="5cde8-156"> (0.8、0.8、0.8、1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="5cde8-157">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-157">Get command:</span></span>     | [<span data-ttu-id="5cde8-158">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="5cde8-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ 反射</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="5cde8-160">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-160">Description:</span></span>     | <span data-ttu-id="5cde8-161">反射材質色彩</span><span class="sxs-lookup"><span data-stu-id="5cde8-161">Specular material color</span></span>                  |
| <span data-ttu-id="5cde8-162">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-162">Attribute group:</span></span> | <span data-ttu-id="5cde8-163">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-163">lighting</span></span>                                 |
| <span data-ttu-id="5cde8-164">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-164">Initial value:</span></span>   | <span data-ttu-id="5cde8-165"> (0.0、0.0、0.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="5cde8-166">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-166">Get command:</span></span>     | [<span data-ttu-id="5cde8-167">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="5cde8-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL \_ 排放</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="5cde8-169">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-169">Description:</span></span>     | <span data-ttu-id="5cde8-170">放射材質色彩</span><span class="sxs-lookup"><span data-stu-id="5cde8-170">Emissive material color</span></span>                  |
| <span data-ttu-id="5cde8-171">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-171">Attribute group:</span></span> | <span data-ttu-id="5cde8-172">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-172">lighting</span></span>                                 |
| <span data-ttu-id="5cde8-173">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-173">Initial value:</span></span>   | <span data-ttu-id="5cde8-174"> (0.0、0.0、0.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="5cde8-175">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-175">Get command:</span></span>     | [<span data-ttu-id="5cde8-176">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="5cde8-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ 反光</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="5cde8-178">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-178">Description:</span></span>     | <span data-ttu-id="5cde8-179">材質的反射指數</span><span class="sxs-lookup"><span data-stu-id="5cde8-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="5cde8-180">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-180">Attribute group:</span></span> | <span data-ttu-id="5cde8-181">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-181">lighting</span></span>                                 |
| <span data-ttu-id="5cde8-182">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-182">Initial value:</span></span>   | <span data-ttu-id="5cde8-183">0.0</span><span class="sxs-lookup"><span data-stu-id="5cde8-183">0.0</span></span>                                      |
| <span data-ttu-id="5cde8-184">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-184">Get command:</span></span>     | [<span data-ttu-id="5cde8-185">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="5cde8-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL \_ LIGHT \_ 模型 \_ 環境</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5cde8-187">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-187">Description:</span></span>     | <span data-ttu-id="5cde8-188">環境場景色彩</span><span class="sxs-lookup"><span data-stu-id="5cde8-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="5cde8-189">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-189">Attribute group:</span></span> | <span data-ttu-id="5cde8-190">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-190">lighting</span></span>                                                                       |
| <span data-ttu-id="5cde8-191">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-191">Initial value:</span></span>   | <span data-ttu-id="5cde8-192"> (0.2、0.2、0.2、1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="5cde8-193">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-193">Get command:</span></span>     | [<span data-ttu-id="5cde8-194">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5cde8-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL \_ 光 \_ 模型 \_ 本機 \_ 檢視器</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5cde8-196">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-196">Description:</span></span>     | <span data-ttu-id="5cde8-197">檢視器為本機</span><span class="sxs-lookup"><span data-stu-id="5cde8-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="5cde8-198">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-198">Attribute group:</span></span> | <span data-ttu-id="5cde8-199">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-199">lighting</span></span>                                                                         |
| <span data-ttu-id="5cde8-200">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-200">Initial value:</span></span>   | <span data-ttu-id="5cde8-201">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="5cde8-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="5cde8-202">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-202">Get command:</span></span>     | [<span data-ttu-id="5cde8-203">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5cde8-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL \_ 燈 \_ 模型 \_ 二 \_ 邊</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5cde8-205">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-205">Description:</span></span>     | <span data-ttu-id="5cde8-206">使用雙面光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="5cde8-207">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-207">Attribute group:</span></span> | <span data-ttu-id="5cde8-208">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-208">lighting</span></span>                                                                         |
| <span data-ttu-id="5cde8-209">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-209">Initial value:</span></span>   | <span data-ttu-id="5cde8-210">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="5cde8-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="5cde8-211">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-211">Get command:</span></span>     | [<span data-ttu-id="5cde8-212">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5cde8-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ 環境</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-214">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-214">Description:</span></span>     | <span data-ttu-id="5cde8-215">Light *i* 的環境濃度</span><span class="sxs-lookup"><span data-stu-id="5cde8-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="5cde8-216">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-216">Attribute group:</span></span> | <span data-ttu-id="5cde8-217">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-217">lighting</span></span>                           |
| <span data-ttu-id="5cde8-218">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-218">Initial value:</span></span>   | <span data-ttu-id="5cde8-219"> (0.0、0.0、0.0、1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="5cde8-220">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-220">Get command:</span></span>     | [<span data-ttu-id="5cde8-221">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ 擴散</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-223">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-223">Description:</span></span>     | <span data-ttu-id="5cde8-224">淺 *i* 的擴散濃度</span><span class="sxs-lookup"><span data-stu-id="5cde8-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="5cde8-225">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-225">Attribute group:</span></span> | <span data-ttu-id="5cde8-226">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-226">lighting</span></span>                           |
| <span data-ttu-id="5cde8-227">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="5cde8-228">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-228">Get command:</span></span>     | [<span data-ttu-id="5cde8-229">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ 反射</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-231">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-231">Description:</span></span>     | <span data-ttu-id="5cde8-232">*光源的* 反射濃度</span><span class="sxs-lookup"><span data-stu-id="5cde8-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="5cde8-233">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-233">Attribute group:</span></span> | <span data-ttu-id="5cde8-234">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-234">lighting</span></span>                           |
| <span data-ttu-id="5cde8-235">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="5cde8-236">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-236">Get command:</span></span>     | [<span data-ttu-id="5cde8-237">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL \_ 位置</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-239">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-239">Description:</span></span>     | <span data-ttu-id="5cde8-240">*燈的* 位置</span><span class="sxs-lookup"><span data-stu-id="5cde8-240">Position of light *i*</span></span>              |
| <span data-ttu-id="5cde8-241">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-241">Attribute group:</span></span> | <span data-ttu-id="5cde8-242">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-242">lighting</span></span>                           |
| <span data-ttu-id="5cde8-243">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-243">Initial value:</span></span>   | <span data-ttu-id="5cde8-244"> (0.0、0.0、1.0、0.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="5cde8-245">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-245">Get command:</span></span>     | [<span data-ttu-id="5cde8-246">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL \_ 常數 \_ 衰減</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-248">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-248">Description:</span></span>     | <span data-ttu-id="5cde8-249">定值衰減因數</span><span class="sxs-lookup"><span data-stu-id="5cde8-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="5cde8-250">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-250">Attribute group:</span></span> | <span data-ttu-id="5cde8-251">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-251">lighting</span></span>                           |
| <span data-ttu-id="5cde8-252">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-252">Initial value:</span></span>   | <span data-ttu-id="5cde8-253">1.0</span><span class="sxs-lookup"><span data-stu-id="5cde8-253">1.0</span></span>                                |
| <span data-ttu-id="5cde8-254">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-254">Get command:</span></span>     | [<span data-ttu-id="5cde8-255">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL \_ 線性 \_ 衰減</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-257">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-257">Description:</span></span>     | <span data-ttu-id="5cde8-258">線性衰減因數</span><span class="sxs-lookup"><span data-stu-id="5cde8-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="5cde8-259">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-259">Attribute group:</span></span> | <span data-ttu-id="5cde8-260">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-260">lighting</span></span>                           |
| <span data-ttu-id="5cde8-261">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-261">Initial value:</span></span>   | <span data-ttu-id="5cde8-262">0.0</span><span class="sxs-lookup"><span data-stu-id="5cde8-262">0.0</span></span>                                |
| <span data-ttu-id="5cde8-263">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-263">Get command:</span></span>     | [<span data-ttu-id="5cde8-264">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL \_ 二次 \_ 衰減</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-266">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-266">Description:</span></span>     | <span data-ttu-id="5cde8-267">二次方衰減因數</span><span class="sxs-lookup"><span data-stu-id="5cde8-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="5cde8-268">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-268">Attribute group:</span></span> | <span data-ttu-id="5cde8-269">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-269">lighting</span></span>                           |
| <span data-ttu-id="5cde8-270">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-270">Initial value:</span></span>   | <span data-ttu-id="5cde8-271">0.0</span><span class="sxs-lookup"><span data-stu-id="5cde8-271">0.0</span></span>                                |
| <span data-ttu-id="5cde8-272">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-272">Get command:</span></span>     | [<span data-ttu-id="5cde8-273">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL \_ 點 \_ 方向</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-275">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-275">Description:</span></span>     | <span data-ttu-id="5cde8-276">*淺色的* 焦點方向</span><span class="sxs-lookup"><span data-stu-id="5cde8-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="5cde8-277">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-277">Attribute group:</span></span> | <span data-ttu-id="5cde8-278">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-278">lighting</span></span>                           |
| <span data-ttu-id="5cde8-279">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-279">Initial value:</span></span>   | <span data-ttu-id="5cde8-280"> (0.0、0.0、-1.0) </span><span class="sxs-lookup"><span data-stu-id="5cde8-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="5cde8-281">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-281">Get command:</span></span>     | [<span data-ttu-id="5cde8-282">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL \_ 點 \_ 指數</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-284">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-284">Description:</span></span>     | <span data-ttu-id="5cde8-285">Light *i* 的焦點指數</span><span class="sxs-lookup"><span data-stu-id="5cde8-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="5cde8-286">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-286">Attribute group:</span></span> | <span data-ttu-id="5cde8-287">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-287">lighting</span></span>                           |
| <span data-ttu-id="5cde8-288">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-288">Initial value:</span></span>   | <span data-ttu-id="5cde8-289">0.0</span><span class="sxs-lookup"><span data-stu-id="5cde8-289">0.0</span></span>                                |
| <span data-ttu-id="5cde8-290">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-290">Get command:</span></span>     | [<span data-ttu-id="5cde8-291">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL \_ 點 \_ 截止</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-293">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-293">Description:</span></span>     | <span data-ttu-id="5cde8-294">*光源的* 焦點角度</span><span class="sxs-lookup"><span data-stu-id="5cde8-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="5cde8-295">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-295">Attribute group:</span></span> | <span data-ttu-id="5cde8-296">光源</span><span class="sxs-lookup"><span data-stu-id="5cde8-296">lighting</span></span>                           |
| <span data-ttu-id="5cde8-297">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-297">Initial value:</span></span>   | <span data-ttu-id="5cde8-298">180.0</span><span class="sxs-lookup"><span data-stu-id="5cde8-298">180.0</span></span>                              |
| <span data-ttu-id="5cde8-299">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-299">Get command:</span></span>     | [<span data-ttu-id="5cde8-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="5cde8-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ 燈</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5cde8-302">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-302">Description:</span></span>     | <span data-ttu-id="5cde8-303">如果 *已啟用* 光線，則為 True</span><span class="sxs-lookup"><span data-stu-id="5cde8-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="5cde8-304">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-304">Attribute group:</span></span> | <span data-ttu-id="5cde8-305">光源/啟用</span><span class="sxs-lookup"><span data-stu-id="5cde8-305">lighting/enable</span></span>                    |
| <span data-ttu-id="5cde8-306">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-306">Initial value:</span></span>   | <span data-ttu-id="5cde8-307">GL \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="5cde8-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="5cde8-308">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-308">Get command:</span></span>     | [<span data-ttu-id="5cde8-309">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5cde8-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="5cde8-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL \_ 色彩 \_ 索引</dt> </span><span class="sxs-lookup"><span data-stu-id="5cde8-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5cde8-311">描述：</span><span class="sxs-lookup"><span data-stu-id="5cde8-311">Description:</span></span>     | <span data-ttu-id="5cde8-312">*C (* 色彩索引光源的) 、 *c (d)* 和 *C (s)*</span><span class="sxs-lookup"><span data-stu-id="5cde8-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="5cde8-313">屬性群組：</span><span class="sxs-lookup"><span data-stu-id="5cde8-313">Attribute group:</span></span> | <span data-ttu-id="5cde8-314">光源/啟用</span><span class="sxs-lookup"><span data-stu-id="5cde8-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="5cde8-315">初始值：</span><span class="sxs-lookup"><span data-stu-id="5cde8-315">Initial value:</span></span>   | <span data-ttu-id="5cde8-316">0、1、1</span><span class="sxs-lookup"><span data-stu-id="5cde8-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="5cde8-317">取得命令：</span><span class="sxs-lookup"><span data-stu-id="5cde8-317">Get command:</span></span>     | [<span data-ttu-id="5cde8-318">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5cde8-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




