---
title: 狀態物件
description: 使用 HLSL 來定義狀態物件。
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991866"
---
# <a name="state-objects"></a><span data-ttu-id="e0908-103">狀態物件</span><span class="sxs-lookup"><span data-stu-id="e0908-103">State Objects</span></span>

<span data-ttu-id="e0908-104">使用著色器模型6.3 和更新版本，應用程式除了使用 Direct3D 12 Api 之外，還能方便且彈性地在 HLSL 著色器程式碼中定義 DXR 狀態物件。</span><span class="sxs-lookup"><span data-stu-id="e0908-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="e0908-105">在 HLSL 中，會使用此語法來宣告狀態物件：</span><span class="sxs-lookup"><span data-stu-id="e0908-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="e0908-106">項目</span><span class="sxs-lookup"><span data-stu-id="e0908-106">Item</span></span>                                                                                         | <span data-ttu-id="e0908-107">描述</span><span class="sxs-lookup"><span data-stu-id="e0908-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0908-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**</span><span class="sxs-lookup"><span data-stu-id="e0908-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="e0908-109">識別子物件的類型。</span><span class="sxs-lookup"><span data-stu-id="e0908-109">Identifies the type of subobject.</span></span> <span data-ttu-id="e0908-110">必須是其中一個支援的 HLSL 子物件類型。</span><span class="sxs-lookup"><span data-stu-id="e0908-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="e0908-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="e0908-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="e0908-112">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="e0908-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**欄位 [1，2，...]**</span><span class="sxs-lookup"><span data-stu-id="e0908-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="e0908-114">子物件的欄位。</span><span class="sxs-lookup"><span data-stu-id="e0908-114">Fields of the subobject.</span></span> <span data-ttu-id="e0908-115">以下說明每個子物件類型的特定欄位。</span><span class="sxs-lookup"><span data-stu-id="e0908-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="e0908-116">子物件類型的清單：</span><span class="sxs-lookup"><span data-stu-id="e0908-116">List of subobject types:</span></span>
-   [<span data-ttu-id="e0908-117">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="e0908-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="e0908-118">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="e0908-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="e0908-119">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="e0908-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="e0908-120">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="e0908-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="e0908-121">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="e0908-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="e0908-122">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="e0908-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="e0908-123">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="e0908-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="e0908-124">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="e0908-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="e0908-125">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="e0908-125">StateObjectConfig</span></span>

<span data-ttu-id="e0908-126">StateObjectConfig 子物件型別會對應至 [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="e0908-127">它有一個欄位，也就是一個位旗標，也就是</span><span class="sxs-lookup"><span data-stu-id="e0908-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="e0908-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="e0908-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="e0908-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="e0908-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="e0908-130">或者，不是它們都是零。</span><span class="sxs-lookup"><span data-stu-id="e0908-130">or, zero for neither of them.</span></span>

<span data-ttu-id="e0908-131">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="e0908-132">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="e0908-132">GlobalRootSignature</span></span>
<span data-ttu-id="e0908-133">GlobalRootSignature 會對應至 [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="e0908-134">這些欄位包含一些描述根簽章各部分的字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="e0908-135">如需相關參考，請參閱 [在 HLSL 中指定根](../direct3d12/specifying-root-signatures-in-hlsl.md)簽章。</span><span class="sxs-lookup"><span data-stu-id="e0908-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="e0908-136">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="e0908-137">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="e0908-137">LocalRootSignature</span></span>
<span data-ttu-id="e0908-138">LocalRootSignature 會對應至 [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="e0908-139">就像全域根簽章子物件一樣，這些欄位包含一些描述根簽章各部分的字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="e0908-140">如需相關參考，請參閱 [在 HLSL 中指定根](../direct3d12/specifying-root-signatures-in-hlsl.md)簽章。</span><span class="sxs-lookup"><span data-stu-id="e0908-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="e0908-141">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="e0908-142">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="e0908-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="e0908-143">根據預設，子物件只會在與匯出相同的程式庫中宣告，因此可以套用至該匯出。</span><span class="sxs-lookup"><span data-stu-id="e0908-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="e0908-144">但是，應用程式可以覆寫該內容，並取得子物件與匯出的相關特定資訊。</span><span class="sxs-lookup"><span data-stu-id="e0908-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="e0908-145">在 HLSL 中，這個「明確關聯」是使用 SubobjectToExportsAssocation 來完成。</span><span class="sxs-lookup"><span data-stu-id="e0908-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="e0908-146">SubobjectToExportsAssocation 會對應至 [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="e0908-147">此子物件是使用語法來宣告</span><span class="sxs-lookup"><span data-stu-id="e0908-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="e0908-148">項目</span><span class="sxs-lookup"><span data-stu-id="e0908-148">Item</span></span>                                                                                         | <span data-ttu-id="e0908-149">描述</span><span class="sxs-lookup"><span data-stu-id="e0908-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0908-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="e0908-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="e0908-151">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="e0908-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span><span class="sxs-lookup"><span data-stu-id="e0908-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="e0908-153">識別匯出之子物件的字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="e0908-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**出口**</span><span class="sxs-lookup"><span data-stu-id="e0908-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="e0908-155">字串，包含以分號分隔的匯出清單。</span><span class="sxs-lookup"><span data-stu-id="e0908-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="e0908-156">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="e0908-157">請注意，這兩個欄位都使用 *匯出* 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0908-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="e0908-158">如果應用程式選擇進行匯出-重新命名，則匯出的名稱可能會與 HLSL 中的原始名稱不同。</span><span class="sxs-lookup"><span data-stu-id="e0908-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="e0908-159">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="e0908-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="e0908-160">RaytracingShaderConfig 會對應至 [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="e0908-161">此子物件是使用語法來宣告</span><span class="sxs-lookup"><span data-stu-id="e0908-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="e0908-162">項目</span><span class="sxs-lookup"><span data-stu-id="e0908-162">Item</span></span>                                                                                         | <span data-ttu-id="e0908-163">描述</span><span class="sxs-lookup"><span data-stu-id="e0908-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0908-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="e0908-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="e0908-165">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="e0908-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span><span class="sxs-lookup"><span data-stu-id="e0908-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="e0908-167">純量的儲存空間上限的數值 (計算為4個位元組，每個) 在相關 raytracing 著色器的光線承載中。</span><span class="sxs-lookup"><span data-stu-id="e0908-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="e0908-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="e0908-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="e0908-169">純量值的最大數目的數值 (計算為4個位元組，每個) 可用於相關聯 raytracing 著色器中的屬性。</span><span class="sxs-lookup"><span data-stu-id="e0908-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="e0908-170">值不能超過 [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e0908-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="e0908-171">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="e0908-172">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="e0908-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="e0908-173">RaytracingPipelineConfig 會對應至 [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) 結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="e0908-174">此子物件是使用語法來宣告</span><span class="sxs-lookup"><span data-stu-id="e0908-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="e0908-175">項目</span><span class="sxs-lookup"><span data-stu-id="e0908-175">Item</span></span>                                                                                         | <span data-ttu-id="e0908-176">描述</span><span class="sxs-lookup"><span data-stu-id="e0908-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0908-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="e0908-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="e0908-178">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="e0908-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span><span class="sxs-lookup"><span data-stu-id="e0908-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="e0908-180">Raytracing 管線中用於光線遞迴的數值限制。</span><span class="sxs-lookup"><span data-stu-id="e0908-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="e0908-181">它是介於0和31（含）之間的數位。</span><span class="sxs-lookup"><span data-stu-id="e0908-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="e0908-182">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="e0908-183">由於 raytracing 遞迴有效能成本，因此應用程式應該使用所需結果的最低遞迴深度。</span><span class="sxs-lookup"><span data-stu-id="e0908-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="e0908-184">如果著色器調用尚未到達最大遞迴深度，則可以呼叫 [TraceRay](../direct3d12/traceray-function.md) 任何次數。</span><span class="sxs-lookup"><span data-stu-id="e0908-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="e0908-185">但是，如果它們達到或超過最大的遞迴深度，則呼叫 TraceRay 會將裝置置於已移除狀態。</span><span class="sxs-lookup"><span data-stu-id="e0908-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="e0908-186">因此，如果 raytracing 著色器已符合或超過最大遞迴深度，則應該小心停止呼叫 TraceRay。</span><span class="sxs-lookup"><span data-stu-id="e0908-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="e0908-187">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="e0908-187">TriangleHitGroup</span></span>

<span data-ttu-id="e0908-188">TriangleHitGroup 會對應至其類型欄位設定為[D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)的[D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc)結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="e0908-189">此子物件是使用語法來宣告</span><span class="sxs-lookup"><span data-stu-id="e0908-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="e0908-190">項目</span><span class="sxs-lookup"><span data-stu-id="e0908-190">Item</span></span>                                                                                         | <span data-ttu-id="e0908-191">描述</span><span class="sxs-lookup"><span data-stu-id="e0908-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0908-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="e0908-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="e0908-193">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="e0908-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="e0908-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="e0908-195">點擊群組之 anyhit 著色器的字串名稱，或空字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="e0908-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="e0908-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="e0908-197">點擊群組最接近的點擊著色器的字串名稱，或空字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="e0908-198">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="e0908-199">請注意，這兩個欄位都使用 *匯出* 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0908-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="e0908-200">如果應用程式選擇進行匯出-重新命名，則匯出的名稱可能會與 HLSL 中的原始名稱不同。</span><span class="sxs-lookup"><span data-stu-id="e0908-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="e0908-201">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="e0908-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="e0908-202">ProceduralPrimitiveHitGroup 會對應至其類型欄位設定為[D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)的[D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc)結構。</span><span class="sxs-lookup"><span data-stu-id="e0908-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="e0908-203">此子物件是使用語法來宣告</span><span class="sxs-lookup"><span data-stu-id="e0908-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="e0908-204">項目</span><span class="sxs-lookup"><span data-stu-id="e0908-204">Item</span></span>                                                                                         | <span data-ttu-id="e0908-205">描述</span><span class="sxs-lookup"><span data-stu-id="e0908-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0908-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="e0908-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="e0908-207">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="e0908-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="e0908-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="e0908-209">點擊群組之 anyhit 著色器的字串名稱，或空字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="e0908-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="e0908-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="e0908-211">點擊群組最接近的點擊著色器的字串名稱，或空字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="e0908-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span><span class="sxs-lookup"><span data-stu-id="e0908-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="e0908-213">點擊群組之交集著色器的字串名稱，或空字串。</span><span class="sxs-lookup"><span data-stu-id="e0908-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="e0908-214">範例：</span><span class="sxs-lookup"><span data-stu-id="e0908-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="e0908-215">請注意，這三個欄位使用 *匯出* 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0908-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="e0908-216">如果應用程式選擇進行匯出-重新命名，則匯出的名稱可能會與 HLSL 中的原始名稱不同。</span><span class="sxs-lookup"><span data-stu-id="e0908-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0908-217">備註</span><span class="sxs-lookup"><span data-stu-id="e0908-217">Remarks</span></span>

<span data-ttu-id="e0908-218">子物件具有 "association" 的概念，或 "association with with export"。</span><span class="sxs-lookup"><span data-stu-id="e0908-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="e0908-219">透過著色器程式碼指定子物件時，選擇「哪一個子物件與哪個匯出」遵循 [DXR 規格](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior)中所述的規則。</span><span class="sxs-lookup"><span data-stu-id="e0908-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="e0908-220">尤其是，假設應用程式有一些匯出。</span><span class="sxs-lookup"><span data-stu-id="e0908-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="e0908-221">如果應用程式透過著色器程式碼和根簽章 B，將該匯出與根簽章 A 產生關聯，則會使用 B。</span><span class="sxs-lookup"><span data-stu-id="e0908-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="e0908-222">「使用 B」的設計，而不是「產生錯誤」，讓應用程式能夠使用應用程式程式碼輕鬆覆寫 DXIL 的關聯，而不是強制重新編譯著色器來解決不相符的專案。</span><span class="sxs-lookup"><span data-stu-id="e0908-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0908-223">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0908-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0908-224">DirectX 開發人員 Blog 文章：「D3D12 的新功能– DirectX Raytracing (DXR) 現在支援程式庫子內容」</span><span class="sxs-lookup"><span data-stu-id="e0908-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="e0908-225">DirectX Raytracing (DXR) 功能規格</span><span class="sxs-lookup"><span data-stu-id="e0908-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="e0908-226">範例： D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="e0908-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>