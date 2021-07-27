---
title: 核心列舉
description: 下列列舉是在 d3d12 中宣告。
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 31cac62c8dfa6b1126d8ff2a7c134490c0c58038
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436223"
---
# <a name="core-enumerations"></a>核心列舉

下列列舉是在 d3d12 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題和描述 |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)。 指定根簽章版面配置的版本。 |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model)。 指定著色器模型。 |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op)。 定義指定轉譯/計算 GPU 作業的常數。 |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode)。 定義常數，指定要套用至後續提交之 GPU 工作的動態優化層級。 |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend)。 指定 blend 因數，這會 lambert 圖元著色器和轉譯目標的值。 |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op)。 指定 RGB 或 Alpha 混合作業。 |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags)。 識別如何查看緩衝區資源。 |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags)。 識別緩衝區資源的未排序存取視圖選項。 |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags)。 從深度樣板視圖中指定要清除的內容。 |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable)。 識別轉譯目標的每個圖元元件在混合期間可以寫入。 |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags)。 用來判斷哪些類型的命令清單可以支援各種作業。 |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)。 指定命令清單的類型。 |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags)。 指定要在建立命令佇列時使用的旗標。 |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority)。 定義命令佇列的優先權層級。 |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func)。 指定比較選項。 |
| [**D3D12_CONSER加值稅IVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode)。 識別是否開啟或關閉保守的點陣化。 |
| [**D3D12_CONSER加值稅IVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier)。 識別保守的點陣化層級。 |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property)。 指定堆積的 CPU 頁面屬性。 |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)。 指定介面卡節點間的共用層級，例如第1層模擬、第1層或第2層。  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode)。 指定不繪製面向特定方向的三角形。 |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)。 指定由 [**ID3D12DebugDevice1：： SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter)和 [**ID3D12DebugDevice1：： GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter)的 *.pdata* 參數所指向之記憶體的資料類型。 |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask)。 識別用來寫入深度資料之深度樣板緩衝區的部分。 |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)。 指定堆積的選項。 |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type)。 指定描述項堆積的類型。  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags)。 以根簽章1.1 描述來指定描述元和其所參考資料的變動性，這可啟用某些驅動程式優化。 |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)。 指定範圍，如此一來，例如，如果部分描述中繼資料表有100著色器資源檢視 (SRVs) 該範圍可以在一個專案中宣告，而不是100。  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type)。 定義指定轉譯/計算 GPU 作業的常數。 |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement)。 定義 [ID3D12DeviceRemovedExtendedDataSettings 介面](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) (所使用的常數，) 指定如何啟用個別裝置移除擴充資料 (dr) 功能。 |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags)。 定義用於 [D3D12_DEVICE_REMOVED_EXTENDED_DATA 結構](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) 中的常數，以指定 Direct3D 執行時間的控制項旗標。 |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version)。 定義常數，可指定 [D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA 結構](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data)所使用 (dr) 的已移除擴充資料的版本。 |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension)。 指定如何存取深度範本視圖中使用的資源。 |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags)。 指定深度樣板的視圖選項。 |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature)。 目前圖形驅動程式支援的 Direct3D 12 功能選項。  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags)。 指定範圍選項。  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode)。 指定呈現三角形時要使用的填滿模式。 |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter)。 指定紋理取樣期間的篩選選項。 |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)。 指定縮減篩選的類型。  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type)。 指定放大或縮制取樣器篩選的類型。  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1)。 指定支援所提供格式的資源。 |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2)。 指定提供的格式支援哪些未排序的資源選項。 |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states)。 定義旗標，以指定與圖形命令清單相關的狀態。 值可以是位 OR。 |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)。 指定堆積選項，例如堆積是否可包含紋理，以及資源是否會在介面卡間共用。  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier)。 定義常數，指定堆積序列化支援。 |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type)。 指定堆積的類型。 當常駐時，堆積位於具有特定 CPU 快取屬性的特定實體記憶體集區中。  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)。 使用三角形區域基本拓撲時，頂點位置會被視為連續三角形帶的頂點。 有一個特殊的索引值，表示要在區域（剪下索引值）中發生不連續的情況。 此列舉會列出支援的剪下值。  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)。 指定間接參數的型別。  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification)。 識別輸入位置中包含的資料類型。 |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state)。 定義常數，指定存留期追蹤物件的存留期狀態。 |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op)。 指定要為呈現目標設定的邏輯作業。 |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action)。 定義常數，指定應如何使用較早的工作負載檢測結果來完成。 |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool)。 指定堆積的記憶體集區。 |
| [**D3D12_MESH_SHADER_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_mesh_shader_tier)。 定義常數，指定網格和放大著色器支援。 |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags)。 定義常數，指定中繼命令的參數旗標。 值可以是位 OR。 |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage)。 定義常數，指定中繼命令的參數階段。 |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type)。 定義常數，指定中繼命令之參數的資料類型。 |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags)。 針對多個圍牆指定多個等候旗標。 |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags)。 指定決定品質層級的選項。  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)。 控制管線狀態的旗標。  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)。 指定管線狀態資料流程描述中子物件的類型。 |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op)。 指定要套用的 predication 作業。  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)。 指定管線如何解讀幾何或輪廓著色器輸入基本專案。 |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier)。 指定介面卡提供之可程式化範例位置的支援層級。 |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags)。 定義常數，指定受保護的資源會話旗標。 |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags)。 定義常數，指定受保護的資源會話支援。 |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status)。 定義指定受保護會話狀態的常數。 |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type)。 指定要建立之查詢堆積的型別。 |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type)。 指定查詢的類型。 |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags)。 傳遞至 [**TraceRay**](./traceray-function.md) 函式的旗標，可覆寫透明度、剔除和早期輸出行為。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags)。 指定 raytracing 加速結構組建的旗標。 使用這個列舉中的值，以及提供加速結構建立作業之輸入的 [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) 結構。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode)。 指定呼叫 [**CopyRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure)時所執行的複製作業類型。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type)。 指定可透過呼叫 [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) 和 [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure)抓取的加速結構後置資訊類型。 |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type)。 指定 raytracing 加速結構的型別。 |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags)。 指定 [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) 結構中 raytracing 幾何的旗標。 |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type)。 指定用於 raytracing 的幾何類型。 使用這個列舉中的值來指定 [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc)中的幾何類型。 |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags)。 Raytracing 加速結構實例的旗標。 這些旗標可以用來覆寫個別實例的 [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) 。 |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier)。 指定圖形裝置上的光線追蹤支援層級。 |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type)。 指定在轉換成轉譯行程時，將應用程式提供給指定之資源 (s) 的存取類型。 |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type)。 指定在從轉譯行程轉換時，將應用程式提供給指定之資源 (s) 的存取類型。 |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags)。 指定轉譯傳遞的本質;例如，它是暫止或繼續的轉譯階段。 |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags)。 搭配 EnqueueMakeResident 函式使用，以選擇當超過記憶體預算時，如何繼續進行落地作業。 |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority)。 指定廣泛的主機優先權值區，適合用來快速建立應用程式優先權配置。 |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode)。 指定解析操作。 |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags)。 用於設定分割資源阻礙的旗標。  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type)。 指定資源使用) 描述中 (轉換的資源屏障類型。 |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier)。 識別正在使用的資源系結層。  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)。 識別正在使用的資源類型。 |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags)。 指定使用資源的選項。  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier)。 指定硬體和驅動程式支援的資源堆積層。  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)。 指定資源的使用方式相關資源的狀態。  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags)。 指定根簽章1.1 描述中描述項所參考之資料的變動性，可啟用某些驅動程式優化。 |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type)。 指定根簽章位置的類型。  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)。 指定根簽章版面配置的選項。  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension)。 識別要視為呈現目標的資源類型。 |
| [**D3D12_SAMPLER_FEEDBACK_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_sampler_feedback_tier)。 定義指定取樣器意見支援的常數。 |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags)。 描述目前圖形驅動程式中著色器快取的支援層級。 |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping)。 指定著色器資源檢視 (SRV) 如何路由記憶體。  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support)。 描述目前圖形驅動程式中著色器的最小精確度支援選項。  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)。 指定可存取指定根簽章位置內容的著色器。 |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier)。 定義常數，指定跨 API 共用支援層。 |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension)。 識別將視為著色器資源的資源類型。 |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color)。 指定靜態取樣器的框線色彩。  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op)。 識別可在深度樣板測試期間執行的樣板作業。 |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode)。 識別用來解析材質範圍外之材質座標的技巧。  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type)。 指定所要進行的材質複製類型。 |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout)。 指定材質版面配置選項。  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags)。 指定如何複製磚。  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags)。 指定如何執行磚對應作業。  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags)。 指定圖格對應的範圍。  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)。 識別支援的並排資源層級。  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension)。 識別未排序的存取視圖選項。 |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags)。 指定 view 實例的選項。 |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier)。 指出支援 view 實例的層級層級。 |
| [**D3D12_WAVE_MMA_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_wave_mma_tier)。 定義常數，指定 WaveMMA (wave_matrix) 作業的支援層級。 |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode)。 指定 **WriteBufferImmediate** 操作所使用的模式。 |

## <a name="related-topics"></a>相關主題

* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
