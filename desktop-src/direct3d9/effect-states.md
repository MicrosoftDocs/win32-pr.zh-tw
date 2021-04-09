---
description: 效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: '效果狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674e72d818cd280bfe75a2cb02733576bc68319e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025728"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="45e73-103">效果狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="45e73-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="45e73-104">效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。</span><span class="sxs-lookup"><span data-stu-id="45e73-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="45e73-105">其中：</span><span class="sxs-lookup"><span data-stu-id="45e73-105">Where:</span></span>

-   <span data-ttu-id="45e73-106">效果狀態-類似于傳統的固定函式管線狀態。</span><span class="sxs-lookup"><span data-stu-id="45e73-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="45e73-107">以下提供完整的狀態清單。</span><span class="sxs-lookup"><span data-stu-id="45e73-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="45e73-108">\[\[ \] 索引 \]-選擇性的整數索引。</span><span class="sxs-lookup"><span data-stu-id="45e73-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="45e73-109">索引會識別效果狀態陣列內的特定狀態。</span><span class="sxs-lookup"><span data-stu-id="45e73-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="45e73-110">外部括弧表示索引是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="45e73-111">如果使用索引，請務必使用內部括弧。</span><span class="sxs-lookup"><span data-stu-id="45e73-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="45e73-112">運算式狀態指派運算式。</span><span class="sxs-lookup"><span data-stu-id="45e73-112">expression - State assignment expression.</span></span> <span data-ttu-id="45e73-113">請參閱 [ (Direct3D 9) 的運算式 ](expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="45e73-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="45e73-114">每個狀態都有原生資料類型。</span><span class="sxs-lookup"><span data-stu-id="45e73-114">Each state has a native data type.</span></span> <span data-ttu-id="45e73-115">這是當效果指派值時，狀態預期值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="45e73-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="45e73-116">以下列出每個狀態所預期的資料類型。</span><span class="sxs-lookup"><span data-stu-id="45e73-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="45e73-117">請注意，效果介面會盡可能儘早地將值轉換成適當的類型。</span><span class="sxs-lookup"><span data-stu-id="45e73-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="45e73-118">常值可以在編譯時期轉換。</span><span class="sxs-lookup"><span data-stu-id="45e73-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="45e73-119">非常值 (亦即，當呼叫適當的 Set 方法時，) 需要轉換的一般變數。</span><span class="sxs-lookup"><span data-stu-id="45e73-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="45e73-120">例如，如有必要，效果介面會轉換使用 [**SetBool**](id3dxbaseeffect--setbool.md)、 [**SetValue**](id3dxbaseeffect--setvalue.md)和其他類似函式設定的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="45e73-121">為了獲得更好的效能，請確定傳遞至效果介面的值已經是正確的類型，而且不需要轉換。</span><span class="sxs-lookup"><span data-stu-id="45e73-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="45e73-122">如果執行時間無法轉換值，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="45e73-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="45e73-123">效果狀態可以分成下列類別：</span><span class="sxs-lookup"><span data-stu-id="45e73-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="45e73-124">亮州</span><span class="sxs-lookup"><span data-stu-id="45e73-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="45e73-125">材質狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="45e73-126">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="45e73-127">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="45e73-128">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="45e73-129">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="45e73-130">取樣器階段狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="45e73-131">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="45e73-132">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="45e73-133">材質狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="45e73-134">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="45e73-135">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="45e73-136">亮州</span><span class="sxs-lookup"><span data-stu-id="45e73-136">Light States</span></span>

<span data-ttu-id="45e73-137">若要啟用效果的最佳效能，應該在效果檔案中指定燈光或材質的所有元件。</span><span class="sxs-lookup"><span data-stu-id="45e73-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="45e73-138">您無法宣告的狀態會設定為某個預設值，因為 Direct3D 無法個別設定燈的狀態。</span><span class="sxs-lookup"><span data-stu-id="45e73-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e73-139">亮州</span><span class="sxs-lookup"><span data-stu-id="45e73-139">Light State</span></span>            | <span data-ttu-id="45e73-140">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-140">Type</span></span>   | <span data-ttu-id="45e73-141">值</span><span class="sxs-lookup"><span data-stu-id="45e73-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="45e73-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="45e73-143">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-143">float4</span></span> | <span data-ttu-id="45e73-144">請參閱 [**D3DLIGHT9**](d3dlight9.md)的環境成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="45e73-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="45e73-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-146">float</span></span>  | <span data-ttu-id="45e73-147">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation0 成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="45e73-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="45e73-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-149">float</span></span>  | <span data-ttu-id="45e73-150">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation1 成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="45e73-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="45e73-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-152">float</span></span>  | <span data-ttu-id="45e73-153">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation2 成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="45e73-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="45e73-155">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-155">float4</span></span> | <span data-ttu-id="45e73-156">請參閱 [**D3DLIGHT9**](d3dlight9.md)的擴散成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="45e73-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="45e73-158">float3</span><span class="sxs-lookup"><span data-stu-id="45e73-158">float3</span></span> | <span data-ttu-id="45e73-159">請參閱 [**D3DLIGHT9**](d3dlight9.md)的方向成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="45e73-160">LightEnable \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="45e73-161">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-161">bool</span></span>   | <span data-ttu-id="45e73-162">**TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="45e73-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="45e73-163">請參閱 [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)中的 bEnable 引數。</span><span class="sxs-lookup"><span data-stu-id="45e73-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="45e73-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="45e73-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-165">float</span></span>  | <span data-ttu-id="45e73-166">[**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="45e73-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="45e73-167">請參閱 [**D3DLIGHT9**](d3dlight9.md)的衰減成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="45e73-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="45e73-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-169">float</span></span>  | <span data-ttu-id="45e73-170">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Phi 成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="45e73-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="45e73-172">float3</span><span class="sxs-lookup"><span data-stu-id="45e73-172">float3</span></span> | <span data-ttu-id="45e73-173">請參閱 [**D3DLIGHT9**](d3dlight9.md)的位置成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="45e73-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-174">LightRange\[n\]</span></span>        | <span data-ttu-id="45e73-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-175">float</span></span>  | <span data-ttu-id="45e73-176">請參閱 [**D3DLIGHT9**](d3dlight9.md)的範圍成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="45e73-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="45e73-178">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-178">float4</span></span> | <span data-ttu-id="45e73-179">請參閱 [**D3DLIGHT9**](d3dlight9.md)的反射成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="45e73-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="45e73-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-181">float</span></span>  | <span data-ttu-id="45e73-182">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Theta 成員。</span><span class="sxs-lookup"><span data-stu-id="45e73-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="45e73-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="45e73-183">LightType\[n\]</span></span>         | <span data-ttu-id="45e73-184">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-184">dword</span></span>  | <span data-ttu-id="45e73-185">與最多 n 個 [**D3DLIGHTTYPE**](./d3dlighttype.md) 值陣列相同的值，不含 D3DLIGHT \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e73-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="45e73-186">範例：</span><span class="sxs-lookup"><span data-stu-id="45e73-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="45e73-187">這會啟用光源、將點光源設定為類型、將光線位置設定為 float3<10.0 f、1.0 f、23.0 f>，然後將環境色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>。</span><span class="sxs-lookup"><span data-stu-id="45e73-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="45e73-188">材質狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-188">Material States</span></span>

<span data-ttu-id="45e73-189">因為 Direct3D 無法個別設定材質狀態，所以您無法宣告的狀態會設定為某些預設值。</span><span class="sxs-lookup"><span data-stu-id="45e73-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="45e73-190">材質狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-190">Material State</span></span>   | <span data-ttu-id="45e73-191">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-191">Type</span></span>   | <span data-ttu-id="45e73-192">值</span><span class="sxs-lookup"><span data-stu-id="45e73-192">Values</span></span>                                         |
| <span data-ttu-id="45e73-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="45e73-193">MaterialAmbient</span></span>  | <span data-ttu-id="45e73-194">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-194">float4</span></span> | <span data-ttu-id="45e73-195">與環境相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="45e73-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="45e73-196">>materialdiffuse</span><span class="sxs-lookup"><span data-stu-id="45e73-196">MaterialDiffuse</span></span>  | <span data-ttu-id="45e73-197">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-197">float4</span></span> | <span data-ttu-id="45e73-198">與漫射相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="45e73-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="45e73-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="45e73-199">MaterialEmissive</span></span> | <span data-ttu-id="45e73-200">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-200">float4</span></span> | <span data-ttu-id="45e73-201">與放射相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="45e73-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="45e73-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="45e73-202">MaterialPower</span></span>    | <span data-ttu-id="45e73-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-203">float</span></span>  | <span data-ttu-id="45e73-204">與電源相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="45e73-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="45e73-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="45e73-205">MaterialSpecular</span></span> | <span data-ttu-id="45e73-206">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-206">float4</span></span> | <span data-ttu-id="45e73-207">與反射的值相同[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="45e73-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="45e73-208">範例：</span><span class="sxs-lookup"><span data-stu-id="45e73-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="45e73-209">這會將擴散色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>，並讓材質 3.0 f 的威力。</span><span class="sxs-lookup"><span data-stu-id="45e73-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="45e73-210">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-210">Render States</span></span>

<span data-ttu-id="45e73-211">轉譯狀態有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="45e73-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="45e73-212">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="45e73-213">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="45e73-214">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="45e73-215">效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e73-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45e73-216">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-216">Render State</span></span></td>
<td><span data-ttu-id="45e73-217">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-217">Type</span></span></td>
<td><span data-ttu-id="45e73-218">值</span><span class="sxs-lookup"><span data-stu-id="45e73-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="45e73-220">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-220">bool</span></span></td>
<td><span data-ttu-id="45e73-221">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-221">True or False.</span></span> <span data-ttu-id="45e73-222">與 <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>中 D3DRS_ALPHABLENDENABLE 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="45e73-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="45e73-224">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-224">dword</span></span></td>
<td><span data-ttu-id="45e73-225">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="45e73-226">請參閱 D3DRS_ALPHAFUNC。</span><span class="sxs-lookup"><span data-stu-id="45e73-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="45e73-227">AlphaRef</span></span></td>
<td><span data-ttu-id="45e73-228">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-228">dword</span></span></td>
<td><span data-ttu-id="45e73-229">與 D3DRS_ALPHAREF 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="45e73-231">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-231">dword</span></span></td>
<td><span data-ttu-id="45e73-232">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-232">True or False.</span></span> <span data-ttu-id="45e73-233">請參閱 D3DRS_ALPHATESTENABLE。</span><span class="sxs-lookup"><span data-stu-id="45e73-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="45e73-234">BlendOp</span></span></td>
<td><span data-ttu-id="45e73-235">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-235">dword</span></span></td>
<td><span data-ttu-id="45e73-236">與沒有 D3DBLENDOP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="45e73-238">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-238">dword</span></span></td>
<td><span data-ttu-id="45e73-239">紅色的位元組合 |綠色 |藍色 |阿 爾 法。</span><span class="sxs-lookup"><span data-stu-id="45e73-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="45e73-240">請參閱 D3DRS_COLORWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="45e73-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="45e73-241">DepthBias</span></span></td>
<td><span data-ttu-id="45e73-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-242">float</span></span></td>
<td><span data-ttu-id="45e73-243">與 D3DRS_DEPTHBIAS 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="45e73-244">DestBlend</span></span></td>
<td><span data-ttu-id="45e73-245">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-245">dword</span></span></td>
<td><span data-ttu-id="45e73-246">與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-247">DitherEnable</span></span></td>
<td><span data-ttu-id="45e73-248">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-248">bool</span></span></td>
<td><span data-ttu-id="45e73-249">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-249">True or False.</span></span> <span data-ttu-id="45e73-250">與 D3DRS_DITHERENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="45e73-251">FillMode</span></span></td>
<td><span data-ttu-id="45e73-252">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-252">dword</span></span></td>
<td><span data-ttu-id="45e73-253">與沒有 D3DFILL_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="45e73-254">LastPixel</span></span></td>
<td><span data-ttu-id="45e73-255">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-255">dword</span></span></td>
<td><span data-ttu-id="45e73-256">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-256">True or False.</span></span> <span data-ttu-id="45e73-257">請參閱 D3DRS_LASTPIXEL。</span><span class="sxs-lookup"><span data-stu-id="45e73-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-258">ShadeMode</span><span class="sxs-lookup"><span data-stu-id="45e73-258">ShadeMode</span></span></td>
<td><span data-ttu-id="45e73-259">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-259">dword</span></span></td>
<td><span data-ttu-id="45e73-260">與沒有 D3DSHADE_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="45e73-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="45e73-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-262">float</span></span></td>
<td><span data-ttu-id="45e73-263">與 D3DRS_SLOPESCALEDEPTHBIAS 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="45e73-264">SrcBlend</span></span></td>
<td><span data-ttu-id="45e73-265">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-265">dword</span></span></td>
<td><span data-ttu-id="45e73-266">與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-267">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-267">StencilEnable</span></span></td>
<td><span data-ttu-id="45e73-268">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-268">bool</span></span></td>
<td><span data-ttu-id="45e73-269">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-269">True or False.</span></span> <span data-ttu-id="45e73-270">與 D3DRS_STENCILENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-270">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-271">StencilFail</span><span class="sxs-lookup"><span data-stu-id="45e73-271">StencilFail</span></span></td>
<td><span data-ttu-id="45e73-272">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-272">dword</span></span></td>
<td><span data-ttu-id="45e73-273">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-273">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="45e73-274">請參閱 D3DRS_STENCILFAIL。</span><span class="sxs-lookup"><span data-stu-id="45e73-274">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-275">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="45e73-275">StencilFunc</span></span></td>
<td><span data-ttu-id="45e73-276">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-276">dword</span></span></td>
<td><span data-ttu-id="45e73-277">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-277">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="45e73-278">請參閱 D3DRS_STENCILFUNC。</span><span class="sxs-lookup"><span data-stu-id="45e73-278">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-279">StencilMask</span><span class="sxs-lookup"><span data-stu-id="45e73-279">StencilMask</span></span></td>
<td><span data-ttu-id="45e73-280">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-280">dword</span></span></td>
<td><span data-ttu-id="45e73-281">與 D3DRS_STENCILMASK 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-281">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-282">StencilPass</span><span class="sxs-lookup"><span data-stu-id="45e73-282">StencilPass</span></span></td>
<td><span data-ttu-id="45e73-283">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-283">dword</span></span></td>
<td><span data-ttu-id="45e73-284">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-284">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="45e73-285">請參閱 D3DRS_STENCILPASS。</span><span class="sxs-lookup"><span data-stu-id="45e73-285">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-286">StencilRef</span><span class="sxs-lookup"><span data-stu-id="45e73-286">StencilRef</span></span></td>
<td><span data-ttu-id="45e73-287">int</span><span class="sxs-lookup"><span data-stu-id="45e73-287">int</span></span></td>
<td><span data-ttu-id="45e73-288">與 D3DRS_STENCILREF 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-288">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-289">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="45e73-289">StencilWriteMask</span></span></td>
<td><span data-ttu-id="45e73-290">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-290">dword</span></span></td>
<td><span data-ttu-id="45e73-291">與 D3DRS_STENCILWRITEMASK 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-291">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-292">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="45e73-292">StencilZFail</span></span></td>
<td><span data-ttu-id="45e73-293">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-293">dword</span></span></td>
<td><span data-ttu-id="45e73-294">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-294">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="45e73-295">請參閱 D3DRS_STENCILZFAIL。</span><span class="sxs-lookup"><span data-stu-id="45e73-295">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-296">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="45e73-296">TextureFactor</span></span></td>
<td><span data-ttu-id="45e73-297">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-297">dword</span></span></td>
<td><span data-ttu-id="45e73-298">與 <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-298">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="45e73-299">與 D3DRS_TEXTUREFACTOR 的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-299">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-300">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="45e73-300">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="45e73-301">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-301">dword</span></span></td>
<td><span data-ttu-id="45e73-302">值與 D3DRS_WRAP0 所使用的值相同。</span><span class="sxs-lookup"><span data-stu-id="45e73-302">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="45e73-303">有效值為：</span><span class="sxs-lookup"><span data-stu-id="45e73-303">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="45e73-304">對應至 D3DWRAPCOORD_0 的 COORD0 () </span><span class="sxs-lookup"><span data-stu-id="45e73-304">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="45e73-305">對應至 D3DWRAPCOORD_1 的 COORD1 () </span><span class="sxs-lookup"><span data-stu-id="45e73-305">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="45e73-306">對應至 D3DWRAPCOORD_2 的 COORD2 () </span><span class="sxs-lookup"><span data-stu-id="45e73-306">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="45e73-307">對應至 D3DWRAPCOORD_3 的 COORD3 () </span><span class="sxs-lookup"><span data-stu-id="45e73-307">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="45e73-308">U (對應至 D3DWRAP_U) </span><span class="sxs-lookup"><span data-stu-id="45e73-308">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="45e73-309">對應至 D3DWRAP_V 的 V () </span><span class="sxs-lookup"><span data-stu-id="45e73-309">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="45e73-310">對應至 D3DWRAP_W 的 W () </span><span class="sxs-lookup"><span data-stu-id="45e73-310">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-311">ZEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-311">ZEnable</span></span></td>
<td><span data-ttu-id="45e73-312">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-312">dword</span></span></td>
<td><span data-ttu-id="45e73-313">與沒有 D3DZB_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-313">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e73-314">ZFunc</span><span class="sxs-lookup"><span data-stu-id="45e73-314">ZFunc</span></span></td>
<td><span data-ttu-id="45e73-315">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-315">dword</span></span></td>
<td><span data-ttu-id="45e73-316">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-316">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="45e73-317">請參閱 D3DRS_ZFUNC。</span><span class="sxs-lookup"><span data-stu-id="45e73-317">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e73-318">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-318">ZWriteEnable</span></span></td>
<td><span data-ttu-id="45e73-319">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-319">bool</span></span></td>
<td><span data-ttu-id="45e73-320">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-320">True or False.</span></span> <span data-ttu-id="45e73-321">請參閱 D3DRS_ZWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="45e73-321">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="45e73-322">範例：</span><span class="sxs-lookup"><span data-stu-id="45e73-322">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="45e73-323">這會啟用 Alpha 混色，並讓所有幾何以線框呈現。</span><span class="sxs-lookup"><span data-stu-id="45e73-323">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="45e73-324">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-324">Vertex Pipe Render States</span></span>

<span data-ttu-id="45e73-325">效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e73-325">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e73-326">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-326">Render State</span></span>             | <span data-ttu-id="45e73-327">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-327">Type</span></span>   | <span data-ttu-id="45e73-328">值</span><span class="sxs-lookup"><span data-stu-id="45e73-328">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="45e73-329">環境</span><span class="sxs-lookup"><span data-stu-id="45e73-329">Ambient</span></span>                  | <span data-ttu-id="45e73-330">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-330">float4</span></span> | <span data-ttu-id="45e73-331">與 D3DRS 環境相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-331">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="45e73-332">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="45e73-332">AmbientMaterialSource</span></span>    | <span data-ttu-id="45e73-333">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-333">dword</span></span>  | <span data-ttu-id="45e73-334">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-334">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="45e73-335">請參閱 D3DRS \_ AMBIENTMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="45e73-335">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="45e73-336">裁剪</span><span class="sxs-lookup"><span data-stu-id="45e73-336">Clipping</span></span>                 | <span data-ttu-id="45e73-337">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-337">bool</span></span>   | <span data-ttu-id="45e73-338">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-338">True or False.</span></span> <span data-ttu-id="45e73-339">與 D3DRS 裁剪相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-339">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="45e73-340">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-340">ClipPlaneEnable</span></span>          | <span data-ttu-id="45e73-341">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-341">dword</span></span>  | <span data-ttu-id="45e73-342">D3DCLIPPLANE0-D3DCLIPPLANE5 宏的位元組合。</span><span class="sxs-lookup"><span data-stu-id="45e73-342">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="45e73-343">請參閱 [**D3DCLIPPLANEn**](d3dclipplanen.md) 和 D3DRS \_ CLIPPLANEENABLE。</span><span class="sxs-lookup"><span data-stu-id="45e73-343">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="45e73-344">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="45e73-344">ColorVertex</span></span>              | <span data-ttu-id="45e73-345">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-345">bool</span></span>   | <span data-ttu-id="45e73-346">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-346">True or False.</span></span> <span data-ttu-id="45e73-347">與 D3DRS COLORVERTEX 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-347">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="45e73-348">CullMode</span><span class="sxs-lookup"><span data-stu-id="45e73-348">CullMode</span></span>                 | <span data-ttu-id="45e73-349">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-349">dword</span></span>  | <span data-ttu-id="45e73-350">與沒有 D3DCULL 前置詞的 [**D3DCULL**](./d3dcull.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-350">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="45e73-351">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="45e73-351">DiffuseMaterialSource</span></span>    | <span data-ttu-id="45e73-352">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-352">dword</span></span>  | <span data-ttu-id="45e73-353">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-353">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="45e73-354">請參閱 D3DRS \_ DIFFUSEMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="45e73-354">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="45e73-355">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="45e73-355">EmissiveMaterialSource</span></span>   | <span data-ttu-id="45e73-356">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-356">dword</span></span>  | <span data-ttu-id="45e73-357">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="45e73-358">請參閱 D3DRS \_ EMISSIVEMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="45e73-358">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="45e73-359">FogColor</span><span class="sxs-lookup"><span data-stu-id="45e73-359">FogColor</span></span>                 | <span data-ttu-id="45e73-360">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-360">dword</span></span>  | <span data-ttu-id="45e73-361">與 [**D3DCOLOR**](d3dcolor.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-361">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="45e73-362">請參閱 D3DRS \_ FOGCOLOR。</span><span class="sxs-lookup"><span data-stu-id="45e73-362">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="45e73-363">FogDensity</span><span class="sxs-lookup"><span data-stu-id="45e73-363">FogDensity</span></span>               | <span data-ttu-id="45e73-364">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-364">float</span></span>  | <span data-ttu-id="45e73-365">與 D3DRS FOGDENSITY 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-365">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="45e73-366">FogEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-366">FogEnable</span></span>                | <span data-ttu-id="45e73-367">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-367">bool</span></span>   | <span data-ttu-id="45e73-368">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-368">True or False.</span></span> <span data-ttu-id="45e73-369">與 D3DRS FOGENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-369">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="45e73-370">FogEnd</span><span class="sxs-lookup"><span data-stu-id="45e73-370">FogEnd</span></span>                   | <span data-ttu-id="45e73-371">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-371">float</span></span>  | <span data-ttu-id="45e73-372">與 D3DRS FOGEND 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-372">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="45e73-373">FogStart</span><span class="sxs-lookup"><span data-stu-id="45e73-373">FogStart</span></span>                 | <span data-ttu-id="45e73-374">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-374">float</span></span>  | <span data-ttu-id="45e73-375">與 D3DRS FOGSTART 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-375">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="45e73-376">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="45e73-376">FogTableMode</span></span>             | <span data-ttu-id="45e73-377">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-377">dword</span></span>  | <span data-ttu-id="45e73-378">與 [**D3DFOGMODE**](./d3dfogmode.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-378">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="45e73-379">請參閱 \_ [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)中的 D3DRS FOGTABLEMODE。</span><span class="sxs-lookup"><span data-stu-id="45e73-379">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="45e73-380">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="45e73-380">FogVertexMode</span></span>            | <span data-ttu-id="45e73-381">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-381">dword</span></span>  | <span data-ttu-id="45e73-382">與沒有 D3DFOG 前置詞的 [**D3DFOGMODE**](./d3dfogmode.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="45e73-383">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-383">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="45e73-384">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-384">bool</span></span>   | <span data-ttu-id="45e73-385">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-385">True or False.</span></span> <span data-ttu-id="45e73-386">與 D3DRS INDEXEDVERTEXBLENDENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-386">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="45e73-387">光源</span><span class="sxs-lookup"><span data-stu-id="45e73-387">Lighting</span></span>                 | <span data-ttu-id="45e73-388">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-388">bool</span></span>   | <span data-ttu-id="45e73-389">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-389">True or False.</span></span> <span data-ttu-id="45e73-390">與 D3DRS 光源相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-390">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="45e73-391">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="45e73-391">LocalViewer</span></span>              | <span data-ttu-id="45e73-392">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-392">bool</span></span>   | <span data-ttu-id="45e73-393">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-393">True or False.</span></span> <span data-ttu-id="45e73-394">與 D3DRS LOCALVIEWER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-394">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="45e73-395">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="45e73-395">MultiSampleAntialias</span></span>     | <span data-ttu-id="45e73-396">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-396">bool</span></span>   | <span data-ttu-id="45e73-397">與 D3DRS MULTISAMPLEANTIALIAS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-397">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="45e73-398">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="45e73-398">MultiSampleMask</span></span>          | <span data-ttu-id="45e73-399">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-399">dword</span></span>  | <span data-ttu-id="45e73-400">與 D3DRS MULTISAMPLEMASK 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-400">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="45e73-401">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="45e73-401">NormalizeNormals</span></span>         | <span data-ttu-id="45e73-402">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-402">bool</span></span>   | <span data-ttu-id="45e73-403">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-403">True or False.</span></span> <span data-ttu-id="45e73-404">與 D3DRS NORMALIZENORMALS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-404">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="45e73-405">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="45e73-405">PatchSegments</span></span>            | <span data-ttu-id="45e73-406">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-406">float</span></span>  | <span data-ttu-id="45e73-407">與 [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)中的 nSegments 相同的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-407">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="45e73-408">PointScale \_</span><span class="sxs-lookup"><span data-stu-id="45e73-408">PointScale\_A</span></span>            | <span data-ttu-id="45e73-409">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-409">float</span></span>  | <span data-ttu-id="45e73-410">與 D3DRS \_ POINTSCALE A 相同 \_ 的值。</span><span class="sxs-lookup"><span data-stu-id="45e73-410">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="45e73-411">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="45e73-411">PointScale\_B</span></span>            | <span data-ttu-id="45e73-412">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-412">float</span></span>  | <span data-ttu-id="45e73-413">與 D3DRS POINTSCALE B 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-413">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="45e73-414">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="45e73-414">PointScale\_C</span></span>            | <span data-ttu-id="45e73-415">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-415">float</span></span>  | <span data-ttu-id="45e73-416">與 D3DRS POINTSCALE C 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-416">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="45e73-417">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-417">PointScaleEnable</span></span>         | <span data-ttu-id="45e73-418">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-418">bool</span></span>   | <span data-ttu-id="45e73-419">與 D3DRS POINTSCALEENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-419">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="45e73-420">Dialog</span><span class="sxs-lookup"><span data-stu-id="45e73-420">PointSize</span></span>                | <span data-ttu-id="45e73-421">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-421">float</span></span>  | <span data-ttu-id="45e73-422">與 D3DRS dialog 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-422">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="45e73-423">Dialog \_ 分鐘</span><span class="sxs-lookup"><span data-stu-id="45e73-423">PointSize\_Min</span></span>           | <span data-ttu-id="45e73-424">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-424">float</span></span>  | <span data-ttu-id="45e73-425">與 D3DRS dialog MIN 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-425">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="45e73-426">Dialog \_ Max</span><span class="sxs-lookup"><span data-stu-id="45e73-426">PointSize\_Max</span></span>           | <span data-ttu-id="45e73-427">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-427">float</span></span>  | <span data-ttu-id="45e73-428">與 D3DRS \_ dialog MAX 相同 \_ 的值，不含 D3DRS \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e73-428">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="45e73-429">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-429">PointSpriteEnable</span></span>        | <span data-ttu-id="45e73-430">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-430">bool</span></span>   | <span data-ttu-id="45e73-431">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-431">True or False.</span></span> <span data-ttu-id="45e73-432">與 D3DRS POINTSPRITEENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-432">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="45e73-433">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-433">RangeFogEnable</span></span>           | <span data-ttu-id="45e73-434">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-434">bool</span></span>   | <span data-ttu-id="45e73-435">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-435">True or False.</span></span> <span data-ttu-id="45e73-436">與 D3DRS RANGEFOGENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-436">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="45e73-437">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="45e73-437">SpecularEnable</span></span>           | <span data-ttu-id="45e73-438">bool</span><span class="sxs-lookup"><span data-stu-id="45e73-438">bool</span></span>   | <span data-ttu-id="45e73-439">是非題。</span><span class="sxs-lookup"><span data-stu-id="45e73-439">True or False.</span></span> <span data-ttu-id="45e73-440">與 D3DRS SPECULARENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-440">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="45e73-441">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="45e73-441">SpecularMaterialSource</span></span>   | <span data-ttu-id="45e73-442">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-442">dword</span></span>  | <span data-ttu-id="45e73-443">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-443">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="45e73-444">請參閱 D3DRS \_ SPECULARMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="45e73-444">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="45e73-445">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="45e73-445">TweenFactor</span></span>              | <span data-ttu-id="45e73-446">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-446">float</span></span>  | <span data-ttu-id="45e73-447">與 D3DRS TWEENFACTOR 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-447">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="45e73-448">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="45e73-448">VertexBlend</span></span>              | <span data-ttu-id="45e73-449">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-449">dword</span></span>  | <span data-ttu-id="45e73-450">與沒有 D3DVBF 前置詞的 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-450">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="45e73-451">請參閱 D3DRS \_ VERTEXBLEND。</span><span class="sxs-lookup"><span data-stu-id="45e73-451">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="45e73-452">範例：</span><span class="sxs-lookup"><span data-stu-id="45e73-452">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="45e73-453">這會使環境色彩 float4<0.7 f、0.0 f、0.0 f、1.0 f>、將背面剔除模式設定為逆時針方向，並將 [霧化色彩] 設定為紅色。</span><span class="sxs-lookup"><span data-stu-id="45e73-453">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="45e73-454">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-454">Sampler States</span></span>

<span data-ttu-id="45e73-455">取樣器狀態代表取樣器物件。</span><span class="sxs-lookup"><span data-stu-id="45e73-455">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="45e73-456">狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-456">State</span></span>   | <span data-ttu-id="45e73-457">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-457">Type</span></span>    | <span data-ttu-id="45e73-458">值</span><span class="sxs-lookup"><span data-stu-id="45e73-458">Values</span></span>                              |
| <span data-ttu-id="45e73-459">取樣器</span><span class="sxs-lookup"><span data-stu-id="45e73-459">Sampler</span></span> | <span data-ttu-id="45e73-460">採樣</span><span class="sxs-lookup"><span data-stu-id="45e73-460">sampler</span></span> | <span data-ttu-id="45e73-461">**Null** 或取樣器狀態欄塊。</span><span class="sxs-lookup"><span data-stu-id="45e73-461">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="45e73-462">取樣器階段狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-462">Sampler Stage States</span></span>

<span data-ttu-id="45e73-463">取樣器階段狀態是用來取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="45e73-463">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="45e73-464">取樣器狀態決定篩選類型和材質定址模式。</span><span class="sxs-lookup"><span data-stu-id="45e73-464">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e73-465">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-465">Sampler State</span></span>       | <span data-ttu-id="45e73-466">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-466">Type</span></span>                         | <span data-ttu-id="45e73-467">值</span><span class="sxs-lookup"><span data-stu-id="45e73-467">Values</span></span>                                                                                                                            |
| <span data-ttu-id="45e73-468">AddressU \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-468">AddressU\[16\]</span></span>      | <span data-ttu-id="45e73-469">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-469">dword</span></span>                        | <span data-ttu-id="45e73-470">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-470">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="45e73-471">請參閱 D3DSAMP \_ ADDRESSU。</span><span class="sxs-lookup"><span data-stu-id="45e73-471">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="45e73-472">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-472">AddressV\[16\]</span></span>      | <span data-ttu-id="45e73-473">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-473">dword</span></span>                        | <span data-ttu-id="45e73-474">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="45e73-475">請參閱 D3DSAMP \_ ADDRESSV。</span><span class="sxs-lookup"><span data-stu-id="45e73-475">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="45e73-476">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-476">AddressW\[16\]</span></span>      | <span data-ttu-id="45e73-477">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-477">dword</span></span>                        | <span data-ttu-id="45e73-478">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="45e73-479">請參閱 D3DSAMP \_ ADDRESSW。</span><span class="sxs-lookup"><span data-stu-id="45e73-479">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="45e73-480">邊框 \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-480">BorderColor\[16\]</span></span>   | [<span data-ttu-id="45e73-481">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="45e73-481">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="45e73-482">與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-482">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="45e73-483">請參閱 D3DSAMP \_ 邊框出。</span><span class="sxs-lookup"><span data-stu-id="45e73-483">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="45e73-484">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-484">MagFilter\[16\]</span></span>     | <span data-ttu-id="45e73-485">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-485">dword</span></span>                        | <span data-ttu-id="45e73-486">與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="45e73-487">請參閱 D3DSAMP \_ MAGFILTER。</span><span class="sxs-lookup"><span data-stu-id="45e73-487">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="45e73-488">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-488">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="45e73-489">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-489">dword</span></span>                        | <span data-ttu-id="45e73-490">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXANISOTROPY 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-490">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="45e73-491">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-491">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="45e73-492">int</span><span class="sxs-lookup"><span data-stu-id="45e73-492">int</span></span>                          | <span data-ttu-id="45e73-493">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXMIPLEVEL 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-493">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="45e73-494">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-494">MinFilter\[16\]</span></span>     | <span data-ttu-id="45e73-495">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-495">dword</span></span>                        | <span data-ttu-id="45e73-496">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MINFILTER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-496">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="45e73-497">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-497">MipFilter\[16\]</span></span>     | <span data-ttu-id="45e73-498">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-498">dword</span></span>                        | <span data-ttu-id="45e73-499">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPFILTER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-499">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="45e73-500">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="45e73-500">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="45e73-501">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-501">float</span></span>                        | <span data-ttu-id="45e73-502">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPMAPLODBIAS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-502">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="45e73-503">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="45e73-503">SRGBTexture</span></span>         | <span data-ttu-id="45e73-504">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-504">float</span></span>                        | <span data-ttu-id="45e73-505">與 D3DSAMP SRGBTEXTURE 的值相同， \_ 不含 D3DSAMP \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e73-505">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                  |



 

<span data-ttu-id="45e73-506">範例：</span><span class="sxs-lookup"><span data-stu-id="45e73-506">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="45e73-507">這個個會 UVW 值介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="45e73-507">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="45e73-508">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-508">Shader States</span></span>

<span data-ttu-id="45e73-509">只有兩種效果著色器狀態：一個與頂點著色器物件相關聯，另一個與圖元著色器物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="45e73-509">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="45e73-510">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-510">Shader State</span></span> | <span data-ttu-id="45e73-511">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-511">Type</span></span>         | <span data-ttu-id="45e73-512">值</span><span class="sxs-lookup"><span data-stu-id="45e73-512">Values</span></span>                                                                      |
| <span data-ttu-id="45e73-513">無效</span><span class="sxs-lookup"><span data-stu-id="45e73-513">PixelShader</span></span>  | <span data-ttu-id="45e73-514">無效</span><span class="sxs-lookup"><span data-stu-id="45e73-514">pixelshader</span></span>  | <span data-ttu-id="45e73-515">**Null**、元件區塊、編譯目標或圖元著色器參數。</span><span class="sxs-lookup"><span data-stu-id="45e73-515">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="45e73-516">VertexShader</span><span class="sxs-lookup"><span data-stu-id="45e73-516">VertexShader</span></span> | <span data-ttu-id="45e73-517">vertexshader</span><span class="sxs-lookup"><span data-stu-id="45e73-517">vertexshader</span></span> | <span data-ttu-id="45e73-518">**Null**、元件區塊、編譯目標或圖元著色器參數。</span><span class="sxs-lookup"><span data-stu-id="45e73-518">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="45e73-519">範例：</span><span class="sxs-lookup"><span data-stu-id="45e73-519">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="45e73-520">這會將 VSTexture （稍早在 fx 檔案中定義的頂點著色器）編譯為頂點著色器1.1 版，然後將該編譯的著色器設定為頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="45e73-520">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="45e73-521">圖元著色器會指派給 **Null**。</span><span class="sxs-lookup"><span data-stu-id="45e73-521">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="45e73-522">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-522">Shader Constant States</span></span>

<span data-ttu-id="45e73-523">著色器常數狀態可用來存取著色器常數參數。</span><span class="sxs-lookup"><span data-stu-id="45e73-523">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="45e73-524">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-524">Shader Constant State</span></span> | <span data-ttu-id="45e73-525">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-525">Type</span></span>            | <span data-ttu-id="45e73-526">值</span><span class="sxs-lookup"><span data-stu-id="45e73-526">Values</span></span>                                       |
| <span data-ttu-id="45e73-527">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="45e73-527">PixelShaderConstant</span></span>   | <span data-ttu-id="45e73-528">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-528">float\[m\[n\]\]</span></span> | <span data-ttu-id="45e73-529">m x n 浮點數的陣列;m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-529">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="45e73-530">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="45e73-530">PixelShaderConstant1</span></span>  | <span data-ttu-id="45e73-531">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-531">float4</span></span>          | <span data-ttu-id="45e73-532">一個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-532">One 4D float.</span></span>                                |
| <span data-ttu-id="45e73-533">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="45e73-533">PixelShaderConstant2</span></span>  | <span data-ttu-id="45e73-534">float4x2</span><span class="sxs-lookup"><span data-stu-id="45e73-534">float4x2</span></span>        | <span data-ttu-id="45e73-535">兩個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-535">Two 4D floats.</span></span>                               |
| <span data-ttu-id="45e73-536">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="45e73-536">PixelShaderConstant3</span></span>  | <span data-ttu-id="45e73-537">float4x3</span><span class="sxs-lookup"><span data-stu-id="45e73-537">float4x3</span></span>        | <span data-ttu-id="45e73-538">三個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-538">Three 4D floats.</span></span>                             |
| <span data-ttu-id="45e73-539">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="45e73-539">PixelShaderConstant4</span></span>  | <span data-ttu-id="45e73-540">float4x4</span><span class="sxs-lookup"><span data-stu-id="45e73-540">float4x4</span></span>        | <span data-ttu-id="45e73-541">四個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-541">Four 4D floats.</span></span>                              |
| <span data-ttu-id="45e73-542">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="45e73-542">PixelShaderConstantB</span></span>  | <span data-ttu-id="45e73-543">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-543">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="45e73-544">m x n bool 的陣列;m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-544">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="45e73-545">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="45e73-545">PixelShaderConstantI</span></span>  | <span data-ttu-id="45e73-546">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-546">int\[m\[n\]\]</span></span>   | <span data-ttu-id="45e73-547">m x n 的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="45e73-547">m x n array of ints.</span></span> <span data-ttu-id="45e73-548">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-548">m and n are optional.</span></span>   |
| <span data-ttu-id="45e73-549">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="45e73-549">PixelShaderConstantF</span></span>  | <span data-ttu-id="45e73-550">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-550">float\[m\[n\]\]</span></span> | <span data-ttu-id="45e73-551">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="45e73-551">m x n array of floats.</span></span> <span data-ttu-id="45e73-552">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-552">m and n are optional.</span></span> |
| <span data-ttu-id="45e73-553">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="45e73-553">VertexShaderConstant</span></span>  | <span data-ttu-id="45e73-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="45e73-555">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="45e73-555">m x n array of floats.</span></span> <span data-ttu-id="45e73-556">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-556">m and n are optional.</span></span> |
| <span data-ttu-id="45e73-557">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="45e73-557">VertexShaderConstant1</span></span> | <span data-ttu-id="45e73-558">float4</span><span class="sxs-lookup"><span data-stu-id="45e73-558">float4</span></span>          | <span data-ttu-id="45e73-559">一個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-559">One 4D float.</span></span>                                |
| <span data-ttu-id="45e73-560">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="45e73-560">VertexShaderConstant2</span></span> | <span data-ttu-id="45e73-561">float4x2</span><span class="sxs-lookup"><span data-stu-id="45e73-561">float4x2</span></span>        | <span data-ttu-id="45e73-562">兩個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-562">Two 4D floats.</span></span>                               |
| <span data-ttu-id="45e73-563">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="45e73-563">VertexShaderConstant3</span></span> | <span data-ttu-id="45e73-564">float4x3</span><span class="sxs-lookup"><span data-stu-id="45e73-564">float4x3</span></span>        | <span data-ttu-id="45e73-565">三個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-565">Three 4D floats.</span></span>                             |
| <span data-ttu-id="45e73-566">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="45e73-566">VertexShaderConstant4</span></span> | <span data-ttu-id="45e73-567">float4x4</span><span class="sxs-lookup"><span data-stu-id="45e73-567">float4x4</span></span>        | <span data-ttu-id="45e73-568">四個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="45e73-568">Four 4D floats.</span></span>                              |
| <span data-ttu-id="45e73-569">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="45e73-569">VertexShaderConstantB</span></span> | <span data-ttu-id="45e73-570">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-570">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="45e73-571">m x n bool 陣列。</span><span class="sxs-lookup"><span data-stu-id="45e73-571">m x n array of bools.</span></span> <span data-ttu-id="45e73-572">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-572">m and n are optional.</span></span>  |
| <span data-ttu-id="45e73-573">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="45e73-573">VertexShaderConstantI</span></span> | <span data-ttu-id="45e73-574">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-574">int\[m\[n\]\]</span></span>   | <span data-ttu-id="45e73-575">m x n 的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="45e73-575">m x n array of ints.</span></span> <span data-ttu-id="45e73-576">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-576">m and n are optional.</span></span>   |
| <span data-ttu-id="45e73-577">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="45e73-577">VertexShaderConstantF</span></span> | <span data-ttu-id="45e73-578">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="45e73-578">float\[m\[n\]\]</span></span> | <span data-ttu-id="45e73-579">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="45e73-579">m x n array of floats.</span></span> <span data-ttu-id="45e73-580">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="45e73-580">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="45e73-581">材質狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-581">Texture States</span></span>

<span data-ttu-id="45e73-582">材質狀態會初始化多紋理 blender 所使用的材質。</span><span class="sxs-lookup"><span data-stu-id="45e73-582">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="45e73-583">材質狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-583">Texture State</span></span> | <span data-ttu-id="45e73-584">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-584">Type</span></span>    | <span data-ttu-id="45e73-585">值</span><span class="sxs-lookup"><span data-stu-id="45e73-585">Values</span></span>                            |
| <span data-ttu-id="45e73-586">材質 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-586">Texture\[8\]</span></span>  | <span data-ttu-id="45e73-587">紋理</span><span class="sxs-lookup"><span data-stu-id="45e73-587">texture</span></span> | <span data-ttu-id="45e73-588">**Null** 或紋理參數。</span><span class="sxs-lookup"><span data-stu-id="45e73-588">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="45e73-589">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-589">Texture Stage States</span></span>

<span data-ttu-id="45e73-590">材質階段狀態會設定多紋理 blender 中的材質和紋理階段。</span><span class="sxs-lookup"><span data-stu-id="45e73-590">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e73-591">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-591">Texture Stage State</span></span>        | <span data-ttu-id="45e73-592">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-592">Type</span></span>  | <span data-ttu-id="45e73-593">值</span><span class="sxs-lookup"><span data-stu-id="45e73-593">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="45e73-594">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-594">AlphaOp\[8\]</span></span>               | <span data-ttu-id="45e73-595">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-595">dword</span></span> | <span data-ttu-id="45e73-596">與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-596">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="45e73-597">請參閱 D3DTSS \_ ALPHAOP。</span><span class="sxs-lookup"><span data-stu-id="45e73-597">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="45e73-598">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-598">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="45e73-599">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-599">dword</span></span> | <span data-ttu-id="45e73-600">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-600">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-601">請參閱 D3DTSS \_ ALPHAARG0。</span><span class="sxs-lookup"><span data-stu-id="45e73-601">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="45e73-602">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-602">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="45e73-603">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-603">dword</span></span> | <span data-ttu-id="45e73-604">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-605">請參閱 D3DTSS \_ ALPHAARG1。</span><span class="sxs-lookup"><span data-stu-id="45e73-605">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="45e73-606">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-606">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="45e73-607">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-607">dword</span></span> | <span data-ttu-id="45e73-608">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-609">請參閱 D3DTSS \_ ALPHAARG2。</span><span class="sxs-lookup"><span data-stu-id="45e73-609">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="45e73-610">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-610">ColorArg0\[8\]</span></span>             | <span data-ttu-id="45e73-611">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-611">dword</span></span> | <span data-ttu-id="45e73-612">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-613">請參閱 D3DTSS \_ COLORARG0。</span><span class="sxs-lookup"><span data-stu-id="45e73-613">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="45e73-614">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-614">ColorArg1\[8\]</span></span>             | <span data-ttu-id="45e73-615">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-615">dword</span></span> | <span data-ttu-id="45e73-616">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-617">請參閱 D3DTSS \_ COLORARG1。</span><span class="sxs-lookup"><span data-stu-id="45e73-617">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="45e73-618">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-618">ColorArg2\[8\]</span></span>             | <span data-ttu-id="45e73-619">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-619">dword</span></span> | <span data-ttu-id="45e73-620">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-621">請參閱 D3DTSS \_ COLORARG2。</span><span class="sxs-lookup"><span data-stu-id="45e73-621">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="45e73-622">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-622">ColorOp\[8\]</span></span>               | <span data-ttu-id="45e73-623">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-623">dword</span></span> | <span data-ttu-id="45e73-624">與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-624">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="45e73-625">請參閱 D3DTSS \_ COLOROP。</span><span class="sxs-lookup"><span data-stu-id="45e73-625">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="45e73-626">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-626">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="45e73-627">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-627">float</span></span> | <span data-ttu-id="45e73-628">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLSCALE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-628">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="45e73-629">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-629">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="45e73-630">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-630">float</span></span> | <span data-ttu-id="45e73-631">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLOFFSET 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-631">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="45e73-632">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-632">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="45e73-633">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-633">float</span></span> | <span data-ttu-id="45e73-634">與 D3DTSS BUMPENVMAT00 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-634">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="45e73-635">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-635">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="45e73-636">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-636">float</span></span> | <span data-ttu-id="45e73-637">與 D3DTSS BUMPENVMAT01 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-637">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="45e73-638">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-638">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="45e73-639">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-639">float</span></span> | <span data-ttu-id="45e73-640">與 D3DTSS BUMPENVMAT10 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-640">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="45e73-641">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-641">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="45e73-642">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45e73-642">float</span></span> | <span data-ttu-id="45e73-643">與 D3DTSS BUMPENVMAT11 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-643">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="45e73-644">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-644">ResultArg\[8\]</span></span>             | <span data-ttu-id="45e73-645">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-645">dword</span></span> | <span data-ttu-id="45e73-646">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-646">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="45e73-647">請參閱 D3DTSS \_ RESULTARG。</span><span class="sxs-lookup"><span data-stu-id="45e73-647">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="45e73-648">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-648">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="45e73-649">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-649">dword</span></span> | <span data-ttu-id="45e73-650">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS TEXCOORDINDEX 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-650">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="45e73-651">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-651">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="45e73-652">dword</span><span class="sxs-lookup"><span data-stu-id="45e73-652">dword</span></span> | <span data-ttu-id="45e73-653">與沒有 D3DTTFF 前置詞的 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 值相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-653">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="45e73-654">請參閱 D3DTSS \_ TEXTURETRANSFORMFLAGS。</span><span class="sxs-lookup"><span data-stu-id="45e73-654">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="45e73-655">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-655">Transform States</span></span>

<span data-ttu-id="45e73-656">設定轉換狀態以初始化轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="45e73-656">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="45e73-657">效果會使用已轉置的矩陣來提高效率。</span><span class="sxs-lookup"><span data-stu-id="45e73-657">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="45e73-658">您可以將已轉換的矩陣提供給效果，或在使用矩陣之前自動變換矩陣。</span><span class="sxs-lookup"><span data-stu-id="45e73-658">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e73-659">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="45e73-659">Transform State</span></span>       | <span data-ttu-id="45e73-660">類型</span><span class="sxs-lookup"><span data-stu-id="45e73-660">Type</span></span>     | <span data-ttu-id="45e73-661">值</span><span class="sxs-lookup"><span data-stu-id="45e73-661">Values</span></span>                                                                                                                          |
| <span data-ttu-id="45e73-662">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="45e73-662">ProjectionTransform</span></span>   | <span data-ttu-id="45e73-663">float4x4</span><span class="sxs-lookup"><span data-stu-id="45e73-663">float4x4</span></span> | <span data-ttu-id="45e73-664">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="45e73-664">A 4x4 matrix of floats.</span></span> <span data-ttu-id="45e73-665">與 \_ 沒有 D3DTS 前置詞的 D3DTS 投射相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-665">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="45e73-666">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="45e73-666">TextureTransform\[8\]</span></span> | <span data-ttu-id="45e73-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="45e73-667">float4x4</span></span> | <span data-ttu-id="45e73-668">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="45e73-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="45e73-669">與沒有 D3DTS 前置詞的 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-669">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="45e73-670">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="45e73-670">ViewTransform</span></span>         | <span data-ttu-id="45e73-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="45e73-671">float4x4</span></span> | <span data-ttu-id="45e73-672">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="45e73-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="45e73-673">D3DTS \_ VIEW 與沒有 D3DTS 前置詞的值相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45e73-673">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="45e73-674">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="45e73-674">WorldTransform</span></span>        | <span data-ttu-id="45e73-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="45e73-675">float4x4</span></span> | <span data-ttu-id="45e73-676">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="45e73-676">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="45e73-677">相關主題</span><span class="sxs-lookup"><span data-stu-id="45e73-677">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e73-678">效果格式</span><span class="sxs-lookup"><span data-stu-id="45e73-678">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
