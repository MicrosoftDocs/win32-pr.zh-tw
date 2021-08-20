---
title: Direct3D 12 的 Helper 結構
description: 這些 helper 結構有助於初始化許多 Direct3D 12 結構。 它們是在中宣告 `d3dx12.h` 。
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Helper 結構
- d3dx12。h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812370"
---
# <a name="helper-structures-for-direct3d-12"></a>Direct3D 12 的 Helper 結構

這些 helper 結構有助於初始化許多 Direct3D 12 結構。 它們是在中宣告 `d3dx12.h` 。

`d3dx12.h` 可以與 Direct3D 12 標頭分開使用。 您可以 `d3dx12.h` 從 [D3D12 Helper 程式庫](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)進行下載。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) 結構。 |
| [**CD3DX12_BOX**](cd3dx12-box.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) 結構。 |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) 結構。 |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構。 |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | 將 **D3D12_DEFAULT** 傳遞至每個 helper 結構的函式。 此結構只是用來做為在其他 helper 結構上設定預設參數的機制。 |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) 結構。 |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) 結構。 |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) 結構。 |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) 結構。 |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | 用來建立 DXIL 程式庫狀態子物件的 helper 類別。 |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | 協助程式類別，用於建立 DXIL 子物件與匯出關聯狀態子物件。 |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | 建立現有集合狀態子物件的 helper 類別。 |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | 用來建立全域根簽章狀態 suboject 的 helper 類別。 |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構。 |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) 結構。 |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) 結構。 |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | 建立點擊群組狀態子物件的 helper 類別。 |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Helper 類別，用於建立狀態子物件，以識別要套用狀態物件的 GPU 節點。 |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | 用來建立本機根簽章狀態 suboject 的 helper 類別。 |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | 協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 請參閱 [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 和 [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。 |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | 協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 請參閱 [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 和 [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。 |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | 協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | 協助程式結構，用來將 blend 描述描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | 用來將快取的 PSO 描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | 協助程式結構，用來將計算著色器描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | 用來將深度樣板描述描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | 用來將深度樣板描述描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | 用來將深度樣板格式描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | 協助程式結構，用來將網域著色器描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | 用來將管線狀態旗標描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | 用來將幾何著色器描述為適合資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | 協助程式結構，可用來將輪廓著色器描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | 協助程式結構，用來將索引緩衝區區域剪下值描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | 用來將輸入配置描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | 用來將節點遮罩描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | 從傳遞至對應成員函式的物件詳細資料，建立內部 CD3DX12_PIPELINE_STATE_STREAM 物件。 此結構會實 [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) 介面。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | 用來將基本拓撲描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | 協助程式結構，用來描述圖元著色器，做為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | 協助程式結構，用來將轉譯器描述描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | 協助程式結構，用來將轉譯目標格式描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | 用來將根簽章描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC**](cd3dx12-pipeline-state-stream-sample-desc.md) | 協助程式結構，用來將範例描述描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | 用來將範例遮罩描述為適用于資料流程描述之單一物件的 helper 結構。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | 協助程式結構，用來將資料流程輸出描述當做適合資料流程描述的單一物件來描述。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | 樣板化的 helper 結構，用來將子物件類型和子物件資料組封裝成適合資料流程描述的單一物件。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | 用來包裝 [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) 結構的 helper 結構。 允許著色器使用單一繪製呼叫轉譯成多個視圖;適用于身歷聲視覺或立方體貼圖產生。 |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | 協助程式結構，用來將頂點著色器描述為適合資料流程描述的單一物件。 |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) 結構。 |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) 結構。 |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) 結構。 |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | 建立 raytracing 管線設定狀態子物件的 helper 類別。 |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | 用來建立具有旗標之 raytracing 管線設定狀態子物件的 helper 類別。 |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | 建立 raytracing 著色器設定狀態子物件的 helper 類別。 |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RECT**](d3d12-rect.md) 結構。 |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) 結構。 |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) 結構。 |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) 結構。 |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) 結構。 |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) 結構。 |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) 結構。 |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) 結構。 |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) 結構。 |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) 結構。 |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) 結構。 |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) 結構。 |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 結構。 |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。 |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) 結構。 |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Helper 類別，用於建立子物件，以定義狀態物件的一般屬性。 |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | D3DX12 狀態物件建立協助程式的 central 類別，這是用來從任意一組子物件建立狀態物件的 helper 類別。 |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構。 |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | 用來建立子物件與匯出關聯狀態子物件的 helper 類別。 |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 結構。 |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) 結構。 |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 結構。 |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) 結構。 |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) 結構。 |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) 結構。 |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) 結構。 |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構。 |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) 結構。 |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | 協助程式結構，可讓您輕鬆地初始化 [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) 結構。 |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | 針對 [網狀 amplifications 著色](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)器，您可以使用來自 [EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription)的資料（使用 **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**）來提供所有狀態。 |

## <a name="related-topics"></a>相關主題

* [D3D12 的 Helper 結構和函式](helper-structures-and-functions-for-d3d12.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
