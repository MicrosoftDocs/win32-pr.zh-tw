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
# <a name="state-objects"></a>狀態物件

使用著色器模型6.3 和更新版本，應用程式除了使用 Direct3D 12 Api 之外，還能方便且彈性地在 HLSL 著色器程式碼中定義 DXR 狀態物件。

在 HLSL 中，會使用此語法來宣告狀態物件：

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**<br/>     | 識別子物件的類型。 必須是其中一個支援的 HLSL 子物件類型。<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**欄位 [1，2，...]**<br/> | 子物件的欄位。 以下說明每個子物件類型的特定欄位。<br/> |




子物件類型的清單：
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

StateObjectConfig 子物件型別會對應至 [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) 結構。

它有一個欄位，也就是一個位旗標，也就是

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

或者，不是它們都是零。

範例：

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>GlobalRootSignature
GlobalRootSignature 會對應至 [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) 結構。

這些欄位包含一些描述根簽章各部分的字串。 如需相關參考，請參閱 [在 HLSL 中指定根](../direct3d12/specifying-root-signatures-in-hlsl.md)簽章。

範例：
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>LocalRootSignature
LocalRootSignature 會對應至 [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) 結構。

就像全域根簽章子物件一樣，這些欄位包含一些描述根簽章各部分的字串。 如需相關參考，請參閱 [在 HLSL 中指定根](../direct3d12/specifying-root-signatures-in-hlsl.md)簽章。

範例：
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
根據預設，子物件只會在與匯出相同的程式庫中宣告，因此可以套用至該匯出。 但是，應用程式可以覆寫該內容，並取得子物件與匯出的相關特定資訊。 在 HLSL 中，這個「明確關聯」是使用 SubobjectToExportsAssocation 來完成。

SubobjectToExportsAssocation 會對應至 [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) 結構。

此子物件是使用語法來宣告

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**<br/>     | 識別匯出之子物件的字串。<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**出口**<br/> | 字串，包含以分號分隔的匯出清單。<br/> |


範例：
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

請注意，這兩個欄位都使用 *匯出* 的名稱。 如果應用程式選擇進行匯出-重新命名，則匯出的名稱可能會與 HLSL 中的原始名稱不同。

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

RaytracingShaderConfig 會對應至 [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) 結構。

此子物件是使用語法來宣告

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | 純量的儲存空間上限的數值 (計算為4個位元組，每個) 在相關 raytracing 著色器的光線承載中。<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | 純量值的最大數目的數值 (計算為4個位元組，每個) 可用於相關聯 raytracing 著色器中的屬性。 值不能超過 [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md)。<br/> |


範例：
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

RaytracingPipelineConfig 會對應至 [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) 結構。

此子物件是使用語法來宣告

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Raytracing 管線中用於光線遞迴的數值限制。 它是介於0和31（含）之間的數位。 <br/> |


範例：
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
由於 raytracing 遞迴有效能成本，因此應用程式應該使用所需結果的最低遞迴深度。

如果著色器調用尚未到達最大遞迴深度，則可以呼叫 [TraceRay](../direct3d12/traceray-function.md) 任何次數。 但是，如果它們達到或超過最大的遞迴深度，則呼叫 TraceRay 會將裝置置於已移除狀態。 因此，如果 raytracing 著色器已符合或超過最大遞迴深度，則應該小心停止呼叫 TraceRay。

## <a name="trianglehitgroup"></a>TriangleHitGroup

TriangleHitGroup 會對應至其類型欄位設定為[D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)的[D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc)結構。

此子物件是使用語法來宣告

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | 點擊群組之 anyhit 著色器的字串名稱，或空字串。<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | 點擊群組最接近的點擊著色器的字串名稱，或空字串。<br/> |


範例：
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

請注意，這兩個欄位都使用 *匯出* 的名稱。 如果應用程式選擇進行匯出-重新命名，則匯出的名稱可能會與 HLSL 中的原始名稱不同。

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

ProceduralPrimitiveHitGroup 會對應至其類型欄位設定為[D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)的[D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc)結構。

此子物件是使用語法來宣告

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | 點擊群組之 anyhit 著色器的字串名稱，或空字串。<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | 點擊群組最接近的點擊著色器的字串名稱，或空字串。<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | 點擊群組之交集著色器的字串名稱，或空字串。<br/> |


範例：
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

請注意，這三個欄位使用 *匯出* 的名稱。 如果應用程式選擇進行匯出-重新命名，則匯出的名稱可能會與 HLSL 中的原始名稱不同。

## <a name="remarks"></a>備註

子物件具有 "association" 的概念，或 "association with with export"。

透過著色器程式碼指定子物件時，選擇「哪一個子物件與哪個匯出」遵循 [DXR 規格](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior)中所述的規則。 尤其是，假設應用程式有一些匯出。 如果應用程式透過著色器程式碼和根簽章 B，將該匯出與根簽章 A 產生關聯，則會使用 B。 「使用 B」的設計，而不是「產生錯誤」，讓應用程式能夠使用應用程式程式碼輕鬆覆寫 DXIL 的關聯，而不是強制重新編譯著色器來解決不相符的專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX 開發人員 Blog 文章：「D3D12 的新功能– DirectX Raytracing (DXR) 現在支援程式庫子內容」](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[DirectX Raytracing (DXR) 功能規格](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[範例： D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>