---
title: " (Direct3D 12 圖形) 的核心結構"
description: 下列結構是在 d3d12 中宣告。
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5dd546055c22711ecd9a3796e520ad034e9e46c6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812683"
---
# <a name="core-structures"></a>核心結構

下列結構是在 d3d12 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題和描述 |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node)。 代表裝置已移除的擴充資料 (DR) 自動階層連結資料，做為連結清單中的節點。 |
| [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc)。 描述 blend 狀態。 |
| [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box)。 描述3D 方塊。 |
| [**D3D12_BUFFER_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_rtv)。 描述要用於轉譯目標視圖之緩衝區資源中的元素。 |
| [**D3D12_BUFFER_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_srv)。 描述緩衝區資源中要在著色器資源檢視中使用的元素。 |
| [**D3D12_BUFFER_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav)。 描述緩衝區中要用於未排序存取視圖的元素。 |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)。 儲存管線狀態。 |
| [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value)。 描述用來將特定資源的明確作業優化的值。 |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)。 描述命令佇列。 |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)。 描述命令簽章 (參數) 的引數。 |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。 描述計算管線狀態物件。 |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)。 描述要查看的常數緩衝區。 |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)。 描述 CPU 描述項控制碼。 |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)。 描述深度樣板的狀態。 |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)。 描述深度樣板的狀態。 |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_value)。 指定深度和範本值。 |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc)。 描述可從深度範本視圖存取的材質子資源。 |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc)。 描述可根據樣板測試結果執行的樣板作業。 |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)。 描述描述元堆積。 |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range)。 描述描述項範圍。 |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1)。 描述描述項範圍，以及用來判斷其變動性的旗標。 |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data)。 代表裝置已移除 (DR) 1.0 版資料的擴充資料。 |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1)。 代表裝置移除的延伸資料 (DR) 1.1 版裝置移除資料，讓偵錯工具和偵錯工具擴充功能可以存取 DR 資料。 |
| [**D3D12_DISCARD_REGION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region)。 描述捨棄資源作業的詳細資料。 |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)。 描述可供計算著色器使用的分派參數。 |
| [**D3D12_DRAW_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_arguments)。 描述繪圖實例的參數。 |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)。 描述用來繪製索引實例的參數。 |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_allocation_node)。 描述為連結清單中的節點，裝置所追蹤之配置的相關資料 (DR) 移除擴充的資料。 |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output)。 包含 [D3D12_AUTO_BREADCRUMB_NODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) 物件之連結清單的標頭指標。 此清單代表裝置移除之前的自動階層連結狀態。 |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output)。 描述與指定虛擬位址 (VA) 的 GPU 分頁錯誤相關的配置資料。 |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)。 提供有關介面卡架構的詳細資料，協助應用程式更有效地針對某些介面卡屬性進行優化。 |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1)。 提供有關介面卡架構的詳細資料，協助應用程式更有效地針對某些介面卡屬性進行優化。 |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority)。 詳細說明支援不同命令佇列類型優先順序的介面卡。 |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node)。 指出不同介面卡之間共用資源的支援層級。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)。 描述目前圖形驅動程式中的 Direct3D 12 功能選項。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1)。 描述 HLSL 6.0 wave 作業的支援層級。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2)。 詳細說明此介面卡對 Direct3D 12 某些選用功能的支援。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3)。 用來指出介面卡針對 Direct3D 12 的選用功能提供的支援層級。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4)。 指出支援64KB 對齊的 MSAA 紋理、跨 API 共用和原生16位著色器作業的層級。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5)。 指出介面卡針對轉譯行程、光線追蹤和著色器所提供的支援層級，以及並排顯示的資源。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6)。 指出介面卡為可變速率陰影提供的支援層級 (VRS) ，並指出是否支援背景處理。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS7**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7)。 指出介面卡針對網格和放大著色器提供的支援層級，以及取樣器的意見反應。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS8**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options8)。 指出是否支援未對齊的區塊壓縮紋理。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS9**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9)。 指出網格著色器的支援是否存在、8或以上的 *SV_RenderTargetArrayIndex* 值、具類型的資源64位整數 atomics、衍生和衍生相依紋理範例作業，以及 WaveMMA (wave_matrix) 作業的支援層級。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS10**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options10)。 指出是否可以使用 SUM 結合器，以及是否可以從網格著色器設定 *SV_ShadingRate* 。 |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS11**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11)。 指出是否支援描述項堆積中資源的64位整數 atomics。 |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps)。 用來 determinine 介面卡是否支援從現有的系統記憶體建立堆積。 這類堆積並非供一般用途使用，但對診斷用途來說非常有用，因為即使在介面卡發生錯誤或遇到裝置移除事件之後，仍保證仍能保存這些堆積。 |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels)。 描述目前圖形驅動程式所支援之 [功能層級](/windows/win32/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 的相關資訊。 |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)。 描述 DXGI 資料格式。 |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_support)。 描述目前圖形驅動程式支援的資源，以指定的格式。 |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support)。 詳細說明介面卡的 GPU 虛擬位址空間限制，包括每個資源和每個進程的最大位址位。 |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels)。 描述給定格式和取樣計數的影像品質層級。 |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support)。 指出受保護資源會話的支援層級。 |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPE_COUNT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_type_count)。 指出受保護資源會話類型的計數。 |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_types)。 指出受保護的資源會話類型清單。 |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command)。 指出介面卡為 metacommands 提供的支援層級。 |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature)。 將此結構傳遞至 [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ，以檢查根簽章版本支援。 |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_serialization)。 表示堆積序列化的支援層級。 |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache)。 描述目前圖形驅動程式所支援的著色器快取層級。 |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model)。 包含支援的著色器模型。 |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)。 描述 GPU 描述項控制碼。 |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)。 描述圖形管線狀態物件。 |
| [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc)。 描述堆積。 |
| [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties)。 描述堆積屬性。 |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_index_buffer_view)。 描述要查看的索引緩衝區。 |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)。 描述間接引數 (間接參數) ，以搭配命令簽章使用。 |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc)。 描述圖形管線之輸入組合語言階段的單一元素。 |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_layout_desc)。 描述輸入組合語言階段的輸入緩衝區資料。 |
| [**D3D12_MEMCPY_DEST**](/windows/win32/api/d3d12/ns-d3d12-d3d12_memcpy_dest)。 描述記憶體複製作業的目的地。 |
| [**D3D12_META_COMMAND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_desc)。 描述中繼命令。 |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc)。 描述中繼命令的參數。 |
| [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info)。 描述具有 mipmap 之已並排資源的磚結構。 |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)。 描述管線狀態資料流程。 |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)。 描述放置 subresource 的使用量，包括位移和 D3D12_SUBRESOURCE_FOOTPRINT。 |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc)。 描述每個介面卡的受保護資源會話旗標。 |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics)。 在呼叫 [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)之間，查詢圖形中的管線活動相關資訊。 |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics)。 描述資料流程輸出的查詢資料。 |
| [**D3D12_QUERY_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc)。 描述查詢堆積的用途。 查詢堆積包含個別查詢的陣列。 |
| [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range)。 描述記憶體範圍。 |
| [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64)。 描述64位位址空間中的記憶體範圍。 |
| [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)。 描述轉譯器的狀態。 |
| [**D3D12_RAYTRACING_AABB**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_aabb)。 表示以軸對齊的周框方塊 (AABB) 當做 raytracing 幾何使用。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc)。 描述壓縮之後加速結構的空間需求。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc)。 描述加速結構目前所使用的空間。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc)。 要從加速結構產生的後置資訊描述。 在對 [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) 和 [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure)的呼叫中使用此結構。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc)。 描述序列化加速結構和標頭的大小和配置 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc)。 描述將加速結構解碼成可由工具視覺化的表單空間需求。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info)。 表示有關 raytracing 加速結構的建置前資訊。 藉由呼叫 [**GetRaytracingAccelerationStructurePrebuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo)來取得這個結構的實例。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv)。 著色器資源檢視 (SRV) 結構來儲存 raytracing 加速結構。 |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc)。 描述一組軸對齊的周框方塊，在 [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) 結構中用來提供輸入資料給 RAYTRACING 加速結構組建作業。 |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc)。 描述 [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) 結構中用來提供輸入資料給 RAYTRACING 加速結構建立作業的一組幾何。 |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc)。 描述一組用來作為 raytracing 幾何的三角形。 此結構所指向的幾何一律是在三角形清單表單中、已編制索引或非索引。 不支援三角形的條紋。 |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc)。 描述在加速結構建立程式期間用於 GPU 記憶體中的 raytracing 加速結構的實例。 |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config)。 代表 raytracing 管線設定的狀態子物件。 |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config1)。 代表 raytracing 管線設定的狀態子物件，具有旗標。 |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config)。 表示著色器設定的狀態子物件。 |
| [**D3D12_RECT**](d3d12-rect.md)。 D3D12_RECT 宣告為 RECT。 |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access)。 描述在轉換成轉譯行程時，應用程式所要求之資源 (s) 的存取權。 |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters)。 描述在轉譯行程開始時，應該清除資源 (s) 的純量值。 |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc)。 描述在轉譯階段) 至深度樣板視圖 (DSV) ，以及其開始和結束存取特性的持續時間內， (固定的系結。 |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access)。 描述從轉譯行程轉換時，應用程式所要求之資源 (s) 的存取權。 |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters)。 描述在轉譯階段結束時要解析的資源。 |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters)。 描述在轉譯行程結束時要解決的子資源。 |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc)。 描述在轉譯行程) 至一或多個轉譯目標視圖 (RTVs) ，以及其開始和結束存取特性的期間， (固定的系結。 |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc)。 描述呈現目標的 blend 狀態。 |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_view_desc)。 描述可使用呈現目標視圖存取之資源的子資源。 |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier)。 描述兩個具有對應至相同堆積之不同資源的使用方式之間的轉換。 |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)。 描述配置資源所需的參數。 |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1)。 描述配置資源所需的參數，包括位移。 |
| [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier)。 描述資源使用) 中 (轉換的資源屏障。 |
| [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc)。 描述資源，例如紋理。 此結構廣泛使用。 |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier)。 描述不同使用方式之間的子資源轉換。 |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier)。 代表資源，在此資源中，所有 UAV 存取都必須先完成，才能開始任何未來的 UAV 存取。 |
| [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants)。 描述以單一常數緩衝區形式出現在著色器中的根簽章中內嵌的常數。 |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor)。 描述以著色器顯示的根簽章版本1.0 中內嵌的描述項。 |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1)。 描述以著色器顯示的根簽章版本1.1 中內嵌的描述項。 |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)。 描述描述中繼資料表的根簽章1.0 配置，做為描述項範圍中另一個後面出現的描述項範圍集合。 |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)。 描述描述中繼資料表的根簽章1.1 配置，做為描述項範圍中另一個後面出現的描述項範圍集合。 |
| [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter)。 描述根簽章版本1.0 的位置。 |
| [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1)。 描述根簽章版本1.1 的位置。 |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc)。 描述根簽章版本1.0 的版面配置。 |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)。 描述根簽章版本1.1 的版面配置。 |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array)。 包裝轉譯目標格式的陣列。 |
| [**D3D12_SAMPLE_POSITION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sample_position)。 描述用於可程式化範例位置的子圖元取樣位置。 |
| [**D3D12_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sampler_desc)。 描述取樣器狀態。 |
| [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)。 描述著色器資料。 |
| [**D3D12_SHADER_CACHE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_cache_session_desc)。 描述著色器快取會話。 |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc)。 描述著色器資源檢視。 |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_so_declaration_entry)。 描述輸出位置頂點緩衝區中的頂點元素。 |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)。 描述靜態取樣器。 |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view)。 描述資料流程輸出緩衝區。 |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_desc)。 描述串流輸出緩衝區。 |
| [**D3D12_SUBRESOURCE_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_data)。 描述 subresource 資料。 |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint)。 描述 subresource 至父資源的格式、寬度、高度、深度和資料列的間距。 |
| [**D3D12_SUBRESOURCE_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_info)。 描述 subresource 資料。 |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)。 描述 subresource 的記憶體範圍。 |
| [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling)。 描述已平 subresource 的磁片區。 |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)。 描述要在深度樣板視圖中使用的一維紋理陣列子資源。 |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)。 描述要在轉譯目標視圖中使用的一維紋理陣列子資源。 |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)。 描述從1D 紋理的陣列子資源，以用於著色器資源檢視。 |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)。 描述未排序存取的1D 材質資源陣列。 |
| [**D3D12_TEX1D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)。 描述可供深度樣板視圖存取的1D 紋理 subresource。 |
| [**D3D12_TEX1D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)。 描述要在轉譯目標視圖中使用的1D 材質 subresource。 |
| [**D3D12_TEX1D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_srv)。 指定要在著色器資源檢視中使用的一維材質 subresource。 |
| [**D3D12_TEX1D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_uav)。 描述未排序存取的1D 材質資源。 |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)。 從2D 材質陣列描述可供深度樣板視圖存取的子資源。 |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)。 描述要在轉譯目標視圖中使用的2D 材質陣列子資源。 |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)。 描述從2D 材質陣列子資源至著色器資源檢視中使用的程式。 |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)。 描述未排序存取2D 材質資源的陣列。 |
| [**D3D12_TEX2D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)。 描述可供深度樣板視圖存取之2D 材質的 subresource。 |
| [**D3D12_TEX2D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)。 描述從2D 材質到轉譯目標視圖中使用的 subresource。 |
| [**D3D12_TEX2D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_srv)。 描述從2D 材質到著色器資源檢視中使用的 subresource。 |
| [**D3D12_TEX2D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_uav)。 描述未排序的存取2D 材質資源。 |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)。 描述深度樣板視圖的多取樣2D 材質陣列中的子資源。 |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)。 描述從多取樣2D 材質的陣列子資源，以便在轉譯目標視圖中使用。 |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)。 描述從多取樣2D 材質的陣列子資源，以用於著色器資源檢視。 |
| [**D3D12_TEX2DMS_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)。 描述可供深度樣板視圖存取之多取樣2D 材質的 subresource。 |
| [**D3D12_TEX2DMS_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)。 描述要在轉譯目標視圖中使用之多取樣2D 材質的 subresource。 |
| [**D3D12_TEX2DMS_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)。 描述從多取樣2D 材質子資源，以用於著色器資源檢視。 |
| [**D3D12_TEX3D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)。 描述要在呈現目標視圖中使用的3D 材質子資源。 |
| [**D3D12_TEX3D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_srv)。 描述要在著色器資源檢視中使用的3D 紋理子資源。 |
| [**D3D12_TEX3D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_uav)。 描述未排序存取的3D 材質資源。 |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)。 描述要在著色器資源檢視中使用的 cube 紋理陣列子資源。 |
| [**D3D12_TEXCUBE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_srv)。 描述要在著色器資源檢視中使用的 cube 材質 subresource。 |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location)。 描述材質複製用途的材質部分。 |
| [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size)。 描述已並排區域的大小。 |
| [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape)。 藉由指定圖格的維度來描述其形狀。 |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)。 描述磚資源的座標。 |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc)。 描述可使用未排序存取視圖來存取的資源子資源。 |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)。 描述頂點緩衝區視圖。 |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data)。 表示已建立版本的裝置 (DR) 資料來移除擴充的資料，讓偵錯工具和偵錯工具擴充功能可以存取 DR 資料。 |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)。 保存任何版本的根簽章描述，而且是設計來搭配序列化/還原序列化函數使用。 |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instance_location)。 指定與視圖實例相關聯的區/樣板和轉譯目標。 |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc)。 指定在 view 實例設定期間使用的參數。 |
| [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)。 描述區的維度。 |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter)。 指定使用 [**ID3D12CommandList2：： WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2)所寫入的立即值和目的地位址。 |

## <a name="related-topics"></a>相關主題

* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)