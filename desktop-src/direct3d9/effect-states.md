---
description: 效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: '效果狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe92661fda82bd7dfa47ead0061ef8606e422a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998865"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="6fc24-103">效果狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="6fc24-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="6fc24-104">效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。</span><span class="sxs-lookup"><span data-stu-id="6fc24-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="6fc24-105">其中：</span><span class="sxs-lookup"><span data-stu-id="6fc24-105">Where:</span></span>

-   <span data-ttu-id="6fc24-106">效果狀態-類似于傳統的固定函式管線狀態。</span><span class="sxs-lookup"><span data-stu-id="6fc24-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="6fc24-107">以下提供完整的狀態清單。</span><span class="sxs-lookup"><span data-stu-id="6fc24-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="6fc24-108">\[\[ \] 索引 \]-選擇性的整數索引。</span><span class="sxs-lookup"><span data-stu-id="6fc24-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="6fc24-109">索引會識別效果狀態陣列內的特定狀態。</span><span class="sxs-lookup"><span data-stu-id="6fc24-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="6fc24-110">外部括弧表示索引是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="6fc24-111">如果使用索引，請務必使用內部括弧。</span><span class="sxs-lookup"><span data-stu-id="6fc24-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="6fc24-112">運算式狀態指派運算式。</span><span class="sxs-lookup"><span data-stu-id="6fc24-112">expression - State assignment expression.</span></span> <span data-ttu-id="6fc24-113">請參閱 [ (Direct3D 9) 的運算式 ](expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc24-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="6fc24-114">每個狀態都有原生資料類型。</span><span class="sxs-lookup"><span data-stu-id="6fc24-114">Each state has a native data type.</span></span> <span data-ttu-id="6fc24-115">這是當效果指派值時，狀態預期值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6fc24-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="6fc24-116">以下列出每個狀態所預期的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6fc24-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="6fc24-117">請注意，效果介面會盡可能儘早地將值轉換成適當的類型。</span><span class="sxs-lookup"><span data-stu-id="6fc24-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="6fc24-118">常值可以在編譯時期轉換。</span><span class="sxs-lookup"><span data-stu-id="6fc24-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="6fc24-119">非常值 (亦即，當呼叫適當的 Set 方法時，) 需要轉換的一般變數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="6fc24-120">例如，如有必要，效果介面會轉換使用 [**SetBool**](id3dxbaseeffect--setbool.md)、 [**SetValue**](id3dxbaseeffect--setvalue.md)和其他類似函式設定的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="6fc24-121">為了獲得更好的效能，請確定傳遞至效果介面的值已經是正確的類型，而且不需要轉換。</span><span class="sxs-lookup"><span data-stu-id="6fc24-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="6fc24-122">如果執行時間無法轉換值，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6fc24-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="6fc24-123">效果狀態可以分成下列類別：</span><span class="sxs-lookup"><span data-stu-id="6fc24-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="6fc24-124">亮州</span><span class="sxs-lookup"><span data-stu-id="6fc24-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="6fc24-125">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="6fc24-126">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="6fc24-127">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="6fc24-128">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="6fc24-129">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="6fc24-130">取樣器階段狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="6fc24-131">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="6fc24-132">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="6fc24-133">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="6fc24-134">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="6fc24-135">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="6fc24-136">亮州</span><span class="sxs-lookup"><span data-stu-id="6fc24-136">Light States</span></span>

<span data-ttu-id="6fc24-137">若要啟用效果的最佳效能，應該在效果檔案中指定燈光或材質的所有元件。</span><span class="sxs-lookup"><span data-stu-id="6fc24-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="6fc24-138">您無法宣告的狀態會設定為某個預設值，因為 Direct3D 無法個別設定燈的狀態。</span><span class="sxs-lookup"><span data-stu-id="6fc24-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



| <span data-ttu-id="6fc24-139">亮州</span><span class="sxs-lookup"><span data-stu-id="6fc24-139">Light State</span></span>            | <span data-ttu-id="6fc24-140">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-140">Type</span></span>   | <span data-ttu-id="6fc24-141">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-141">Values</span></span>                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc24-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="6fc24-143">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-143">float4</span></span> | <span data-ttu-id="6fc24-144">請參閱 [**D3DLIGHT9**](d3dlight9.md)的環境成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="6fc24-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="6fc24-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-146">float</span></span>  | <span data-ttu-id="6fc24-147">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation0 成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="6fc24-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="6fc24-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-149">float</span></span>  | <span data-ttu-id="6fc24-150">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation1 成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="6fc24-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="6fc24-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-152">float</span></span>  | <span data-ttu-id="6fc24-153">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation2 成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="6fc24-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="6fc24-155">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-155">float4</span></span> | <span data-ttu-id="6fc24-156">請參閱 [**D3DLIGHT9**](d3dlight9.md)的擴散成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="6fc24-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="6fc24-158">float3</span><span class="sxs-lookup"><span data-stu-id="6fc24-158">float3</span></span> | <span data-ttu-id="6fc24-159">請參閱 [**D3DLIGHT9**](d3dlight9.md)的方向成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="6fc24-160">LightEnable \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="6fc24-161">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-161">bool</span></span>   | <span data-ttu-id="6fc24-162">**TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6fc24-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="6fc24-163">請參閱 [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)中的 bEnable 引數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="6fc24-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="6fc24-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-165">float</span></span>  | <span data-ttu-id="6fc24-166">[**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc24-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="6fc24-167">請參閱 [**D3DLIGHT9**](d3dlight9.md)的衰減成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="6fc24-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="6fc24-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-169">float</span></span>  | <span data-ttu-id="6fc24-170">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Phi 成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="6fc24-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="6fc24-172">float3</span><span class="sxs-lookup"><span data-stu-id="6fc24-172">float3</span></span> | <span data-ttu-id="6fc24-173">請參閱 [**D3DLIGHT9**](d3dlight9.md)的位置成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="6fc24-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-174">LightRange\[n\]</span></span>        | <span data-ttu-id="6fc24-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-175">float</span></span>  | <span data-ttu-id="6fc24-176">請參閱 [**D3DLIGHT9**](d3dlight9.md)的範圍成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="6fc24-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="6fc24-178">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-178">float4</span></span> | <span data-ttu-id="6fc24-179">請參閱 [**D3DLIGHT9**](d3dlight9.md)的反射成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="6fc24-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="6fc24-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-181">float</span></span>  | <span data-ttu-id="6fc24-182">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Theta 成員。</span><span class="sxs-lookup"><span data-stu-id="6fc24-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="6fc24-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-183">LightType\[n\]</span></span>         | <span data-ttu-id="6fc24-184">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-184">dword</span></span>  | <span data-ttu-id="6fc24-185">與最多 n 個 [**D3DLIGHTTYPE**](./d3dlighttype.md) 值陣列相同的值，不含 D3DLIGHT \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="6fc24-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="6fc24-186">範例：</span><span class="sxs-lookup"><span data-stu-id="6fc24-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="6fc24-187">這會啟用光源、將點光源設定為類型、將光線位置設定為 float3<10.0 f、1.0 f、23.0 f>，然後將環境色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>。</span><span class="sxs-lookup"><span data-stu-id="6fc24-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="6fc24-188">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-188">Material States</span></span>

<span data-ttu-id="6fc24-189">因為 Direct3D 無法個別設定材質狀態，所以您無法宣告的狀態會設定為某些預設值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



| <span data-ttu-id="6fc24-190">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-190">Material State</span></span>   | <span data-ttu-id="6fc24-191">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-191">Type</span></span>   | <span data-ttu-id="6fc24-192">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-192">Values</span></span>                                         |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="6fc24-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="6fc24-193">MaterialAmbient</span></span>  | <span data-ttu-id="6fc24-194">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-194">float4</span></span> | <span data-ttu-id="6fc24-195">與環境相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="6fc24-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="6fc24-196">>materialdiffuse</span><span class="sxs-lookup"><span data-stu-id="6fc24-196">MaterialDiffuse</span></span>  | <span data-ttu-id="6fc24-197">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-197">float4</span></span> | <span data-ttu-id="6fc24-198">與漫射相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="6fc24-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="6fc24-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="6fc24-199">MaterialEmissive</span></span> | <span data-ttu-id="6fc24-200">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-200">float4</span></span> | <span data-ttu-id="6fc24-201">與放射相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="6fc24-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="6fc24-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="6fc24-202">MaterialPower</span></span>    | <span data-ttu-id="6fc24-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-203">float</span></span>  | <span data-ttu-id="6fc24-204">與電源相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="6fc24-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="6fc24-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="6fc24-205">MaterialSpecular</span></span> | <span data-ttu-id="6fc24-206">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-206">float4</span></span> | <span data-ttu-id="6fc24-207">與反射的值相同[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="6fc24-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="6fc24-208">範例：</span><span class="sxs-lookup"><span data-stu-id="6fc24-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="6fc24-209">這會將擴散色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>，並讓材質 3.0 f 的威力。</span><span class="sxs-lookup"><span data-stu-id="6fc24-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="6fc24-210">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-210">Render States</span></span>

<span data-ttu-id="6fc24-211">轉譯狀態有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="6fc24-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="6fc24-212">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="6fc24-213">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="6fc24-214">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="6fc24-215">效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="6fc24-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fc24-216">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-216">Render State</span></span></td>
<td><span data-ttu-id="6fc24-217">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-217">Type</span></span></td>
<td><span data-ttu-id="6fc24-218">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="6fc24-220">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-220">bool</span></span></td>
<td><span data-ttu-id="6fc24-221">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-221">True or False.</span></span> <span data-ttu-id="6fc24-222">與 <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>中 D3DRS_ALPHABLENDENABLE 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="6fc24-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="6fc24-224">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-224">dword</span></span></td>
<td><span data-ttu-id="6fc24-225">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="6fc24-226">請參閱 D3DRS_ALPHAFUNC。</span><span class="sxs-lookup"><span data-stu-id="6fc24-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="6fc24-227">AlphaRef</span></span></td>
<td><span data-ttu-id="6fc24-228">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-228">dword</span></span></td>
<td><span data-ttu-id="6fc24-229">與 D3DRS_ALPHAREF 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="6fc24-231">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-231">dword</span></span></td>
<td><span data-ttu-id="6fc24-232">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-232">True or False.</span></span> <span data-ttu-id="6fc24-233">請參閱 D3DRS_ALPHATESTENABLE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="6fc24-234">BlendOp</span></span></td>
<td><span data-ttu-id="6fc24-235">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-235">dword</span></span></td>
<td><span data-ttu-id="6fc24-236">與沒有 D3DBLENDOP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="6fc24-238">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-238">dword</span></span></td>
<td><span data-ttu-id="6fc24-239">紅色的位元組合 |綠色 |藍色 |阿 爾 法。</span><span class="sxs-lookup"><span data-stu-id="6fc24-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="6fc24-240">請參閱 D3DRS_COLORWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="6fc24-241">DepthBias</span></span></td>
<td><span data-ttu-id="6fc24-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-242">float</span></span></td>
<td><span data-ttu-id="6fc24-243">與 D3DRS_DEPTHBIAS 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="6fc24-244">DestBlend</span></span></td>
<td><span data-ttu-id="6fc24-245">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-245">dword</span></span></td>
<td><span data-ttu-id="6fc24-246">與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-247">DitherEnable</span></span></td>
<td><span data-ttu-id="6fc24-248">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-248">bool</span></span></td>
<td><span data-ttu-id="6fc24-249">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-249">True or False.</span></span> <span data-ttu-id="6fc24-250">與 D3DRS_DITHERENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="6fc24-251">FillMode</span></span></td>
<td><span data-ttu-id="6fc24-252">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-252">dword</span></span></td>
<td><span data-ttu-id="6fc24-253">與沒有 D3DFILL_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="6fc24-254">LastPixel</span></span></td>
<td><span data-ttu-id="6fc24-255">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-255">dword</span></span></td>
<td><span data-ttu-id="6fc24-256">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-256">True or False.</span></span> <span data-ttu-id="6fc24-257">請參閱 D3DRS_LASTPIXEL。</span><span class="sxs-lookup"><span data-stu-id="6fc24-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-258">ShadeMode</span><span class="sxs-lookup"><span data-stu-id="6fc24-258">ShadeMode</span></span></td>
<td><span data-ttu-id="6fc24-259">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-259">dword</span></span></td>
<td><span data-ttu-id="6fc24-260">與沒有 D3DSHADE_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="6fc24-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="6fc24-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-262">float</span></span></td>
<td><span data-ttu-id="6fc24-263">與 D3DRS_SLOPESCALEDEPTHBIAS 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="6fc24-264">SrcBlend</span></span></td>
<td><span data-ttu-id="6fc24-265">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-265">dword</span></span></td>
<td><span data-ttu-id="6fc24-266">與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="6fc24-268">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-268">bool</span></span></td>
<td><span data-ttu-id="6fc24-269">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-269">True or False.</span></span> <span data-ttu-id="6fc24-270">與 D3DRS_SRGBWRITEENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-271">StencilEnable</span></span></td>
<td><span data-ttu-id="6fc24-272">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-272">bool</span></span></td>
<td><span data-ttu-id="6fc24-273">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-273">True or False.</span></span> <span data-ttu-id="6fc24-274">與 D3DRS_STENCILENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="6fc24-275">StencilFail</span></span></td>
<td><span data-ttu-id="6fc24-276">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-276">dword</span></span></td>
<td><span data-ttu-id="6fc24-277">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="6fc24-278">請參閱 D3DRS_STENCILFAIL。</span><span class="sxs-lookup"><span data-stu-id="6fc24-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="6fc24-279">StencilFunc</span></span></td>
<td><span data-ttu-id="6fc24-280">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-280">dword</span></span></td>
<td><span data-ttu-id="6fc24-281">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="6fc24-282">請參閱 D3DRS_STENCILFUNC。</span><span class="sxs-lookup"><span data-stu-id="6fc24-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="6fc24-283">StencilMask</span></span></td>
<td><span data-ttu-id="6fc24-284">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-284">dword</span></span></td>
<td><span data-ttu-id="6fc24-285">與 D3DRS_STENCILMASK 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="6fc24-286">StencilPass</span></span></td>
<td><span data-ttu-id="6fc24-287">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-287">dword</span></span></td>
<td><span data-ttu-id="6fc24-288">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="6fc24-289">請參閱 D3DRS_STENCILPASS。</span><span class="sxs-lookup"><span data-stu-id="6fc24-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="6fc24-290">StencilRef</span></span></td>
<td><span data-ttu-id="6fc24-291">int</span><span class="sxs-lookup"><span data-stu-id="6fc24-291">int</span></span></td>
<td><span data-ttu-id="6fc24-292">與 D3DRS_STENCILREF 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="6fc24-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="6fc24-294">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-294">dword</span></span></td>
<td><span data-ttu-id="6fc24-295">與 D3DRS_STENCILWRITEMASK 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="6fc24-296">StencilZFail</span></span></td>
<td><span data-ttu-id="6fc24-297">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-297">dword</span></span></td>
<td><span data-ttu-id="6fc24-298">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="6fc24-299">請參閱 D3DRS_STENCILZFAIL。</span><span class="sxs-lookup"><span data-stu-id="6fc24-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="6fc24-300">TextureFactor</span></span></td>
<td><span data-ttu-id="6fc24-301">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-301">dword</span></span></td>
<td><span data-ttu-id="6fc24-302">與 <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="6fc24-303">與 D3DRS_TEXTUREFACTOR 的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="6fc24-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="6fc24-305">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-305">dword</span></span></td>
<td><span data-ttu-id="6fc24-306">值與 D3DRS_WRAP0 所使用的值相同。</span><span class="sxs-lookup"><span data-stu-id="6fc24-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="6fc24-307">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6fc24-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="6fc24-308">對應至 D3DWRAPCOORD_0 的 COORD0 () </span><span class="sxs-lookup"><span data-stu-id="6fc24-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="6fc24-309">對應至 D3DWRAPCOORD_1 的 COORD1 () </span><span class="sxs-lookup"><span data-stu-id="6fc24-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="6fc24-310">對應至 D3DWRAPCOORD_2 的 COORD2 () </span><span class="sxs-lookup"><span data-stu-id="6fc24-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="6fc24-311">對應至 D3DWRAPCOORD_3 的 COORD3 () </span><span class="sxs-lookup"><span data-stu-id="6fc24-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="6fc24-312">U (對應至 D3DWRAP_U) </span><span class="sxs-lookup"><span data-stu-id="6fc24-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="6fc24-313">對應至 D3DWRAP_V 的 V () </span><span class="sxs-lookup"><span data-stu-id="6fc24-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="6fc24-314">對應至 D3DWRAP_W 的 W () </span><span class="sxs-lookup"><span data-stu-id="6fc24-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-315">ZEnable</span></span></td>
<td><span data-ttu-id="6fc24-316">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-316">dword</span></span></td>
<td><span data-ttu-id="6fc24-317">與沒有 D3DZB_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fc24-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="6fc24-318">ZFunc</span></span></td>
<td><span data-ttu-id="6fc24-319">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-319">dword</span></span></td>
<td><span data-ttu-id="6fc24-320">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="6fc24-321">請參閱 D3DRS_ZFUNC。</span><span class="sxs-lookup"><span data-stu-id="6fc24-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fc24-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="6fc24-323">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-323">bool</span></span></td>
<td><span data-ttu-id="6fc24-324">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-324">True or False.</span></span> <span data-ttu-id="6fc24-325">請參閱 D3DRS_ZWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6fc24-326">範例：</span><span class="sxs-lookup"><span data-stu-id="6fc24-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="6fc24-327">這會啟用 Alpha 混色，並讓所有幾何以線框呈現。</span><span class="sxs-lookup"><span data-stu-id="6fc24-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="6fc24-328">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="6fc24-329">效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="6fc24-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



| <span data-ttu-id="6fc24-330">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-330">Render State</span></span>             | <span data-ttu-id="6fc24-331">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-331">Type</span></span>   | <span data-ttu-id="6fc24-332">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-332">Values</span></span>                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc24-333">環境</span><span class="sxs-lookup"><span data-stu-id="6fc24-333">Ambient</span></span>                  | <span data-ttu-id="6fc24-334">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-334">float4</span></span> | <span data-ttu-id="6fc24-335">與 D3DRS 環境相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="6fc24-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="6fc24-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="6fc24-337">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-337">dword</span></span>  | <span data-ttu-id="6fc24-338">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="6fc24-339">請參閱 D3DRS \_ AMBIENTMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="6fc24-340">裁剪</span><span class="sxs-lookup"><span data-stu-id="6fc24-340">Clipping</span></span>                 | <span data-ttu-id="6fc24-341">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-341">bool</span></span>   | <span data-ttu-id="6fc24-342">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-342">True or False.</span></span> <span data-ttu-id="6fc24-343">與 D3DRS 裁剪相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="6fc24-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="6fc24-345">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-345">dword</span></span>  | <span data-ttu-id="6fc24-346">D3DCLIPPLANE0-D3DCLIPPLANE5 宏的位元組合。</span><span class="sxs-lookup"><span data-stu-id="6fc24-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="6fc24-347">請參閱 [**D3DCLIPPLANEn**](d3dclipplanen.md) 和 D3DRS \_ CLIPPLANEENABLE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="6fc24-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="6fc24-348">ColorVertex</span></span>              | <span data-ttu-id="6fc24-349">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-349">bool</span></span>   | <span data-ttu-id="6fc24-350">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-350">True or False.</span></span> <span data-ttu-id="6fc24-351">與 D3DRS COLORVERTEX 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="6fc24-352">CullMode</span><span class="sxs-lookup"><span data-stu-id="6fc24-352">CullMode</span></span>                 | <span data-ttu-id="6fc24-353">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-353">dword</span></span>  | <span data-ttu-id="6fc24-354">與沒有 D3DCULL 前置詞的 [**D3DCULL**](./d3dcull.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="6fc24-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="6fc24-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="6fc24-356">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-356">dword</span></span>  | <span data-ttu-id="6fc24-357">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="6fc24-358">請參閱 D3DRS \_ DIFFUSEMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="6fc24-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="6fc24-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="6fc24-360">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-360">dword</span></span>  | <span data-ttu-id="6fc24-361">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="6fc24-362">請參閱 D3DRS \_ EMISSIVEMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="6fc24-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="6fc24-363">FogColor</span></span>                 | <span data-ttu-id="6fc24-364">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-364">dword</span></span>  | <span data-ttu-id="6fc24-365">與 [**D3DCOLOR**](d3dcolor.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="6fc24-366">請參閱 D3DRS \_ FOGCOLOR。</span><span class="sxs-lookup"><span data-stu-id="6fc24-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="6fc24-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="6fc24-367">FogDensity</span></span>               | <span data-ttu-id="6fc24-368">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-368">float</span></span>  | <span data-ttu-id="6fc24-369">與 D3DRS FOGDENSITY 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="6fc24-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-370">FogEnable</span></span>                | <span data-ttu-id="6fc24-371">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-371">bool</span></span>   | <span data-ttu-id="6fc24-372">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-372">True or False.</span></span> <span data-ttu-id="6fc24-373">與 D3DRS FOGENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="6fc24-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="6fc24-374">FogEnd</span></span>                   | <span data-ttu-id="6fc24-375">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-375">float</span></span>  | <span data-ttu-id="6fc24-376">與 D3DRS FOGEND 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="6fc24-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="6fc24-377">FogStart</span></span>                 | <span data-ttu-id="6fc24-378">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-378">float</span></span>  | <span data-ttu-id="6fc24-379">與 D3DRS FOGSTART 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="6fc24-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="6fc24-380">FogTableMode</span></span>             | <span data-ttu-id="6fc24-381">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-381">dword</span></span>  | <span data-ttu-id="6fc24-382">與 [**D3DFOGMODE**](./d3dfogmode.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="6fc24-383">請參閱 \_ [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)中的 D3DRS FOGTABLEMODE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="6fc24-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="6fc24-384">FogVertexMode</span></span>            | <span data-ttu-id="6fc24-385">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-385">dword</span></span>  | <span data-ttu-id="6fc24-386">與沒有 D3DFOG 前置詞的 [**D3DFOGMODE**](./d3dfogmode.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="6fc24-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="6fc24-388">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-388">bool</span></span>   | <span data-ttu-id="6fc24-389">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-389">True or False.</span></span> <span data-ttu-id="6fc24-390">與 D3DRS INDEXEDVERTEXBLENDENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="6fc24-391">光源</span><span class="sxs-lookup"><span data-stu-id="6fc24-391">Lighting</span></span>                 | <span data-ttu-id="6fc24-392">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-392">bool</span></span>   | <span data-ttu-id="6fc24-393">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-393">True or False.</span></span> <span data-ttu-id="6fc24-394">與 D3DRS 光源相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="6fc24-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="6fc24-395">LocalViewer</span></span>              | <span data-ttu-id="6fc24-396">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-396">bool</span></span>   | <span data-ttu-id="6fc24-397">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-397">True or False.</span></span> <span data-ttu-id="6fc24-398">與 D3DRS LOCALVIEWER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="6fc24-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="6fc24-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="6fc24-400">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-400">bool</span></span>   | <span data-ttu-id="6fc24-401">與 D3DRS MULTISAMPLEANTIALIAS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="6fc24-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="6fc24-402">MultiSampleMask</span></span>          | <span data-ttu-id="6fc24-403">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-403">dword</span></span>  | <span data-ttu-id="6fc24-404">與 D3DRS MULTISAMPLEMASK 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="6fc24-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="6fc24-405">NormalizeNormals</span></span>         | <span data-ttu-id="6fc24-406">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-406">bool</span></span>   | <span data-ttu-id="6fc24-407">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-407">True or False.</span></span> <span data-ttu-id="6fc24-408">與 D3DRS NORMALIZENORMALS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="6fc24-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="6fc24-409">PatchSegments</span></span>            | <span data-ttu-id="6fc24-410">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-410">float</span></span>  | <span data-ttu-id="6fc24-411">與 [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)中的 nSegments 相同的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="6fc24-412">PointScale \_</span><span class="sxs-lookup"><span data-stu-id="6fc24-412">PointScale\_A</span></span>            | <span data-ttu-id="6fc24-413">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-413">float</span></span>  | <span data-ttu-id="6fc24-414">與 D3DRS \_ POINTSCALE A 相同 \_ 的值。</span><span class="sxs-lookup"><span data-stu-id="6fc24-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="6fc24-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="6fc24-415">PointScale\_B</span></span>            | <span data-ttu-id="6fc24-416">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-416">float</span></span>  | <span data-ttu-id="6fc24-417">與 D3DRS POINTSCALE B 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="6fc24-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="6fc24-418">PointScale\_C</span></span>            | <span data-ttu-id="6fc24-419">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-419">float</span></span>  | <span data-ttu-id="6fc24-420">與 D3DRS POINTSCALE C 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="6fc24-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-421">PointScaleEnable</span></span>         | <span data-ttu-id="6fc24-422">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-422">bool</span></span>   | <span data-ttu-id="6fc24-423">與 D3DRS POINTSCALEENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="6fc24-424">Dialog</span><span class="sxs-lookup"><span data-stu-id="6fc24-424">PointSize</span></span>                | <span data-ttu-id="6fc24-425">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-425">float</span></span>  | <span data-ttu-id="6fc24-426">與 D3DRS dialog 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="6fc24-427">Dialog \_ 分鐘</span><span class="sxs-lookup"><span data-stu-id="6fc24-427">PointSize\_Min</span></span>           | <span data-ttu-id="6fc24-428">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-428">float</span></span>  | <span data-ttu-id="6fc24-429">與 D3DRS dialog MIN 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="6fc24-430">Dialog \_ Max</span><span class="sxs-lookup"><span data-stu-id="6fc24-430">PointSize\_Max</span></span>           | <span data-ttu-id="6fc24-431">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-431">float</span></span>  | <span data-ttu-id="6fc24-432">與 D3DRS \_ dialog MAX 相同 \_ 的值，不含 D3DRS \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="6fc24-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="6fc24-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-433">PointSpriteEnable</span></span>        | <span data-ttu-id="6fc24-434">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-434">bool</span></span>   | <span data-ttu-id="6fc24-435">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-435">True or False.</span></span> <span data-ttu-id="6fc24-436">與 D3DRS POINTSPRITEENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="6fc24-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-437">RangeFogEnable</span></span>           | <span data-ttu-id="6fc24-438">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-438">bool</span></span>   | <span data-ttu-id="6fc24-439">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-439">True or False.</span></span> <span data-ttu-id="6fc24-440">與 D3DRS RANGEFOGENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="6fc24-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="6fc24-441">SpecularEnable</span></span>           | <span data-ttu-id="6fc24-442">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-442">bool</span></span>   | <span data-ttu-id="6fc24-443">是非題。</span><span class="sxs-lookup"><span data-stu-id="6fc24-443">True or False.</span></span> <span data-ttu-id="6fc24-444">與 D3DRS SPECULARENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="6fc24-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="6fc24-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="6fc24-446">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-446">dword</span></span>  | <span data-ttu-id="6fc24-447">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="6fc24-448">請參閱 D3DRS \_ SPECULARMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="6fc24-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="6fc24-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="6fc24-449">TweenFactor</span></span>              | <span data-ttu-id="6fc24-450">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-450">float</span></span>  | <span data-ttu-id="6fc24-451">與 D3DRS TWEENFACTOR 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="6fc24-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="6fc24-452">VertexBlend</span></span>              | <span data-ttu-id="6fc24-453">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-453">dword</span></span>  | <span data-ttu-id="6fc24-454">與沒有 D3DVBF 前置詞的 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="6fc24-455">請參閱 D3DRS \_ VERTEXBLEND。</span><span class="sxs-lookup"><span data-stu-id="6fc24-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="6fc24-456">範例：</span><span class="sxs-lookup"><span data-stu-id="6fc24-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="6fc24-457">這會使環境色彩 float4<0.7 f、0.0 f、0.0 f、1.0 f>、將背面剔除模式設定為逆時針方向，並將 [霧化色彩] 設定為紅色。</span><span class="sxs-lookup"><span data-stu-id="6fc24-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="6fc24-458">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-458">Sampler States</span></span>

<span data-ttu-id="6fc24-459">取樣器狀態代表取樣器物件。</span><span class="sxs-lookup"><span data-stu-id="6fc24-459">A sampler state represents a sampler object.</span></span>



| <span data-ttu-id="6fc24-460">狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-460">State</span></span>   | <span data-ttu-id="6fc24-461">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-461">Type</span></span>    | <span data-ttu-id="6fc24-462">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-462">Values</span></span>                              |
|---------|---------|-------------------------------------|
| <span data-ttu-id="6fc24-463">取樣器</span><span class="sxs-lookup"><span data-stu-id="6fc24-463">Sampler</span></span> | <span data-ttu-id="6fc24-464">採樣</span><span class="sxs-lookup"><span data-stu-id="6fc24-464">sampler</span></span> | <span data-ttu-id="6fc24-465">**Null** 或取樣器狀態欄塊。</span><span class="sxs-lookup"><span data-stu-id="6fc24-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="6fc24-466">取樣器階段狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-466">Sampler Stage States</span></span>

<span data-ttu-id="6fc24-467">取樣器階段狀態是用來取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="6fc24-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="6fc24-468">取樣器狀態決定篩選類型和材質定址模式。</span><span class="sxs-lookup"><span data-stu-id="6fc24-468">Sampler state determines filtering types and texture addressing modes.</span></span>



| <span data-ttu-id="6fc24-469">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-469">Sampler State</span></span>       | <span data-ttu-id="6fc24-470">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-470">Type</span></span>                         | <span data-ttu-id="6fc24-471">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-471">Values</span></span>                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc24-472">AddressU \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-472">AddressU\[16\]</span></span>      | <span data-ttu-id="6fc24-473">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-473">dword</span></span>                        | <span data-ttu-id="6fc24-474">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="6fc24-475">請參閱 D3DSAMP \_ ADDRESSU。</span><span class="sxs-lookup"><span data-stu-id="6fc24-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="6fc24-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-476">AddressV\[16\]</span></span>      | <span data-ttu-id="6fc24-477">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-477">dword</span></span>                        | <span data-ttu-id="6fc24-478">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="6fc24-479">請參閱 D3DSAMP \_ ADDRESSV。</span><span class="sxs-lookup"><span data-stu-id="6fc24-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="6fc24-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-480">AddressW\[16\]</span></span>      | <span data-ttu-id="6fc24-481">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-481">dword</span></span>                        | <span data-ttu-id="6fc24-482">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="6fc24-483">請參閱 D3DSAMP \_ ADDRESSW。</span><span class="sxs-lookup"><span data-stu-id="6fc24-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="6fc24-484">邊框 \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="6fc24-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="6fc24-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="6fc24-486">與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="6fc24-487">請參閱 D3DSAMP \_ 邊框出。</span><span class="sxs-lookup"><span data-stu-id="6fc24-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="6fc24-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="6fc24-489">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-489">dword</span></span>                        | <span data-ttu-id="6fc24-490">與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="6fc24-491">請參閱 D3DSAMP \_ MAGFILTER。</span><span class="sxs-lookup"><span data-stu-id="6fc24-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="6fc24-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="6fc24-493">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-493">dword</span></span>                        | <span data-ttu-id="6fc24-494">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXANISOTROPY 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="6fc24-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="6fc24-496">int</span><span class="sxs-lookup"><span data-stu-id="6fc24-496">int</span></span>                          | <span data-ttu-id="6fc24-497">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXMIPLEVEL 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="6fc24-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="6fc24-499">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-499">dword</span></span>                        | <span data-ttu-id="6fc24-500">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MINFILTER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="6fc24-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="6fc24-502">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-502">dword</span></span>                        | <span data-ttu-id="6fc24-503">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPFILTER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="6fc24-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="6fc24-505">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-505">float</span></span>                        | <span data-ttu-id="6fc24-506">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPMAPLODBIAS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="6fc24-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="6fc24-507">SRGBTexture</span></span>         | <span data-ttu-id="6fc24-508">bool</span><span class="sxs-lookup"><span data-stu-id="6fc24-508">bool</span></span>                         | <span data-ttu-id="6fc24-509">與 D3DSAMP SRGBTEXTURE 的值相同， \_ 不含 D3DSAMP \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="6fc24-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="6fc24-510">範例：</span><span class="sxs-lookup"><span data-stu-id="6fc24-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="6fc24-511">這個個會 UVW 值介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="6fc24-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="6fc24-512">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-512">Shader States</span></span>

<span data-ttu-id="6fc24-513">只有兩種效果著色器狀態：一個與頂點著色器物件相關聯，另一個與圖元著色器物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="6fc24-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



| <span data-ttu-id="6fc24-514">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-514">Shader State</span></span> | <span data-ttu-id="6fc24-515">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-515">Type</span></span>         | <span data-ttu-id="6fc24-516">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-516">Values</span></span>                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6fc24-517">無效</span><span class="sxs-lookup"><span data-stu-id="6fc24-517">PixelShader</span></span>  | <span data-ttu-id="6fc24-518">無效</span><span class="sxs-lookup"><span data-stu-id="6fc24-518">pixelshader</span></span>  | <span data-ttu-id="6fc24-519">**Null**、元件區塊、編譯目標或圖元著色器參數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="6fc24-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="6fc24-520">VertexShader</span></span> | <span data-ttu-id="6fc24-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="6fc24-521">vertexshader</span></span> | <span data-ttu-id="6fc24-522">**Null**、元件區塊、編譯目標或圖元著色器參數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="6fc24-523">範例：</span><span class="sxs-lookup"><span data-stu-id="6fc24-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="6fc24-524">這會將 VSTexture （稍早在 fx 檔案中定義的頂點著色器）編譯為頂點著色器1.1 版，然後將該編譯的著色器設定為頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="6fc24-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="6fc24-525">圖元著色器會指派給 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6fc24-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="6fc24-526">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-526">Shader Constant States</span></span>

<span data-ttu-id="6fc24-527">著色器常數狀態可用來存取著色器常數參數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-527">Shader constant states are used to access shader constant parameters.</span></span>



| <span data-ttu-id="6fc24-528">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-528">Shader Constant State</span></span> | <span data-ttu-id="6fc24-529">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-529">Type</span></span>            | <span data-ttu-id="6fc24-530">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-530">Values</span></span>                                       |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="6fc24-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="6fc24-531">PixelShaderConstant</span></span>   | <span data-ttu-id="6fc24-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="6fc24-533">m x n 浮點數的陣列;m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="6fc24-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="6fc24-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="6fc24-535">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-535">float4</span></span>          | <span data-ttu-id="6fc24-536">一個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-536">One 4D float.</span></span>                                |
| <span data-ttu-id="6fc24-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="6fc24-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="6fc24-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="6fc24-538">float4x2</span></span>        | <span data-ttu-id="6fc24-539">兩個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="6fc24-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="6fc24-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="6fc24-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="6fc24-541">float4x3</span></span>        | <span data-ttu-id="6fc24-542">三個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="6fc24-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="6fc24-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="6fc24-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="6fc24-544">float4x4</span></span>        | <span data-ttu-id="6fc24-545">四個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="6fc24-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="6fc24-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="6fc24-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="6fc24-548">m x n bool 的陣列;m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="6fc24-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="6fc24-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="6fc24-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="6fc24-551">m x n 的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc24-551">m x n array of ints.</span></span> <span data-ttu-id="6fc24-552">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-552">m and n are optional.</span></span>   |
| <span data-ttu-id="6fc24-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="6fc24-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="6fc24-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="6fc24-555">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc24-555">m x n array of floats.</span></span> <span data-ttu-id="6fc24-556">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-556">m and n are optional.</span></span> |
| <span data-ttu-id="6fc24-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="6fc24-557">VertexShaderConstant</span></span>  | <span data-ttu-id="6fc24-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="6fc24-559">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc24-559">m x n array of floats.</span></span> <span data-ttu-id="6fc24-560">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-560">m and n are optional.</span></span> |
| <span data-ttu-id="6fc24-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="6fc24-561">VertexShaderConstant1</span></span> | <span data-ttu-id="6fc24-562">float4</span><span class="sxs-lookup"><span data-stu-id="6fc24-562">float4</span></span>          | <span data-ttu-id="6fc24-563">一個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-563">One 4D float.</span></span>                                |
| <span data-ttu-id="6fc24-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="6fc24-564">VertexShaderConstant2</span></span> | <span data-ttu-id="6fc24-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="6fc24-565">float4x2</span></span>        | <span data-ttu-id="6fc24-566">兩個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="6fc24-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="6fc24-567">VertexShaderConstant3</span></span> | <span data-ttu-id="6fc24-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="6fc24-568">float4x3</span></span>        | <span data-ttu-id="6fc24-569">三個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="6fc24-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="6fc24-570">VertexShaderConstant4</span></span> | <span data-ttu-id="6fc24-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="6fc24-571">float4x4</span></span>        | <span data-ttu-id="6fc24-572">四個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="6fc24-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="6fc24-573">VertexShaderConstantB</span></span> | <span data-ttu-id="6fc24-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="6fc24-575">m x n bool 陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc24-575">m x n array of bools.</span></span> <span data-ttu-id="6fc24-576">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-576">m and n are optional.</span></span>  |
| <span data-ttu-id="6fc24-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="6fc24-577">VertexShaderConstantI</span></span> | <span data-ttu-id="6fc24-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="6fc24-579">m x n 的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc24-579">m x n array of ints.</span></span> <span data-ttu-id="6fc24-580">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-580">m and n are optional.</span></span>   |
| <span data-ttu-id="6fc24-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="6fc24-581">VertexShaderConstantF</span></span> | <span data-ttu-id="6fc24-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="6fc24-583">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc24-583">m x n array of floats.</span></span> <span data-ttu-id="6fc24-584">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fc24-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="6fc24-585">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-585">Texture States</span></span>

<span data-ttu-id="6fc24-586">材質狀態會初始化多紋理 blender 所使用的材質。</span><span class="sxs-lookup"><span data-stu-id="6fc24-586">Texture states initialize textures used by the multitexture blender.</span></span>



| <span data-ttu-id="6fc24-587">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-587">Texture State</span></span> | <span data-ttu-id="6fc24-588">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-588">Type</span></span>    | <span data-ttu-id="6fc24-589">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-589">Values</span></span>                            |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="6fc24-590">材質 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-590">Texture\[8\]</span></span>  | <span data-ttu-id="6fc24-591">紋理</span><span class="sxs-lookup"><span data-stu-id="6fc24-591">texture</span></span> | <span data-ttu-id="6fc24-592">**Null** 或紋理參數。</span><span class="sxs-lookup"><span data-stu-id="6fc24-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="6fc24-593">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-593">Texture Stage States</span></span>

<span data-ttu-id="6fc24-594">材質階段狀態會設定多紋理 blender 中的材質和紋理階段。</span><span class="sxs-lookup"><span data-stu-id="6fc24-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



| <span data-ttu-id="6fc24-595">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-595">Texture Stage State</span></span>        | <span data-ttu-id="6fc24-596">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-596">Type</span></span>  | <span data-ttu-id="6fc24-597">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-597">Values</span></span>                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc24-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="6fc24-599">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-599">dword</span></span> | <span data-ttu-id="6fc24-600">與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="6fc24-601">請參閱 D3DTSS \_ ALPHAOP。</span><span class="sxs-lookup"><span data-stu-id="6fc24-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="6fc24-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="6fc24-603">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-603">dword</span></span> | <span data-ttu-id="6fc24-604">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-605">請參閱 D3DTSS \_ ALPHAARG0。</span><span class="sxs-lookup"><span data-stu-id="6fc24-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="6fc24-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="6fc24-607">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-607">dword</span></span> | <span data-ttu-id="6fc24-608">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-609">請參閱 D3DTSS \_ ALPHAARG1。</span><span class="sxs-lookup"><span data-stu-id="6fc24-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="6fc24-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="6fc24-611">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-611">dword</span></span> | <span data-ttu-id="6fc24-612">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-613">請參閱 D3DTSS \_ ALPHAARG2。</span><span class="sxs-lookup"><span data-stu-id="6fc24-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="6fc24-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="6fc24-615">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-615">dword</span></span> | <span data-ttu-id="6fc24-616">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-617">請參閱 D3DTSS \_ COLORARG0。</span><span class="sxs-lookup"><span data-stu-id="6fc24-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="6fc24-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="6fc24-619">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-619">dword</span></span> | <span data-ttu-id="6fc24-620">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-621">請參閱 D3DTSS \_ COLORARG1。</span><span class="sxs-lookup"><span data-stu-id="6fc24-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="6fc24-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="6fc24-623">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-623">dword</span></span> | <span data-ttu-id="6fc24-624">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-625">請參閱 D3DTSS \_ COLORARG2。</span><span class="sxs-lookup"><span data-stu-id="6fc24-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="6fc24-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="6fc24-627">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-627">dword</span></span> | <span data-ttu-id="6fc24-628">與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="6fc24-629">請參閱 D3DTSS \_ COLOROP。</span><span class="sxs-lookup"><span data-stu-id="6fc24-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="6fc24-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="6fc24-631">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-631">float</span></span> | <span data-ttu-id="6fc24-632">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLSCALE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="6fc24-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="6fc24-634">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-634">float</span></span> | <span data-ttu-id="6fc24-635">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLOFFSET 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="6fc24-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="6fc24-637">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-637">float</span></span> | <span data-ttu-id="6fc24-638">與 D3DTSS BUMPENVMAT00 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="6fc24-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="6fc24-640">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-640">float</span></span> | <span data-ttu-id="6fc24-641">與 D3DTSS BUMPENVMAT01 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="6fc24-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="6fc24-643">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-643">float</span></span> | <span data-ttu-id="6fc24-644">與 D3DTSS BUMPENVMAT10 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="6fc24-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="6fc24-646">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6fc24-646">float</span></span> | <span data-ttu-id="6fc24-647">與 D3DTSS BUMPENVMAT11 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="6fc24-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="6fc24-649">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-649">dword</span></span> | <span data-ttu-id="6fc24-650">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="6fc24-651">請參閱 D3DTSS \_ RESULTARG。</span><span class="sxs-lookup"><span data-stu-id="6fc24-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="6fc24-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="6fc24-653">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-653">dword</span></span> | <span data-ttu-id="6fc24-654">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS TEXCOORDINDEX 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="6fc24-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="6fc24-656">dword</span><span class="sxs-lookup"><span data-stu-id="6fc24-656">dword</span></span> | <span data-ttu-id="6fc24-657">與沒有 D3DTTFF 前置詞的 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 值相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="6fc24-658">請參閱 D3DTSS \_ TEXTURETRANSFORMFLAGS。</span><span class="sxs-lookup"><span data-stu-id="6fc24-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="6fc24-659">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-659">Transform States</span></span>

<span data-ttu-id="6fc24-660">設定轉換狀態以初始化轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="6fc24-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="6fc24-661">效果會使用已轉置的矩陣來提高效率。</span><span class="sxs-lookup"><span data-stu-id="6fc24-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="6fc24-662">您可以將已轉換的矩陣提供給效果，或在使用矩陣之前自動變換矩陣。</span><span class="sxs-lookup"><span data-stu-id="6fc24-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



| <span data-ttu-id="6fc24-663">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="6fc24-663">Transform State</span></span>       | <span data-ttu-id="6fc24-664">類型</span><span class="sxs-lookup"><span data-stu-id="6fc24-664">Type</span></span>     | <span data-ttu-id="6fc24-665">值</span><span class="sxs-lookup"><span data-stu-id="6fc24-665">Values</span></span>                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc24-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="6fc24-666">ProjectionTransform</span></span>   | <span data-ttu-id="6fc24-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="6fc24-667">float4x4</span></span> | <span data-ttu-id="6fc24-668">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="6fc24-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="6fc24-669">與 \_ 沒有 D3DTS 前置詞的 D3DTS 投射相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="6fc24-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="6fc24-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="6fc24-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="6fc24-671">float4x4</span></span> | <span data-ttu-id="6fc24-672">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="6fc24-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="6fc24-673">與沒有 D3DTS 前置詞的 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="6fc24-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="6fc24-674">ViewTransform</span></span>         | <span data-ttu-id="6fc24-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="6fc24-675">float4x4</span></span> | <span data-ttu-id="6fc24-676">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="6fc24-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="6fc24-677">D3DTS \_ VIEW 與沒有 D3DTS 前置詞的值相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6fc24-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="6fc24-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="6fc24-678">WorldTransform</span></span>        | <span data-ttu-id="6fc24-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="6fc24-679">float4x4</span></span> | <span data-ttu-id="6fc24-680">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="6fc24-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="6fc24-681">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fc24-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fc24-682">效果格式</span><span class="sxs-lookup"><span data-stu-id="6fc24-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
