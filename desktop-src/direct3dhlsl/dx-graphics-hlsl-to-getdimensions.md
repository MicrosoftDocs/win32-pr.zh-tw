---
title: 'GetDimensions (DirectX HLSL 材質物件) '
description: 取得材質大小資訊。 語法區塊會顯示在方法宣告中可能的所有參數。 [備註] 區段中的表格會顯示針對每個材質物件類型所執行的參數。
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841648"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="559cb-105">GetDimensions (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="559cb-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="559cb-106">取得材質大小資訊。</span><span class="sxs-lookup"><span data-stu-id="559cb-106">Gets texture size information.</span></span> <span data-ttu-id="559cb-107">語法區塊會顯示在方法宣告中可能的所有參數。</span><span class="sxs-lookup"><span data-stu-id="559cb-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="559cb-108">[備註] 區段中的表格會顯示針對每個材質物件類型所執行的參數。</span><span class="sxs-lookup"><span data-stu-id="559cb-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="559cb-109">void Object. GetDimensions ( UINT MipLevel、typeX Width、typeX Height、typeX Elements、typeX Depth、typeX NumberOfLevels、typeX NumberOfSamples ) ;</span><span class="sxs-lookup"><span data-stu-id="559cb-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="559cb-110">typeX 表示有兩種可能的類型： **uint** 或 **float**。</span><span class="sxs-lookup"><span data-stu-id="559cb-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="559cb-111">參數</span><span class="sxs-lookup"><span data-stu-id="559cb-111">Parameters</span></span>



| <span data-ttu-id="559cb-112">項目</span><span class="sxs-lookup"><span data-stu-id="559cb-112">Item</span></span>                                                                                                                               | <span data-ttu-id="559cb-113">描述</span><span class="sxs-lookup"><span data-stu-id="559cb-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="559cb-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*</span><span class="sxs-lookup"><span data-stu-id="559cb-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="559cb-115">除 **緩衝區** 物件以外的任何 [材質物件](dx-graphics-hlsl-to-type.md)類型。</span><span class="sxs-lookup"><span data-stu-id="559cb-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="559cb-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="559cb-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="559cb-117">\[以 \] 零為基底的索引，用來識別 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="559cb-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="559cb-118">如果未使用這個引數，則會假設為第一個 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="559cb-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="559cb-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*寬度*</span><span class="sxs-lookup"><span data-stu-id="559cb-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="559cb-120">\[輸出 \] 材質寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="559cb-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="559cb-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*高度*</span><span class="sxs-lookup"><span data-stu-id="559cb-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="559cb-122">\[\]材質中的材質高度。</span><span class="sxs-lookup"><span data-stu-id="559cb-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="559cb-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*元素*</span><span class="sxs-lookup"><span data-stu-id="559cb-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="559cb-124">\[\]陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="559cb-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="559cb-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*深度*</span><span class="sxs-lookup"><span data-stu-id="559cb-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="559cb-126">\[\]材質中的材質深度。</span><span class="sxs-lookup"><span data-stu-id="559cb-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="559cb-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="559cb-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="559cb-128">\[\]mipmap 層級的數目。</span><span class="sxs-lookup"><span data-stu-id="559cb-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="559cb-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="559cb-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="559cb-130">\[\]樣本數。</span><span class="sxs-lookup"><span data-stu-id="559cb-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="559cb-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="559cb-131">Return Value</span></span>

<span data-ttu-id="559cb-132">無</span><span class="sxs-lookup"><span data-stu-id="559cb-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="559cb-133">多載方法</span><span class="sxs-lookup"><span data-stu-id="559cb-133">Overloaded Methods</span></span>

<span data-ttu-id="559cb-134">下表列出所有不同版本的方法;版本與輸入參數的數目不同。</span><span class="sxs-lookup"><span data-stu-id="559cb-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="559cb-135">請注意，對於採用整數參數的每個方法，有一個使用浮點參數的多載方法。</span><span class="sxs-lookup"><span data-stu-id="559cb-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="559cb-136">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="559cb-136">Texture-Object Type</span></span> | <span data-ttu-id="559cb-137">輸入參數</span><span class="sxs-lookup"><span data-stu-id="559cb-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="559cb-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="559cb-138">Texture1D</span></span>           | <span data-ttu-id="559cb-139">UINT MipLevel、UINT Width、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="559cb-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="559cb-140">Texture1D</span></span>           | <span data-ttu-id="559cb-141">UINT 寬度</span><span class="sxs-lookup"><span data-stu-id="559cb-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="559cb-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="559cb-142">Texture1D</span></span>           | <span data-ttu-id="559cb-143">UINT MipLevel、float Width、float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="559cb-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="559cb-144">Texture1D</span></span>           | <span data-ttu-id="559cb-145">浮點數寬度</span><span class="sxs-lookup"><span data-stu-id="559cb-145">float Width</span></span>                                                                    |
| <span data-ttu-id="559cb-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-146">Texture1DArray</span></span>      | <span data-ttu-id="559cb-147">UINT MipLevel、UINT Width、UINT 元素、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="559cb-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-148">Texture1DArray</span></span>      | <span data-ttu-id="559cb-149">UINT 寬度、UINT 元素</span><span class="sxs-lookup"><span data-stu-id="559cb-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="559cb-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-150">Texture1DArray</span></span>      | <span data-ttu-id="559cb-151">UINT MipLevel、float Width、float Elements、float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="559cb-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-152">Texture1DArray</span></span>      | <span data-ttu-id="559cb-153">浮點數寬度、浮點數元素</span><span class="sxs-lookup"><span data-stu-id="559cb-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="559cb-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="559cb-154">Texture2D</span></span>           | <span data-ttu-id="559cb-155">UINT MipLevel、UINT Width、UINT Height、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="559cb-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="559cb-156">Texture2D</span></span>           | <span data-ttu-id="559cb-157">UINT 寬度、UINT 高度</span><span class="sxs-lookup"><span data-stu-id="559cb-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="559cb-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="559cb-158">Texture2D</span></span>           | <span data-ttu-id="559cb-159">UINT MipLevel、float Width、float Height、float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="559cb-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="559cb-160">Texture2D</span></span>           | <span data-ttu-id="559cb-161">浮點數寬度、浮點數高度</span><span class="sxs-lookup"><span data-stu-id="559cb-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="559cb-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-162">Texture2DArray</span></span>      | <span data-ttu-id="559cb-163">UINT MipLevel、UINT Width、UINT Height、UINT 元素、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="559cb-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-164">Texture2DArray</span></span>      | <span data-ttu-id="559cb-165">UINT Width、UINT Height、UINT 元素</span><span class="sxs-lookup"><span data-stu-id="559cb-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="559cb-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-166">Texture2DArray</span></span>      | <span data-ttu-id="559cb-167">UINT MipLevel、float Width、float Height、float Elements、float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="559cb-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="559cb-168">Texture2DArray</span></span>      | <span data-ttu-id="559cb-169">浮點數寬度、浮點數高度、浮點數元素</span><span class="sxs-lookup"><span data-stu-id="559cb-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="559cb-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="559cb-170">Texture3D</span></span>           | <span data-ttu-id="559cb-171">UINT MipLevel、UINT Width、UINT Height、UINT Depth、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="559cb-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="559cb-172">Texture3D</span></span>           | <span data-ttu-id="559cb-173">UINT 寬度、UINT 高度、UINT 深度</span><span class="sxs-lookup"><span data-stu-id="559cb-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="559cb-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="559cb-174">Texture3D</span></span>           | <span data-ttu-id="559cb-175">UINT MipLevel、float Width、float Height、float Depth、float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="559cb-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="559cb-176">Texture3D</span></span>           | <span data-ttu-id="559cb-177">浮點數寬度、浮點數高度、浮點數深度</span><span class="sxs-lookup"><span data-stu-id="559cb-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="559cb-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="559cb-178">TextureCube</span></span>         | <span data-ttu-id="559cb-179">UINT MipLevel、UINT Width、UINT Height、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="559cb-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="559cb-180">TextureCube</span></span>         | <span data-ttu-id="559cb-181">UINT 寬度、UINT 高度</span><span class="sxs-lookup"><span data-stu-id="559cb-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="559cb-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="559cb-182">TextureCube</span></span>         | <span data-ttu-id="559cb-183">UINT MipLevel、float Width、float Height、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="559cb-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="559cb-184">TextureCube</span></span>         | <span data-ttu-id="559cb-185">浮點數寬度、浮點數高度</span><span class="sxs-lookup"><span data-stu-id="559cb-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="559cb-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="559cb-186">TextureCubeArray</span></span>    | <span data-ttu-id="559cb-187">UINT MipLevel、UINT Width、UINT Height、UINT 元素、UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="559cb-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="559cb-188">TextureCubeArray</span></span>    | <span data-ttu-id="559cb-189">UINT Width、UINT Height、UINT 元素</span><span class="sxs-lookup"><span data-stu-id="559cb-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="559cb-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="559cb-190">TextureCubeArray</span></span>    | <span data-ttu-id="559cb-191">UINT MipLevel、float Width、float Height、float Elements、float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="559cb-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="559cb-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="559cb-192">TextureCubeArray</span></span>    | <span data-ttu-id="559cb-193">浮點數寬度、浮點數高度、浮點數元素</span><span class="sxs-lookup"><span data-stu-id="559cb-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="559cb-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="559cb-194">Texture2DMS</span></span>         | <span data-ttu-id="559cb-195">UINT 寬度、UINT 高度、UINT 樣本</span><span class="sxs-lookup"><span data-stu-id="559cb-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="559cb-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="559cb-196">Texture2DMS</span></span>         | <span data-ttu-id="559cb-197">浮點數寬度、浮點數高度、浮點數範例</span><span class="sxs-lookup"><span data-stu-id="559cb-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="559cb-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="559cb-198">Texture2DMSArray</span></span>    | <span data-ttu-id="559cb-199">UINT 寬度、UINT Height、UINT 元素、UINT 範例</span><span class="sxs-lookup"><span data-stu-id="559cb-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="559cb-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="559cb-200">Texture2DMSArray</span></span>    | <span data-ttu-id="559cb-201">浮點數寬度、浮點數高度、浮點數元素、浮點數範例</span><span class="sxs-lookup"><span data-stu-id="559cb-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="559cb-202">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="559cb-202">Minimum Shader Model</span></span>

<span data-ttu-id="559cb-203">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="559cb-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="559cb-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="559cb-204">vs\_4\_0</span></span> | <span data-ttu-id="559cb-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="559cb-205">vs\_4\_1</span></span>  | <span data-ttu-id="559cb-206">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="559cb-206">ps\_4\_0</span></span> | <span data-ttu-id="559cb-207">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="559cb-207">ps\_4\_1</span></span>  | <span data-ttu-id="559cb-208">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="559cb-208">gs\_4\_0</span></span> | <span data-ttu-id="559cb-209">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="559cb-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="559cb-210">x</span><span class="sxs-lookup"><span data-stu-id="559cb-210">x</span></span>        | <span data-ttu-id="559cb-211">x</span><span class="sxs-lookup"><span data-stu-id="559cb-211">x</span></span>         | <span data-ttu-id="559cb-212">x</span><span class="sxs-lookup"><span data-stu-id="559cb-212">x</span></span>        | <span data-ttu-id="559cb-213">x</span><span class="sxs-lookup"><span data-stu-id="559cb-213">x</span></span>         | <span data-ttu-id="559cb-214">x</span><span class="sxs-lookup"><span data-stu-id="559cb-214">x</span></span>        | <span data-ttu-id="559cb-215">x</span><span class="sxs-lookup"><span data-stu-id="559cb-215">x</span></span>         |



 

1.  <span data-ttu-id="559cb-216">傳回最大 (第零個) mipmap 層級的維度。</span><span class="sxs-lookup"><span data-stu-id="559cb-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="559cb-217">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="559cb-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="559cb-218">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="559cb-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="559cb-219">相關主題</span><span class="sxs-lookup"><span data-stu-id="559cb-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="559cb-220">材質物件</span><span class="sxs-lookup"><span data-stu-id="559cb-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





