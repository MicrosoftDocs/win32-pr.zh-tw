---
title: 下層硬體上的計算著色器
description: 本主題將討論如何在 Direct3D 10 硬體上的 Direct3D 11 應用程式中使用計算著色器。
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024302"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>下層硬體上的計算著色器

Direct3D 11 提供使用 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器的功能，可在大部分的 Direct3D 2.x 硬體上運作，但有一些作業限制。 計算著色器技術也稱為 DirectCompute 技術。 本主題將討論如何在 Direct3D 10 硬體上的 Direct3D 11 應用程式中使用 [計算著色](direct3d-11-advanced-stages-compute-shader.md) 器。

舊版硬體上的計算著色器支援僅適用于與 Direct3D 2.x 相容的裝置。 無法在 Direct3D 2.x 硬體上使用計算著色器。

若要檢查 Direct3D 10. x 硬體是否支援計算著色器，請呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)。 在 **CheckFeatureSupport** 呼叫中，將 D3D11 \_ feature \_ D3D10 \_ X \_ 硬體 \_ 選項值傳遞至 *FEATURE* 參數、將 [**D3D11 \_ FEATURE \_ data \_ D3D10 \_ x \_ 硬體 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) 結構的指標傳遞至 *pFeatureSupportData* 參數，並將 **D3D11 \_ FEATURE \_ data \_ D3D10 \_ x \_ 硬體 \_ 選項** 結構的大小傳遞給 *FeatureSupportDataSize* 參數。 如果 Direct3D 2.x 硬體支援計算著色器， **CheckFeatureSupport** 會在 ComputeShaders Plus RawAndStructuredBuffers 中透過 **D3D11 \_ FEATURE \_ DATA \_ D3D10 \_ x \_ 硬體 \_ 選項** 的 **\_ \_ \_ \_ 著色器 \_ 4 \_ x** 成員傳回 **TRUE** 。

[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。

-   [未排序的存取視圖 (UAVs) ](#unordered-access-views-uavs)
-   [著色器資源檢視 (SRVs) ](#shader-resource-views-srvs)
-   [執行緒群組](#thread-groups)
    -   [執行緒群組維度](#thread-group-dimensions)
    -   [二維執行緒索引](#two-dimensional-thread-indices)
    -   [執行緒群組共用記憶體 (TGSM) ](#thread-group-shared-memory-tgsm)
-   [使用 D3DCOMPILE \_ SKIP \_ 優化的 D3DCompile](/windows)
-   [相關主題](#related-topics)

## <a name="unordered-access-views-uavs"></a>未排序的存取視圖 (UAVs) 

舊版硬體支援原始的 ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) 和結構化 ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) 未排序的存取視圖，但有下列限制：

-   一次只能透過 [**>id3d11devicecoNtext：： CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)，將單一 UAV 系結至管線。
-   原始 UAV 的基底位移必須對齊256位元組的界限 (而不是 Direct3D 11 硬體) 所需的16位元組對齊。

下層硬體不支援具類型的 UAVs。 這包括 [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)、 [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)和 [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAVs。

下層硬體上的圖元著色器不支援未排序的存取。

## <a name="shader-resource-views-srvs"></a>著色器資源檢視 (SRVs) 

在舊版硬體上，支援將原始和結構化緩衝區作為著色器資源查看，以進行唯讀存取，因為它們是在 Direct3D 11 硬體上。 這些資源類型支援頂點著色器、幾何著色器、圖元著色器以及計算著色器。

## <a name="thread-groups"></a>執行緒群組

計算著色器可以線上程群組內以平行方式在多個執行緒上執行。

下層硬體支援執行緒群組，但有下列限制：

### <a name="thread-group-dimensions"></a>執行緒群組維度

針對下層硬體定義的執行緒群組受限於768的 X 和 Y 維度。 這小於 Direct3D 11 硬體的最大值1024。 64的最大 Z 維度未變更。

群組中的執行緒總數 (X × Y × Z) 限制為768。 這小於適用于 Direct3D 11 硬體的1024限制。

如果超過這些數位，著色器編譯將會失敗。

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional 執行緒索引

執行緒群組內的特定執行緒會使用 (x、y、z) 指定的3D 向量進行編制索引。

針對在舊版硬體上運作的計算著色器，執行緒群組只支援兩個維度。 這表示3D 向量中的 Z 值必須一律為1。

這項限制特別適用于下列各項：

-   [**>id3d11devicecoNtext：:D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)— *ThreadGroupCountZ* 引數必須是1。
-   [**>id3d11devicecoNtext：:D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)-在舊版硬體上不支援此功能。
-   [numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)-Z 值必須是1。

### <a name="thread-group-shared-memory-tgsm"></a>執行緒群組共用記憶體 (TGSM) 

執行緒群組共用記憶體僅限於在下層硬體上16Kb。 這小於適用于 Direct3D 11 硬體的32Kb。

計算著色器執行緒只能寫入自己的 TGSM 區域。 這個僅限寫入區域的大小上限為256個位元組或較小，且最大值會隨著針對群組宣告的執行緒數目增加而減少。

下錶針對群組中的執行緒數目，定義每個執行緒的 TGSM 區域大小上限：



| 群組中的執行緒數目 | 每個執行緒的 TGSM 大小上限 |
|----------------------------|------------------------------|
| 0-64                       | 256                          |
| 65-68                      | 240                          |
| 69-72                      | 224                          |
| 73-76                      | 208                          |
| 77-84                      | 192                          |
| 85-92                      | 176                          |
| 93-100                     | 160                          |
| 101-112                    | 144                          |
| 113-128                    | 128                          |
| 129-144                    | 112                          |
| 145-168                    | 96                           |
| 169-204                    | 80                           |
| 205-256                    | 64                           |
| 257-340                    | 48                           |
| 341-512                    | 32                           |
| 513-768                    | 16                           |



 

計算著色器執行緒可能會從任何位置讀取 TGSM。

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>使用 D3DCOMPILE \_ SKIP \_ 優化的 D3DCompile

當您傳遞 cs 4 0 做為著色器目標時， [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile)會傳回 **E \_ >notimpl** ， \_ \_ 以及 [**D3DCompile \_ SKIP \_ 優化**](/windows/desktop/direct3dhlsl/d3dcompile-constants)編譯選項。 Cs \_ 5 \_ 0 著色器目標適用于 **D3DCOMPILE \_ SKIP \_ 優化**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[舊版硬體上的 Direct3D 11](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 