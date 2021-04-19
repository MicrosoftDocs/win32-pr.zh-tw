---
description: 效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: '效果狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314761"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="ec3db-103">效果狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="ec3db-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="ec3db-104">效果狀態是用來初始化管線狀態，以準備頂點和圖元處理。</span><span class="sxs-lookup"><span data-stu-id="ec3db-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="ec3db-105">其中：</span><span class="sxs-lookup"><span data-stu-id="ec3db-105">Where:</span></span>

-   <span data-ttu-id="ec3db-106">效果狀態-類似于傳統的固定函式管線狀態。</span><span class="sxs-lookup"><span data-stu-id="ec3db-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="ec3db-107">以下提供完整的狀態清單。</span><span class="sxs-lookup"><span data-stu-id="ec3db-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="ec3db-108">\[\[ \] 索引 \]-選擇性的整數索引。</span><span class="sxs-lookup"><span data-stu-id="ec3db-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="ec3db-109">索引會識別效果狀態陣列內的特定狀態。</span><span class="sxs-lookup"><span data-stu-id="ec3db-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="ec3db-110">外部括弧表示索引是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="ec3db-111">如果使用索引，請務必使用內部括弧。</span><span class="sxs-lookup"><span data-stu-id="ec3db-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="ec3db-112">運算式狀態指派運算式。</span><span class="sxs-lookup"><span data-stu-id="ec3db-112">expression - State assignment expression.</span></span> <span data-ttu-id="ec3db-113">請參閱 [ (Direct3D 9) 的運算式 ](expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="ec3db-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="ec3db-114">每個狀態都有原生資料類型。</span><span class="sxs-lookup"><span data-stu-id="ec3db-114">Each state has a native data type.</span></span> <span data-ttu-id="ec3db-115">這是當效果指派值時，狀態預期值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="ec3db-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="ec3db-116">以下列出每個狀態所預期的資料類型。</span><span class="sxs-lookup"><span data-stu-id="ec3db-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="ec3db-117">請注意，效果介面會盡可能儘早地將值轉換成適當的類型。</span><span class="sxs-lookup"><span data-stu-id="ec3db-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="ec3db-118">常值可以在編譯時期轉換。</span><span class="sxs-lookup"><span data-stu-id="ec3db-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="ec3db-119">非常值 (亦即，當呼叫適當的 Set 方法時，) 需要轉換的一般變數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="ec3db-120">例如，如有必要，效果介面會轉換使用 [**SetBool**](id3dxbaseeffect--setbool.md)、 [**SetValue**](id3dxbaseeffect--setvalue.md)和其他類似函式設定的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="ec3db-121">為了獲得更好的效能，請確定傳遞至效果介面的值已經是正確的類型，而且不需要轉換。</span><span class="sxs-lookup"><span data-stu-id="ec3db-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="ec3db-122">如果執行時間無法轉換值，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec3db-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="ec3db-123">效果狀態可以分成下列類別：</span><span class="sxs-lookup"><span data-stu-id="ec3db-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="ec3db-124">亮州</span><span class="sxs-lookup"><span data-stu-id="ec3db-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="ec3db-125">材質狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="ec3db-126">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="ec3db-127">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="ec3db-128">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="ec3db-129">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="ec3db-130">取樣器階段狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="ec3db-131">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="ec3db-132">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="ec3db-133">材質狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="ec3db-134">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="ec3db-135">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="ec3db-136">亮州</span><span class="sxs-lookup"><span data-stu-id="ec3db-136">Light States</span></span>

<span data-ttu-id="ec3db-137">若要啟用效果的最佳效能，應該在效果檔案中指定燈光或材質的所有元件。</span><span class="sxs-lookup"><span data-stu-id="ec3db-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="ec3db-138">您無法宣告的狀態會設定為某個預設值，因為 Direct3D 無法個別設定燈的狀態。</span><span class="sxs-lookup"><span data-stu-id="ec3db-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3db-139">亮州</span><span class="sxs-lookup"><span data-stu-id="ec3db-139">Light State</span></span>            | <span data-ttu-id="ec3db-140">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-140">Type</span></span>   | <span data-ttu-id="ec3db-141">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="ec3db-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="ec3db-143">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-143">float4</span></span> | <span data-ttu-id="ec3db-144">請參閱 [**D3DLIGHT9**](d3dlight9.md)的環境成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="ec3db-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="ec3db-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-146">float</span></span>  | <span data-ttu-id="ec3db-147">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation0 成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="ec3db-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="ec3db-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-149">float</span></span>  | <span data-ttu-id="ec3db-150">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation1 成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="ec3db-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="ec3db-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-152">float</span></span>  | <span data-ttu-id="ec3db-153">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Attenuation2 成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="ec3db-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="ec3db-155">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-155">float4</span></span> | <span data-ttu-id="ec3db-156">請參閱 [**D3DLIGHT9**](d3dlight9.md)的擴散成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="ec3db-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="ec3db-158">float3</span><span class="sxs-lookup"><span data-stu-id="ec3db-158">float3</span></span> | <span data-ttu-id="ec3db-159">請參閱 [**D3DLIGHT9**](d3dlight9.md)的方向成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="ec3db-160">LightEnable \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="ec3db-161">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-161">bool</span></span>   | <span data-ttu-id="ec3db-162">**TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ec3db-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="ec3db-163">請參閱 [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)中的 bEnable 引數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="ec3db-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="ec3db-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-165">float</span></span>  | <span data-ttu-id="ec3db-166">[**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="ec3db-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="ec3db-167">請參閱 [**D3DLIGHT9**](d3dlight9.md)的衰減成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="ec3db-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="ec3db-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-169">float</span></span>  | <span data-ttu-id="ec3db-170">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Phi 成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="ec3db-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="ec3db-172">float3</span><span class="sxs-lookup"><span data-stu-id="ec3db-172">float3</span></span> | <span data-ttu-id="ec3db-173">請參閱 [**D3DLIGHT9**](d3dlight9.md)的位置成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="ec3db-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-174">LightRange\[n\]</span></span>        | <span data-ttu-id="ec3db-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-175">float</span></span>  | <span data-ttu-id="ec3db-176">請參閱 [**D3DLIGHT9**](d3dlight9.md)的範圍成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="ec3db-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="ec3db-178">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-178">float4</span></span> | <span data-ttu-id="ec3db-179">請參閱 [**D3DLIGHT9**](d3dlight9.md)的反射成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="ec3db-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="ec3db-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-181">float</span></span>  | <span data-ttu-id="ec3db-182">請參閱 [**D3DLIGHT9**](d3dlight9.md)的 Theta 成員。</span><span class="sxs-lookup"><span data-stu-id="ec3db-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="ec3db-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-183">LightType\[n\]</span></span>         | <span data-ttu-id="ec3db-184">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-184">dword</span></span>  | <span data-ttu-id="ec3db-185">與最多 n 個 [**D3DLIGHTTYPE**](./d3dlighttype.md) 值陣列相同的值，不含 D3DLIGHT \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="ec3db-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="ec3db-186">範例：</span><span class="sxs-lookup"><span data-stu-id="ec3db-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="ec3db-187">這會啟用光源、將點光源設定為類型、將光線位置設定為 float3<10.0 f、1.0 f、23.0 f>，然後將環境色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>。</span><span class="sxs-lookup"><span data-stu-id="ec3db-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="ec3db-188">材質狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-188">Material States</span></span>

<span data-ttu-id="ec3db-189">因為 Direct3D 無法個別設定材質狀態，所以您無法宣告的狀態會設定為某些預設值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="ec3db-190">材質狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-190">Material State</span></span>   | <span data-ttu-id="ec3db-191">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-191">Type</span></span>   | <span data-ttu-id="ec3db-192">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-192">Values</span></span>                                         |
| <span data-ttu-id="ec3db-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="ec3db-193">MaterialAmbient</span></span>  | <span data-ttu-id="ec3db-194">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-194">float4</span></span> | <span data-ttu-id="ec3db-195">與環境相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="ec3db-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="ec3db-196">>materialdiffuse</span><span class="sxs-lookup"><span data-stu-id="ec3db-196">MaterialDiffuse</span></span>  | <span data-ttu-id="ec3db-197">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-197">float4</span></span> | <span data-ttu-id="ec3db-198">與漫射相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="ec3db-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="ec3db-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="ec3db-199">MaterialEmissive</span></span> | <span data-ttu-id="ec3db-200">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-200">float4</span></span> | <span data-ttu-id="ec3db-201">與放射相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="ec3db-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="ec3db-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="ec3db-202">MaterialPower</span></span>    | <span data-ttu-id="ec3db-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-203">float</span></span>  | <span data-ttu-id="ec3db-204">與電源相同的值[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="ec3db-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="ec3db-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="ec3db-205">MaterialSpecular</span></span> | <span data-ttu-id="ec3db-206">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-206">float4</span></span> | <span data-ttu-id="ec3db-207">與反射的值相同[ ](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="ec3db-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="ec3db-208">範例：</span><span class="sxs-lookup"><span data-stu-id="ec3db-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="ec3db-209">這會將擴散色彩設定為 float4<0.7 f、0.0 f、0.0 f、1.0 f>，並讓材質 3.0 f 的威力。</span><span class="sxs-lookup"><span data-stu-id="ec3db-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="ec3db-210">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-210">Render States</span></span>

<span data-ttu-id="ec3db-211">轉譯狀態有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="ec3db-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="ec3db-212">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="ec3db-213">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="ec3db-214">圖元管道呈現狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="ec3db-215">效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="ec3db-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec3db-216">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-216">Render State</span></span></td>
<td><span data-ttu-id="ec3db-217">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-217">Type</span></span></td>
<td><span data-ttu-id="ec3db-218">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="ec3db-220">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-220">bool</span></span></td>
<td><span data-ttu-id="ec3db-221">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-221">True or False.</span></span> <span data-ttu-id="ec3db-222">與 <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>中 D3DRS_ALPHABLENDENABLE 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="ec3db-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="ec3db-224">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-224">dword</span></span></td>
<td><span data-ttu-id="ec3db-225">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="ec3db-226">請參閱 D3DRS_ALPHAFUNC。</span><span class="sxs-lookup"><span data-stu-id="ec3db-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="ec3db-227">AlphaRef</span></span></td>
<td><span data-ttu-id="ec3db-228">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-228">dword</span></span></td>
<td><span data-ttu-id="ec3db-229">與 D3DRS_ALPHAREF 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="ec3db-231">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-231">dword</span></span></td>
<td><span data-ttu-id="ec3db-232">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-232">True or False.</span></span> <span data-ttu-id="ec3db-233">請參閱 D3DRS_ALPHATESTENABLE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="ec3db-234">BlendOp</span></span></td>
<td><span data-ttu-id="ec3db-235">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-235">dword</span></span></td>
<td><span data-ttu-id="ec3db-236">與沒有 D3DBLENDOP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="ec3db-238">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-238">dword</span></span></td>
<td><span data-ttu-id="ec3db-239">紅色的位元組合 |綠色 |藍色 |阿 爾 法。</span><span class="sxs-lookup"><span data-stu-id="ec3db-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="ec3db-240">請參閱 D3DRS_COLORWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="ec3db-241">DepthBias</span></span></td>
<td><span data-ttu-id="ec3db-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-242">float</span></span></td>
<td><span data-ttu-id="ec3db-243">與 D3DRS_DEPTHBIAS 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="ec3db-244">DestBlend</span></span></td>
<td><span data-ttu-id="ec3db-245">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-245">dword</span></span></td>
<td><span data-ttu-id="ec3db-246">與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-247">DitherEnable</span></span></td>
<td><span data-ttu-id="ec3db-248">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-248">bool</span></span></td>
<td><span data-ttu-id="ec3db-249">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-249">True or False.</span></span> <span data-ttu-id="ec3db-250">與 D3DRS_DITHERENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="ec3db-251">FillMode</span></span></td>
<td><span data-ttu-id="ec3db-252">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-252">dword</span></span></td>
<td><span data-ttu-id="ec3db-253">與沒有 D3DFILL_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="ec3db-254">LastPixel</span></span></td>
<td><span data-ttu-id="ec3db-255">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-255">dword</span></span></td>
<td><span data-ttu-id="ec3db-256">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-256">True or False.</span></span> <span data-ttu-id="ec3db-257">請參閱 D3DRS_LASTPIXEL。</span><span class="sxs-lookup"><span data-stu-id="ec3db-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-258">ShadeMode</span><span class="sxs-lookup"><span data-stu-id="ec3db-258">ShadeMode</span></span></td>
<td><span data-ttu-id="ec3db-259">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-259">dword</span></span></td>
<td><span data-ttu-id="ec3db-260">與沒有 D3DSHADE_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="ec3db-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="ec3db-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-262">float</span></span></td>
<td><span data-ttu-id="ec3db-263">與 D3DRS_SLOPESCALEDEPTHBIAS 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="ec3db-264">SrcBlend</span></span></td>
<td><span data-ttu-id="ec3db-265">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-265">dword</span></span></td>
<td><span data-ttu-id="ec3db-266">與沒有 D3DBLEND_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="ec3db-268">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-268">bool</span></span></td>
<td><span data-ttu-id="ec3db-269">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-269">True or False.</span></span> <span data-ttu-id="ec3db-270">與 D3DRS_SRGBWRITEENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-271">StencilEnable</span></span></td>
<td><span data-ttu-id="ec3db-272">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-272">bool</span></span></td>
<td><span data-ttu-id="ec3db-273">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-273">True or False.</span></span> <span data-ttu-id="ec3db-274">與 D3DRS_STENCILENABLE 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="ec3db-275">StencilFail</span></span></td>
<td><span data-ttu-id="ec3db-276">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-276">dword</span></span></td>
<td><span data-ttu-id="ec3db-277">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="ec3db-278">請參閱 D3DRS_STENCILFAIL。</span><span class="sxs-lookup"><span data-stu-id="ec3db-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="ec3db-279">StencilFunc</span></span></td>
<td><span data-ttu-id="ec3db-280">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-280">dword</span></span></td>
<td><span data-ttu-id="ec3db-281">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="ec3db-282">請參閱 D3DRS_STENCILFUNC。</span><span class="sxs-lookup"><span data-stu-id="ec3db-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="ec3db-283">StencilMask</span></span></td>
<td><span data-ttu-id="ec3db-284">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-284">dword</span></span></td>
<td><span data-ttu-id="ec3db-285">與 D3DRS_STENCILMASK 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="ec3db-286">StencilPass</span></span></td>
<td><span data-ttu-id="ec3db-287">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-287">dword</span></span></td>
<td><span data-ttu-id="ec3db-288">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="ec3db-289">請參閱 D3DRS_STENCILPASS。</span><span class="sxs-lookup"><span data-stu-id="ec3db-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="ec3db-290">StencilRef</span></span></td>
<td><span data-ttu-id="ec3db-291">int</span><span class="sxs-lookup"><span data-stu-id="ec3db-291">int</span></span></td>
<td><span data-ttu-id="ec3db-292">與 D3DRS_STENCILREF 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="ec3db-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="ec3db-294">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-294">dword</span></span></td>
<td><span data-ttu-id="ec3db-295">與 D3DRS_STENCILWRITEMASK 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="ec3db-296">StencilZFail</span></span></td>
<td><span data-ttu-id="ec3db-297">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-297">dword</span></span></td>
<td><span data-ttu-id="ec3db-298">與沒有 D3DSTENCILCAP_ 前置詞的 <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="ec3db-299">請參閱 D3DRS_STENCILZFAIL。</span><span class="sxs-lookup"><span data-stu-id="ec3db-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="ec3db-300">TextureFactor</span></span></td>
<td><span data-ttu-id="ec3db-301">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-301">dword</span></span></td>
<td><span data-ttu-id="ec3db-302">與 <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="ec3db-303">與 D3DRS_TEXTUREFACTOR 的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="ec3db-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="ec3db-305">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-305">dword</span></span></td>
<td><span data-ttu-id="ec3db-306">值與 D3DRS_WRAP0 所使用的值相同。</span><span class="sxs-lookup"><span data-stu-id="ec3db-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="ec3db-307">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ec3db-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="ec3db-308">對應至 D3DWRAPCOORD_0 的 COORD0 () </span><span class="sxs-lookup"><span data-stu-id="ec3db-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="ec3db-309">對應至 D3DWRAPCOORD_1 的 COORD1 () </span><span class="sxs-lookup"><span data-stu-id="ec3db-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="ec3db-310">對應至 D3DWRAPCOORD_2 的 COORD2 () </span><span class="sxs-lookup"><span data-stu-id="ec3db-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="ec3db-311">對應至 D3DWRAPCOORD_3 的 COORD3 () </span><span class="sxs-lookup"><span data-stu-id="ec3db-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="ec3db-312">U (對應至 D3DWRAP_U) </span><span class="sxs-lookup"><span data-stu-id="ec3db-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="ec3db-313">對應至 D3DWRAP_V 的 V () </span><span class="sxs-lookup"><span data-stu-id="ec3db-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="ec3db-314">對應至 D3DWRAP_W 的 W () </span><span class="sxs-lookup"><span data-stu-id="ec3db-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-315">ZEnable</span></span></td>
<td><span data-ttu-id="ec3db-316">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-316">dword</span></span></td>
<td><span data-ttu-id="ec3db-317">與沒有 D3DZB_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec3db-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="ec3db-318">ZFunc</span></span></td>
<td><span data-ttu-id="ec3db-319">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-319">dword</span></span></td>
<td><span data-ttu-id="ec3db-320">與沒有 D3DCMP_ 前置詞的 <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="ec3db-321">請參閱 D3DRS_ZFUNC。</span><span class="sxs-lookup"><span data-stu-id="ec3db-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec3db-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="ec3db-323">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-323">bool</span></span></td>
<td><span data-ttu-id="ec3db-324">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-324">True or False.</span></span> <span data-ttu-id="ec3db-325">請參閱 D3DRS_ZWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ec3db-326">範例：</span><span class="sxs-lookup"><span data-stu-id="ec3db-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="ec3db-327">這會啟用 Alpha 混色，並讓所有幾何以線框呈現。</span><span class="sxs-lookup"><span data-stu-id="ec3db-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="ec3db-328">頂點管線呈現狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="ec3db-329">效果檔案轉譯狀態的名稱類似于固定函式管線狀態，通常會移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="ec3db-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3db-330">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-330">Render State</span></span>             | <span data-ttu-id="ec3db-331">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-331">Type</span></span>   | <span data-ttu-id="ec3db-332">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-332">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="ec3db-333">環境</span><span class="sxs-lookup"><span data-stu-id="ec3db-333">Ambient</span></span>                  | <span data-ttu-id="ec3db-334">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-334">float4</span></span> | <span data-ttu-id="ec3db-335">與 D3DRS 環境相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="ec3db-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="ec3db-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="ec3db-337">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-337">dword</span></span>  | <span data-ttu-id="ec3db-338">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="ec3db-339">請參閱 D3DRS \_ AMBIENTMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="ec3db-340">裁剪</span><span class="sxs-lookup"><span data-stu-id="ec3db-340">Clipping</span></span>                 | <span data-ttu-id="ec3db-341">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-341">bool</span></span>   | <span data-ttu-id="ec3db-342">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-342">True or False.</span></span> <span data-ttu-id="ec3db-343">與 D3DRS 裁剪相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="ec3db-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="ec3db-345">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-345">dword</span></span>  | <span data-ttu-id="ec3db-346">D3DCLIPPLANE0-D3DCLIPPLANE5 宏的位元組合。</span><span class="sxs-lookup"><span data-stu-id="ec3db-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="ec3db-347">請參閱 [**D3DCLIPPLANEn**](d3dclipplanen.md) 和 D3DRS \_ CLIPPLANEENABLE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="ec3db-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="ec3db-348">ColorVertex</span></span>              | <span data-ttu-id="ec3db-349">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-349">bool</span></span>   | <span data-ttu-id="ec3db-350">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-350">True or False.</span></span> <span data-ttu-id="ec3db-351">與 D3DRS COLORVERTEX 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="ec3db-352">CullMode</span><span class="sxs-lookup"><span data-stu-id="ec3db-352">CullMode</span></span>                 | <span data-ttu-id="ec3db-353">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-353">dword</span></span>  | <span data-ttu-id="ec3db-354">與沒有 D3DCULL 前置詞的 [**D3DCULL**](./d3dcull.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="ec3db-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="ec3db-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="ec3db-356">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-356">dword</span></span>  | <span data-ttu-id="ec3db-357">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="ec3db-358">請參閱 D3DRS \_ DIFFUSEMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="ec3db-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="ec3db-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="ec3db-360">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-360">dword</span></span>  | <span data-ttu-id="ec3db-361">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="ec3db-362">請參閱 D3DRS \_ EMISSIVEMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="ec3db-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="ec3db-363">FogColor</span></span>                 | <span data-ttu-id="ec3db-364">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-364">dword</span></span>  | <span data-ttu-id="ec3db-365">與 [**D3DCOLOR**](d3dcolor.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="ec3db-366">請參閱 D3DRS \_ FOGCOLOR。</span><span class="sxs-lookup"><span data-stu-id="ec3db-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="ec3db-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="ec3db-367">FogDensity</span></span>               | <span data-ttu-id="ec3db-368">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-368">float</span></span>  | <span data-ttu-id="ec3db-369">與 D3DRS FOGDENSITY 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="ec3db-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-370">FogEnable</span></span>                | <span data-ttu-id="ec3db-371">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-371">bool</span></span>   | <span data-ttu-id="ec3db-372">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-372">True or False.</span></span> <span data-ttu-id="ec3db-373">與 D3DRS FOGENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="ec3db-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="ec3db-374">FogEnd</span></span>                   | <span data-ttu-id="ec3db-375">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-375">float</span></span>  | <span data-ttu-id="ec3db-376">與 D3DRS FOGEND 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="ec3db-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="ec3db-377">FogStart</span></span>                 | <span data-ttu-id="ec3db-378">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-378">float</span></span>  | <span data-ttu-id="ec3db-379">與 D3DRS FOGSTART 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="ec3db-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="ec3db-380">FogTableMode</span></span>             | <span data-ttu-id="ec3db-381">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-381">dword</span></span>  | <span data-ttu-id="ec3db-382">與 [**D3DFOGMODE**](./d3dfogmode.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="ec3db-383">請參閱 \_ [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)中的 D3DRS FOGTABLEMODE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="ec3db-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="ec3db-384">FogVertexMode</span></span>            | <span data-ttu-id="ec3db-385">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-385">dword</span></span>  | <span data-ttu-id="ec3db-386">與沒有 D3DFOG 前置詞的 [**D3DFOGMODE**](./d3dfogmode.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="ec3db-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="ec3db-388">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-388">bool</span></span>   | <span data-ttu-id="ec3db-389">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-389">True or False.</span></span> <span data-ttu-id="ec3db-390">與 D3DRS INDEXEDVERTEXBLENDENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="ec3db-391">光源</span><span class="sxs-lookup"><span data-stu-id="ec3db-391">Lighting</span></span>                 | <span data-ttu-id="ec3db-392">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-392">bool</span></span>   | <span data-ttu-id="ec3db-393">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-393">True or False.</span></span> <span data-ttu-id="ec3db-394">與 D3DRS 光源相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="ec3db-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="ec3db-395">LocalViewer</span></span>              | <span data-ttu-id="ec3db-396">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-396">bool</span></span>   | <span data-ttu-id="ec3db-397">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-397">True or False.</span></span> <span data-ttu-id="ec3db-398">與 D3DRS LOCALVIEWER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="ec3db-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="ec3db-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="ec3db-400">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-400">bool</span></span>   | <span data-ttu-id="ec3db-401">與 D3DRS MULTISAMPLEANTIALIAS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="ec3db-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="ec3db-402">MultiSampleMask</span></span>          | <span data-ttu-id="ec3db-403">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-403">dword</span></span>  | <span data-ttu-id="ec3db-404">與 D3DRS MULTISAMPLEMASK 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="ec3db-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="ec3db-405">NormalizeNormals</span></span>         | <span data-ttu-id="ec3db-406">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-406">bool</span></span>   | <span data-ttu-id="ec3db-407">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-407">True or False.</span></span> <span data-ttu-id="ec3db-408">與 D3DRS NORMALIZENORMALS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="ec3db-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="ec3db-409">PatchSegments</span></span>            | <span data-ttu-id="ec3db-410">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-410">float</span></span>  | <span data-ttu-id="ec3db-411">與 [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)中的 nSegments 相同的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="ec3db-412">PointScale \_</span><span class="sxs-lookup"><span data-stu-id="ec3db-412">PointScale\_A</span></span>            | <span data-ttu-id="ec3db-413">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-413">float</span></span>  | <span data-ttu-id="ec3db-414">與 D3DRS \_ POINTSCALE A 相同 \_ 的值。</span><span class="sxs-lookup"><span data-stu-id="ec3db-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="ec3db-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="ec3db-415">PointScale\_B</span></span>            | <span data-ttu-id="ec3db-416">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-416">float</span></span>  | <span data-ttu-id="ec3db-417">與 D3DRS POINTSCALE B 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="ec3db-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="ec3db-418">PointScale\_C</span></span>            | <span data-ttu-id="ec3db-419">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-419">float</span></span>  | <span data-ttu-id="ec3db-420">與 D3DRS POINTSCALE C 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="ec3db-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-421">PointScaleEnable</span></span>         | <span data-ttu-id="ec3db-422">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-422">bool</span></span>   | <span data-ttu-id="ec3db-423">與 D3DRS POINTSCALEENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="ec3db-424">Dialog</span><span class="sxs-lookup"><span data-stu-id="ec3db-424">PointSize</span></span>                | <span data-ttu-id="ec3db-425">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-425">float</span></span>  | <span data-ttu-id="ec3db-426">與 D3DRS dialog 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="ec3db-427">Dialog \_ 分鐘</span><span class="sxs-lookup"><span data-stu-id="ec3db-427">PointSize\_Min</span></span>           | <span data-ttu-id="ec3db-428">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-428">float</span></span>  | <span data-ttu-id="ec3db-429">與 D3DRS dialog MIN 相同的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="ec3db-430">Dialog \_ Max</span><span class="sxs-lookup"><span data-stu-id="ec3db-430">PointSize\_Max</span></span>           | <span data-ttu-id="ec3db-431">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-431">float</span></span>  | <span data-ttu-id="ec3db-432">與 D3DRS \_ dialog MAX 相同 \_ 的值，不含 D3DRS \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="ec3db-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="ec3db-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-433">PointSpriteEnable</span></span>        | <span data-ttu-id="ec3db-434">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-434">bool</span></span>   | <span data-ttu-id="ec3db-435">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-435">True or False.</span></span> <span data-ttu-id="ec3db-436">與 D3DRS POINTSPRITEENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="ec3db-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-437">RangeFogEnable</span></span>           | <span data-ttu-id="ec3db-438">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-438">bool</span></span>   | <span data-ttu-id="ec3db-439">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-439">True or False.</span></span> <span data-ttu-id="ec3db-440">與 D3DRS RANGEFOGENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="ec3db-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="ec3db-441">SpecularEnable</span></span>           | <span data-ttu-id="ec3db-442">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-442">bool</span></span>   | <span data-ttu-id="ec3db-443">是非題。</span><span class="sxs-lookup"><span data-stu-id="ec3db-443">True or False.</span></span> <span data-ttu-id="ec3db-444">與 D3DRS SPECULARENABLE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="ec3db-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="ec3db-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="ec3db-446">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-446">dword</span></span>  | <span data-ttu-id="ec3db-447">與沒有 D3DMCS 前置詞的 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="ec3db-448">請參閱 D3DRS \_ SPECULARMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="ec3db-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="ec3db-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="ec3db-449">TweenFactor</span></span>              | <span data-ttu-id="ec3db-450">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-450">float</span></span>  | <span data-ttu-id="ec3db-451">與 D3DRS TWEENFACTOR 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="ec3db-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="ec3db-452">VertexBlend</span></span>              | <span data-ttu-id="ec3db-453">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-453">dword</span></span>  | <span data-ttu-id="ec3db-454">與沒有 D3DVBF 前置詞的 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="ec3db-455">請參閱 D3DRS \_ VERTEXBLEND。</span><span class="sxs-lookup"><span data-stu-id="ec3db-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="ec3db-456">範例：</span><span class="sxs-lookup"><span data-stu-id="ec3db-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="ec3db-457">這會使環境色彩 float4<0.7 f、0.0 f、0.0 f、1.0 f>、將背面剔除模式設定為逆時針方向，並將 [霧化色彩] 設定為紅色。</span><span class="sxs-lookup"><span data-stu-id="ec3db-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="ec3db-458">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-458">Sampler States</span></span>

<span data-ttu-id="ec3db-459">取樣器狀態代表取樣器物件。</span><span class="sxs-lookup"><span data-stu-id="ec3db-459">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="ec3db-460">狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-460">State</span></span>   | <span data-ttu-id="ec3db-461">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-461">Type</span></span>    | <span data-ttu-id="ec3db-462">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-462">Values</span></span>                              |
| <span data-ttu-id="ec3db-463">取樣器</span><span class="sxs-lookup"><span data-stu-id="ec3db-463">Sampler</span></span> | <span data-ttu-id="ec3db-464">採樣</span><span class="sxs-lookup"><span data-stu-id="ec3db-464">sampler</span></span> | <span data-ttu-id="ec3db-465">**Null** 或取樣器狀態欄塊。</span><span class="sxs-lookup"><span data-stu-id="ec3db-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="ec3db-466">取樣器階段狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-466">Sampler Stage States</span></span>

<span data-ttu-id="ec3db-467">取樣器階段狀態是用來取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="ec3db-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="ec3db-468">取樣器狀態決定篩選類型和材質定址模式。</span><span class="sxs-lookup"><span data-stu-id="ec3db-468">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3db-469">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-469">Sampler State</span></span>       | <span data-ttu-id="ec3db-470">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-470">Type</span></span>                         | <span data-ttu-id="ec3db-471">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-471">Values</span></span>                                                                                                                            |
| <span data-ttu-id="ec3db-472">AddressU \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-472">AddressU\[16\]</span></span>      | <span data-ttu-id="ec3db-473">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-473">dword</span></span>                        | <span data-ttu-id="ec3db-474">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="ec3db-475">請參閱 D3DSAMP \_ ADDRESSU。</span><span class="sxs-lookup"><span data-stu-id="ec3db-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="ec3db-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-476">AddressV\[16\]</span></span>      | <span data-ttu-id="ec3db-477">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-477">dword</span></span>                        | <span data-ttu-id="ec3db-478">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="ec3db-479">請參閱 D3DSAMP \_ ADDRESSV。</span><span class="sxs-lookup"><span data-stu-id="ec3db-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="ec3db-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-480">AddressW\[16\]</span></span>      | <span data-ttu-id="ec3db-481">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-481">dword</span></span>                        | <span data-ttu-id="ec3db-482">與沒有 D3DTADDRESS 前置詞的 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="ec3db-483">請參閱 D3DSAMP \_ ADDRESSW。</span><span class="sxs-lookup"><span data-stu-id="ec3db-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="ec3db-484">邊框 \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="ec3db-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="ec3db-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="ec3db-486">與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="ec3db-487">請參閱 D3DSAMP \_ 邊框出。</span><span class="sxs-lookup"><span data-stu-id="ec3db-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="ec3db-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="ec3db-489">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-489">dword</span></span>                        | <span data-ttu-id="ec3db-490">與沒有 D3DTEXF 前置詞的 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="ec3db-491">請參閱 D3DSAMP \_ MAGFILTER。</span><span class="sxs-lookup"><span data-stu-id="ec3db-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="ec3db-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="ec3db-493">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-493">dword</span></span>                        | <span data-ttu-id="ec3db-494">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXANISOTROPY 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="ec3db-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="ec3db-496">int</span><span class="sxs-lookup"><span data-stu-id="ec3db-496">int</span></span>                          | <span data-ttu-id="ec3db-497">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MAXMIPLEVEL 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="ec3db-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="ec3db-499">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-499">dword</span></span>                        | <span data-ttu-id="ec3db-500">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MINFILTER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="ec3db-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="ec3db-502">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-502">dword</span></span>                        | <span data-ttu-id="ec3db-503">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPFILTER 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="ec3db-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="ec3db-505">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-505">float</span></span>                        | <span data-ttu-id="ec3db-506">與 \_ 沒有 D3DSAMP 前置詞的 D3DSAMP MIPMAPLODBIAS 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="ec3db-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="ec3db-507">SRGBTexture</span></span>         | <span data-ttu-id="ec3db-508">bool</span><span class="sxs-lookup"><span data-stu-id="ec3db-508">bool</span></span>                         | <span data-ttu-id="ec3db-509">與 D3DSAMP SRGBTEXTURE 的值相同， \_ 不含 D3DSAMP \_ 前置詞。</span><span class="sxs-lookup"><span data-stu-id="ec3db-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="ec3db-510">範例：</span><span class="sxs-lookup"><span data-stu-id="ec3db-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="ec3db-511">這個個會 UVW 值介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="ec3db-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="ec3db-512">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-512">Shader States</span></span>

<span data-ttu-id="ec3db-513">只有兩種效果著色器狀態：一個與頂點著色器物件相關聯，另一個與圖元著色器物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="ec3db-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="ec3db-514">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-514">Shader State</span></span> | <span data-ttu-id="ec3db-515">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-515">Type</span></span>         | <span data-ttu-id="ec3db-516">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-516">Values</span></span>                                                                      |
| <span data-ttu-id="ec3db-517">無效</span><span class="sxs-lookup"><span data-stu-id="ec3db-517">PixelShader</span></span>  | <span data-ttu-id="ec3db-518">無效</span><span class="sxs-lookup"><span data-stu-id="ec3db-518">pixelshader</span></span>  | <span data-ttu-id="ec3db-519">**Null**、元件區塊、編譯目標或圖元著色器參數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="ec3db-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="ec3db-520">VertexShader</span></span> | <span data-ttu-id="ec3db-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="ec3db-521">vertexshader</span></span> | <span data-ttu-id="ec3db-522">**Null**、元件區塊、編譯目標或圖元著色器參數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="ec3db-523">範例：</span><span class="sxs-lookup"><span data-stu-id="ec3db-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="ec3db-524">這會將 VSTexture （稍早在 fx 檔案中定義的頂點著色器）編譯為頂點著色器1.1 版，然後將該編譯的著色器設定為頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="ec3db-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="ec3db-525">圖元著色器會指派給 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec3db-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="ec3db-526">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-526">Shader Constant States</span></span>

<span data-ttu-id="ec3db-527">著色器常數狀態可用來存取著色器常數參數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-527">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="ec3db-528">著色器常數狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-528">Shader Constant State</span></span> | <span data-ttu-id="ec3db-529">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-529">Type</span></span>            | <span data-ttu-id="ec3db-530">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-530">Values</span></span>                                       |
| <span data-ttu-id="ec3db-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="ec3db-531">PixelShaderConstant</span></span>   | <span data-ttu-id="ec3db-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="ec3db-533">m x n 浮點數的陣列;m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="ec3db-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="ec3db-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="ec3db-535">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-535">float4</span></span>          | <span data-ttu-id="ec3db-536">一個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-536">One 4D float.</span></span>                                |
| <span data-ttu-id="ec3db-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="ec3db-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="ec3db-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="ec3db-538">float4x2</span></span>        | <span data-ttu-id="ec3db-539">兩個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="ec3db-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="ec3db-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="ec3db-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="ec3db-541">float4x3</span></span>        | <span data-ttu-id="ec3db-542">三個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="ec3db-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="ec3db-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="ec3db-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="ec3db-544">float4x4</span></span>        | <span data-ttu-id="ec3db-545">四個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="ec3db-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="ec3db-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="ec3db-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="ec3db-548">m x n bool 的陣列;m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="ec3db-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="ec3db-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="ec3db-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="ec3db-551">m x n 的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="ec3db-551">m x n array of ints.</span></span> <span data-ttu-id="ec3db-552">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-552">m and n are optional.</span></span>   |
| <span data-ttu-id="ec3db-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="ec3db-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="ec3db-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="ec3db-555">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="ec3db-555">m x n array of floats.</span></span> <span data-ttu-id="ec3db-556">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-556">m and n are optional.</span></span> |
| <span data-ttu-id="ec3db-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="ec3db-557">VertexShaderConstant</span></span>  | <span data-ttu-id="ec3db-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="ec3db-559">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="ec3db-559">m x n array of floats.</span></span> <span data-ttu-id="ec3db-560">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-560">m and n are optional.</span></span> |
| <span data-ttu-id="ec3db-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="ec3db-561">VertexShaderConstant1</span></span> | <span data-ttu-id="ec3db-562">float4</span><span class="sxs-lookup"><span data-stu-id="ec3db-562">float4</span></span>          | <span data-ttu-id="ec3db-563">一個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-563">One 4D float.</span></span>                                |
| <span data-ttu-id="ec3db-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="ec3db-564">VertexShaderConstant2</span></span> | <span data-ttu-id="ec3db-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="ec3db-565">float4x2</span></span>        | <span data-ttu-id="ec3db-566">兩個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="ec3db-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="ec3db-567">VertexShaderConstant3</span></span> | <span data-ttu-id="ec3db-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="ec3db-568">float4x3</span></span>        | <span data-ttu-id="ec3db-569">三個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="ec3db-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="ec3db-570">VertexShaderConstant4</span></span> | <span data-ttu-id="ec3db-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="ec3db-571">float4x4</span></span>        | <span data-ttu-id="ec3db-572">四個4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="ec3db-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="ec3db-573">VertexShaderConstantB</span></span> | <span data-ttu-id="ec3db-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="ec3db-575">m x n bool 陣列。</span><span class="sxs-lookup"><span data-stu-id="ec3db-575">m x n array of bools.</span></span> <span data-ttu-id="ec3db-576">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-576">m and n are optional.</span></span>  |
| <span data-ttu-id="ec3db-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="ec3db-577">VertexShaderConstantI</span></span> | <span data-ttu-id="ec3db-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="ec3db-579">m x n 的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="ec3db-579">m x n array of ints.</span></span> <span data-ttu-id="ec3db-580">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-580">m and n are optional.</span></span>   |
| <span data-ttu-id="ec3db-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="ec3db-581">VertexShaderConstantF</span></span> | <span data-ttu-id="ec3db-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="ec3db-583">m x n 浮點數陣列。</span><span class="sxs-lookup"><span data-stu-id="ec3db-583">m x n array of floats.</span></span> <span data-ttu-id="ec3db-584">m 和 n 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ec3db-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="ec3db-585">材質狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-585">Texture States</span></span>

<span data-ttu-id="ec3db-586">材質狀態會初始化多紋理 blender 所使用的材質。</span><span class="sxs-lookup"><span data-stu-id="ec3db-586">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="ec3db-587">材質狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-587">Texture State</span></span> | <span data-ttu-id="ec3db-588">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-588">Type</span></span>    | <span data-ttu-id="ec3db-589">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-589">Values</span></span>                            |
| <span data-ttu-id="ec3db-590">材質 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-590">Texture\[8\]</span></span>  | <span data-ttu-id="ec3db-591">紋理</span><span class="sxs-lookup"><span data-stu-id="ec3db-591">texture</span></span> | <span data-ttu-id="ec3db-592">**Null** 或紋理參數。</span><span class="sxs-lookup"><span data-stu-id="ec3db-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="ec3db-593">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-593">Texture Stage States</span></span>

<span data-ttu-id="ec3db-594">材質階段狀態會設定多紋理 blender 中的材質和紋理階段。</span><span class="sxs-lookup"><span data-stu-id="ec3db-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3db-595">材質階段狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-595">Texture Stage State</span></span>        | <span data-ttu-id="ec3db-596">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-596">Type</span></span>  | <span data-ttu-id="ec3db-597">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-597">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="ec3db-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="ec3db-599">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-599">dword</span></span> | <span data-ttu-id="ec3db-600">與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="ec3db-601">請參閱 D3DTSS \_ ALPHAOP。</span><span class="sxs-lookup"><span data-stu-id="ec3db-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="ec3db-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="ec3db-603">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-603">dword</span></span> | <span data-ttu-id="ec3db-604">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-605">請參閱 D3DTSS \_ ALPHAARG0。</span><span class="sxs-lookup"><span data-stu-id="ec3db-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="ec3db-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="ec3db-607">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-607">dword</span></span> | <span data-ttu-id="ec3db-608">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-609">請參閱 D3DTSS \_ ALPHAARG1。</span><span class="sxs-lookup"><span data-stu-id="ec3db-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="ec3db-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="ec3db-611">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-611">dword</span></span> | <span data-ttu-id="ec3db-612">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-613">請參閱 D3DTSS \_ ALPHAARG2。</span><span class="sxs-lookup"><span data-stu-id="ec3db-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="ec3db-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="ec3db-615">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-615">dword</span></span> | <span data-ttu-id="ec3db-616">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-617">請參閱 D3DTSS \_ COLORARG0。</span><span class="sxs-lookup"><span data-stu-id="ec3db-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="ec3db-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="ec3db-619">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-619">dword</span></span> | <span data-ttu-id="ec3db-620">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-621">請參閱 D3DTSS \_ COLORARG1。</span><span class="sxs-lookup"><span data-stu-id="ec3db-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="ec3db-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="ec3db-623">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-623">dword</span></span> | <span data-ttu-id="ec3db-624">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-625">請參閱 D3DTSS \_ COLORARG2。</span><span class="sxs-lookup"><span data-stu-id="ec3db-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="ec3db-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="ec3db-627">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-627">dword</span></span> | <span data-ttu-id="ec3db-628">與沒有 D3DTOP 前置詞的 [**D3DTEXTUREOP**](./d3dtextureop.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="ec3db-629">請參閱 D3DTSS \_ COLOROP。</span><span class="sxs-lookup"><span data-stu-id="ec3db-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="ec3db-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="ec3db-631">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-631">float</span></span> | <span data-ttu-id="ec3db-632">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLSCALE 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="ec3db-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="ec3db-634">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-634">float</span></span> | <span data-ttu-id="ec3db-635">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS BUMPENVLOFFSET 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="ec3db-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="ec3db-637">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-637">float</span></span> | <span data-ttu-id="ec3db-638">與 D3DTSS BUMPENVMAT00 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="ec3db-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="ec3db-640">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-640">float</span></span> | <span data-ttu-id="ec3db-641">與 D3DTSS BUMPENVMAT01 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="ec3db-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="ec3db-643">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-643">float</span></span> | <span data-ttu-id="ec3db-644">與 D3DTSS BUMPENVMAT10 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="ec3db-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="ec3db-646">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec3db-646">float</span></span> | <span data-ttu-id="ec3db-647">與 D3DTSS BUMPENVMAT11 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="ec3db-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="ec3db-649">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-649">dword</span></span> | <span data-ttu-id="ec3db-650">與沒有 D3DTA 前置詞的 [D3DTA](d3dta.md) 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="ec3db-651">請參閱 D3DTSS \_ RESULTARG。</span><span class="sxs-lookup"><span data-stu-id="ec3db-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="ec3db-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="ec3db-653">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-653">dword</span></span> | <span data-ttu-id="ec3db-654">與 \_ 沒有 D3DTSS TCI 前置詞的 D3DTSS TEXCOORDINDEX 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="ec3db-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="ec3db-656">dword</span><span class="sxs-lookup"><span data-stu-id="ec3db-656">dword</span></span> | <span data-ttu-id="ec3db-657">與沒有 D3DTTFF 前置詞的 [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) 值相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="ec3db-658">請參閱 D3DTSS \_ TEXTURETRANSFORMFLAGS。</span><span class="sxs-lookup"><span data-stu-id="ec3db-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="ec3db-659">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-659">Transform States</span></span>

<span data-ttu-id="ec3db-660">設定轉換狀態以初始化轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec3db-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="ec3db-661">效果會使用已轉置的矩陣來提高效率。</span><span class="sxs-lookup"><span data-stu-id="ec3db-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="ec3db-662">您可以將已轉換的矩陣提供給效果，或在使用矩陣之前自動變換矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec3db-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3db-663">轉換狀態</span><span class="sxs-lookup"><span data-stu-id="ec3db-663">Transform State</span></span>       | <span data-ttu-id="ec3db-664">類型</span><span class="sxs-lookup"><span data-stu-id="ec3db-664">Type</span></span>     | <span data-ttu-id="ec3db-665">值</span><span class="sxs-lookup"><span data-stu-id="ec3db-665">Values</span></span>                                                                                                                          |
| <span data-ttu-id="ec3db-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="ec3db-666">ProjectionTransform</span></span>   | <span data-ttu-id="ec3db-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="ec3db-667">float4x4</span></span> | <span data-ttu-id="ec3db-668">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec3db-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="ec3db-669">與 \_ 沒有 D3DTS 前置詞的 D3DTS 投射相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="ec3db-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="ec3db-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="ec3db-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="ec3db-671">float4x4</span></span> | <span data-ttu-id="ec3db-672">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec3db-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="ec3db-673">與沒有 D3DTS 前置詞的 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 相同的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="ec3db-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="ec3db-674">ViewTransform</span></span>         | <span data-ttu-id="ec3db-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="ec3db-675">float4x4</span></span> | <span data-ttu-id="ec3db-676">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec3db-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="ec3db-677">D3DTS \_ VIEW 與沒有 D3DTS 前置詞的值相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec3db-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="ec3db-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="ec3db-678">WorldTransform</span></span>        | <span data-ttu-id="ec3db-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="ec3db-679">float4x4</span></span> | <span data-ttu-id="ec3db-680">浮點數的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec3db-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="ec3db-681">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec3db-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec3db-682">效果格式</span><span class="sxs-lookup"><span data-stu-id="ec3db-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
