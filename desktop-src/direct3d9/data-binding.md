---
description: 您可以使用 SasHostParameterValue 集合來定義主應用程式值的集合，以及其類型和成員，而這些值會公開給效果。
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: 資料繫結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317592"
---
# <a name="data-binding"></a><span data-ttu-id="bc580-103">資料繫結</span><span class="sxs-lookup"><span data-stu-id="bc580-103">Data Binding</span></span>

<span data-ttu-id="bc580-104">您可以使用 [SasHostParameterValue 集合](#sashostparametervalue-collection) 來定義主應用程式值的集合，以及其類型和成員，而這些值會公開給效果。</span><span class="sxs-lookup"><span data-stu-id="bc580-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="bc580-105">使用效果檔案中的 [SasBindAddress](#sasbindaddress) 注釋，將效果參數與其在主應用程式中對應的參數產生關聯。</span><span class="sxs-lookup"><span data-stu-id="bc580-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="bc580-106">SasHostParameterValue 集合</span><span class="sxs-lookup"><span data-stu-id="bc580-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="bc580-107">SasHostParameterValue 是使用效果檔案 () 語法來定義。</span><span class="sxs-lookup"><span data-stu-id="bc580-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="bc580-108">語法與效果檔案語法非常類似，但有一些差異。</span><span class="sxs-lookup"><span data-stu-id="bc580-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="bc580-109">例如，物件類型（例如 texture2d、取樣器和字串）在實際效果檔案中是不正確，但在 SasHostParameterValue 中是有效的。</span><span class="sxs-lookup"><span data-stu-id="bc580-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="bc580-110">主機應用程式可以使用任何方式來執行 SasHostParameterValue，只要它符合以下的描述即可：實際的定義位於 DXSAS 標準效果中，包括 file (\[ SDK Root \] /Utilities/Source/Sas/Sas.fxh) 。</span><span class="sxs-lookup"><span data-stu-id="bc580-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="bc580-111">請注意，SasHostParameterValue 中的陣列（例如燈光或攝影機）的長度不限。</span><span class="sxs-lookup"><span data-stu-id="bc580-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="bc580-112">這表示效果可以系結至這些陣列中的任何任意索引，而主應用程式必須在無法提供任何應用程式值的情況下，提供有意義的預設值。</span><span class="sxs-lookup"><span data-stu-id="bc580-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="bc580-113">某些類型和常數必須在 DXSAS 標準包含中定義，如標準包含的定義中所述。</span><span class="sxs-lookup"><span data-stu-id="bc580-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="bc580-114">這可讓您輕鬆地將 SasHostParameterValue 的匯總值系結至結構化效果參數。</span><span class="sxs-lookup"><span data-stu-id="bc580-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="bc580-115">SasHostParameterValue 集合</span><span class="sxs-lookup"><span data-stu-id="bc580-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="bc580-116">類型</span><span class="sxs-lookup"><span data-stu-id="bc580-116">Type</span></span>            | <span data-ttu-id="bc580-117">成員</span><span class="sxs-lookup"><span data-stu-id="bc580-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="bc580-118">Time</span><span class="sxs-lookup"><span data-stu-id="bc580-118">Time</span></span>](#time)                       | <span data-ttu-id="bc580-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc580-119">float</span></span>           | <span data-ttu-id="bc580-120">目前的 Sas。</span><span class="sxs-lookup"><span data-stu-id="bc580-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="bc580-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc580-121">float</span></span>           | <span data-ttu-id="bc580-122">Sas。上次時間</span><span class="sxs-lookup"><span data-stu-id="bc580-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="bc580-123">int</span><span class="sxs-lookup"><span data-stu-id="bc580-123">int</span></span>             | <span data-ttu-id="bc580-124">FrameNumber</span><span class="sxs-lookup"><span data-stu-id="bc580-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="bc580-125">環境對應</span><span class="sxs-lookup"><span data-stu-id="bc580-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="bc580-126">textureCUBE</span><span class="sxs-lookup"><span data-stu-id="bc580-126">textureCUBE</span></span>     | <span data-ttu-id="bc580-127">Sas. EnvironmentMap</span><span class="sxs-lookup"><span data-stu-id="bc580-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="bc580-128">相機</span><span class="sxs-lookup"><span data-stu-id="bc580-128">Camera</span></span>](#camera)                   | <span data-ttu-id="bc580-129">SasCamera</span><span class="sxs-lookup"><span data-stu-id="bc580-129">SasCamera</span></span>       | <span data-ttu-id="bc580-130">Sas 攝影機</span><span class="sxs-lookup"><span data-stu-id="bc580-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="bc580-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc580-131">float4x4</span></span>        | <span data-ttu-id="bc580-132">WorldToView</span><span class="sxs-lookup"><span data-stu-id="bc580-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="bc580-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc580-133">float4x4</span></span>        | <span data-ttu-id="bc580-134">Sas. 投影</span><span class="sxs-lookup"><span data-stu-id="bc580-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="bc580-135">float2</span><span class="sxs-lookup"><span data-stu-id="bc580-135">float2</span></span>          | <span data-ttu-id="bc580-136">NearFarClipping</span><span class="sxs-lookup"><span data-stu-id="bc580-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="bc580-137">淺色</span><span class="sxs-lookup"><span data-stu-id="bc580-137">Light</span></span>](#light)                     | <span data-ttu-id="bc580-138">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="bc580-138">SasAmbientLight</span></span> | <span data-ttu-id="bc580-139">AmbientLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="bc580-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="bc580-140">int</span><span class="sxs-lookup"><span data-stu-id="bc580-140">int</span></span>             | <span data-ttu-id="bc580-141">Sas. NumAmbientLights</span><span class="sxs-lookup"><span data-stu-id="bc580-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="bc580-142">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="bc580-142">SasAmbientLight</span></span> | <span data-ttu-id="bc580-143">DirectionalLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="bc580-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="bc580-144">int</span><span class="sxs-lookup"><span data-stu-id="bc580-144">int</span></span>             | <span data-ttu-id="bc580-145">Sas. NumDirectionalLights</span><span class="sxs-lookup"><span data-stu-id="bc580-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="bc580-146">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="bc580-146">SasAmbientLight</span></span> | <span data-ttu-id="bc580-147">PointLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="bc580-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="bc580-148">int</span><span class="sxs-lookup"><span data-stu-id="bc580-148">int</span></span>             | <span data-ttu-id="bc580-149">Sas. NumPointLights</span><span class="sxs-lookup"><span data-stu-id="bc580-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="bc580-150">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="bc580-150">SasAmbientLight</span></span> | <span data-ttu-id="bc580-151">焦點 \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="bc580-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="bc580-152">int</span><span class="sxs-lookup"><span data-stu-id="bc580-152">int</span></span>             | <span data-ttu-id="bc580-153">Sas. NumSpotLights</span><span class="sxs-lookup"><span data-stu-id="bc580-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="bc580-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="bc580-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="bc580-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc580-155">float4x4</span></span>        | <span data-ttu-id="bc580-156">Sas. Shadow \[ ZeroOrMore \] 。WorldToShadow</span><span class="sxs-lookup"><span data-stu-id="bc580-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="bc580-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="bc580-157">texture2D</span></span>       | <span data-ttu-id="bc580-158">Sas. Shadow \[ ZeroOrMore \] 。ShadowMap</span><span class="sxs-lookup"><span data-stu-id="bc580-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="bc580-159">骨架</span><span class="sxs-lookup"><span data-stu-id="bc580-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="bc580-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc580-160">float4x4</span></span>        | <span data-ttu-id="bc580-161">MeshToJointToWorld \[ OneOrMore\]</span><span class="sxs-lookup"><span data-stu-id="bc580-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="bc580-162">int</span><span class="sxs-lookup"><span data-stu-id="bc580-162">int</span></span>             | <span data-ttu-id="bc580-163">NumJoints</span><span class="sxs-lookup"><span data-stu-id="bc580-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="bc580-164">Time</span><span class="sxs-lookup"><span data-stu-id="bc580-164">Time</span></span>

<span data-ttu-id="bc580-165">主機應用程式的虛擬時鐘或時間值。</span><span class="sxs-lookup"><span data-stu-id="bc580-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="bc580-166">成員包括：</span><span class="sxs-lookup"><span data-stu-id="bc580-166">Members include:</span></span>

-   <span data-ttu-id="bc580-167">Sas。現在-將轉譯效果的時間點的主機應用程式虛擬時鐘的值。</span><span class="sxs-lookup"><span data-stu-id="bc580-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="bc580-168">[上一步]-目前在先前轉譯時的值。</span><span class="sxs-lookup"><span data-stu-id="bc580-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="bc580-169">FrameNumber-每個轉譯框架都會遞增一次的計數器值。</span><span class="sxs-lookup"><span data-stu-id="bc580-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="bc580-170">效果必須適當地處理這些成員的值可能會在非常長的執行時間內換行的事實。</span><span class="sxs-lookup"><span data-stu-id="bc580-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="bc580-171">現在和最後的值可能會非常大。</span><span class="sxs-lookup"><span data-stu-id="bc580-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="bc580-172">環境對應</span><span class="sxs-lookup"><span data-stu-id="bc580-172">Environment Map</span></span>

<span data-ttu-id="bc580-173">立方環境對應。</span><span class="sxs-lookup"><span data-stu-id="bc580-173">A cubic environment map.</span></span> <span data-ttu-id="bc580-174">如果效果嘗試系結至 EnvironmentMap，則主應用程式必須提供有效的 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="bc580-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="bc580-175">相機</span><span class="sxs-lookup"><span data-stu-id="bc580-175">Camera</span></span>

<span data-ttu-id="bc580-176">目前呈現的相機。</span><span class="sxs-lookup"><span data-stu-id="bc580-176">The camera currently being rendered.</span></span> <span data-ttu-id="bc580-177">成員包括：</span><span class="sxs-lookup"><span data-stu-id="bc580-177">Members include:</span></span>

-   <span data-ttu-id="bc580-178">WorldToView-相機的複合世界視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="bc580-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="bc580-179">Sas. 投影-相機的投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="bc580-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="bc580-180">NearFarClipping-接近或遠裁剪平面的值。</span><span class="sxs-lookup"><span data-stu-id="bc580-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="bc580-181">淺色</span><span class="sxs-lookup"><span data-stu-id="bc580-181">Light</span></span>

<span data-ttu-id="bc580-182">一或多個場景燈。</span><span class="sxs-lookup"><span data-stu-id="bc580-182">One or more scene lights.</span></span> <span data-ttu-id="bc580-183">光源的集合會宣告為數組，其中：</span><span class="sxs-lookup"><span data-stu-id="bc580-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="bc580-184">色彩-RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="bc580-184">Color - an RGB color.</span></span> <span data-ttu-id="bc580-185">預設值為 (0,0,0)。</span><span class="sxs-lookup"><span data-stu-id="bc580-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="bc580-186">方向-淺色方向。</span><span class="sxs-lookup"><span data-stu-id="bc580-186">Direction - the light direction.</span></span> <span data-ttu-id="bc580-187">預設值為 (0,0,0)。</span><span class="sxs-lookup"><span data-stu-id="bc580-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="bc580-188">範圍-光線對場景沒有任何作用的距離。</span><span class="sxs-lookup"><span data-stu-id="bc580-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="bc580-189">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bc580-189">The default value is 0.</span></span>
-   <span data-ttu-id="bc580-190">Theta-焦點的內部錐形角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="bc580-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="bc580-191">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bc580-191">The default value is 0.</span></span>
-   <span data-ttu-id="bc580-192">Phi-焦點的外部錐形角度，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="bc580-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="bc580-193">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="bc580-193">The default value is 0.</span></span>

<span data-ttu-id="bc580-194">燈光數目必須設定為系結至相關聯陣列的燈光數目。</span><span class="sxs-lookup"><span data-stu-id="bc580-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="bc580-195">效果可以選擇忽略燈光的數目，並系結至其中一個燈光陣列的任何元素。</span><span class="sxs-lookup"><span data-stu-id="bc580-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="bc580-196">因此，主機應用程式必須針對陣列中的燈光數目以外的元素提供有效的系結。</span><span class="sxs-lookup"><span data-stu-id="bc580-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="bc580-197">ZeroOrMore 意指陣列可以有任意數目的元素。</span><span class="sxs-lookup"><span data-stu-id="bc580-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="bc580-198">陰影</span><span class="sxs-lookup"><span data-stu-id="bc580-198">Shadow</span></span>

<span data-ttu-id="bc580-199">陰影緩衝區，其中包含：</span><span class="sxs-lookup"><span data-stu-id="bc580-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="bc580-200">WorldToShadow-矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="bc580-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="bc580-201">ShadowMap-2D 材質檔。</span><span class="sxs-lookup"><span data-stu-id="bc580-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="bc580-202">ZeroOrMore 意指陣列可以有任意數目的元素 (零表示) 的空陣列。</span><span class="sxs-lookup"><span data-stu-id="bc580-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="bc580-203">效果會宣告取樣器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bc580-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="bc580-204">骨架</span><span class="sxs-lookup"><span data-stu-id="bc580-204">Skeleton</span></span>

<span data-ttu-id="bc580-205">組成目前呈現物件的框架組。</span><span class="sxs-lookup"><span data-stu-id="bc580-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="bc580-206">畫面格範例包括骨骼和轉換。</span><span class="sxs-lookup"><span data-stu-id="bc580-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="bc580-207">這包括：</span><span class="sxs-lookup"><span data-stu-id="bc580-207">This includes:</span></span>

-   <span data-ttu-id="bc580-208">MeshToJointToWorld-矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="bc580-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="bc580-209">NumJoints-基本架構中的接點數目。</span><span class="sxs-lookup"><span data-stu-id="bc580-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="bc580-210">OneOrMore 意指陣列至少有一個，而且可以包含任何數目的元素。</span><span class="sxs-lookup"><span data-stu-id="bc580-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="bc580-211">定義支援使用相同的一組 [SasHostParameterValue 集合](#sashostparametervalue-collection) 值搭配不同的轉譯，來支援固定和 skinned 的網狀物件。</span><span class="sxs-lookup"><span data-stu-id="bc580-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="bc580-212">SasBindAddress</span><span class="sxs-lookup"><span data-stu-id="bc580-212">SasBindAddress</span></span>

<span data-ttu-id="bc580-213">這個批註會新增到效果檔案的頂端，以將效果參數與其在 [SasHostParameterValue 集合](#sashostparametervalue-collection)中定義的對應參數產生關聯。</span><span class="sxs-lookup"><span data-stu-id="bc580-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="bc580-214">批註的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="bc580-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="bc580-215">此範例會將效果世界矩陣系結至 MeshToJointToWorld 矩陣：</span><span class="sxs-lookup"><span data-stu-id="bc580-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="bc580-216">這個批註會告知主應用程式，它必須使用 MeshToJointToWorld 矩陣中的資料來設定效果世界矩陣的值。</span><span class="sxs-lookup"><span data-stu-id="bc580-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="bc580-217">系結位址注釋語法的定義與 [**ID3DXEffect**](id3dxeffect.md) 用來取得和設定效果參數的語法非常類似。</span><span class="sxs-lookup"><span data-stu-id="bc580-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="bc580-218">DXSAS 文法和 **ID3DXEffect** 方法之間的唯一差異在於新增星號索引標記。</span><span class="sxs-lookup"><span data-stu-id="bc580-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="bc580-219">以下是使用星號索引的另一個範例：</span><span class="sxs-lookup"><span data-stu-id="bc580-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="bc580-220">星號索引標記表示特定主控制項 envirnmant 值陣列的所有元素，在此案例中 (色彩) 應該在相關聯的參數中系結。</span><span class="sxs-lookup"><span data-stu-id="bc580-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="bc580-221">多個星號索引標記可讓效果系結至結構陣列的子項目，而不需要系結整個結構本身。</span><span class="sxs-lookup"><span data-stu-id="bc580-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="bc580-222">此範例會將前六個燈的色彩值系結至效果參數。</span><span class="sxs-lookup"><span data-stu-id="bc580-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc580-223">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc580-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc580-224">DirectX 標準注釋和語義參考</span><span class="sxs-lookup"><span data-stu-id="bc580-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



