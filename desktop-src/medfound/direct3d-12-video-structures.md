---
description: 本章節包含 Microsoft Direct3D 12 video API 結構的參考資訊。
ms.assetid: ''
title: Direct3D 12 影片結構
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 8914e8af9e21f3ee9a93e8bf9d122bec71483932
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314561"
---
# <a name="direct3d-12-video-structures"></a>Direct3D 12 影片結構

本章節包含 Microsoft Direct3D 12 video API 結構的參考資訊。

## <a name="in-this-section"></a>本節內容

| 主題                                                                                | 描述                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support)  | 抓取支援的配置檔案清單。|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats)  | 抓取支援的格式清單。|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_histogram)  | 當 D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM 指定的功能時，提供呼叫 ID3D12VideoDevice：： CheckFeatureSupport 的資料。|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles)  | 抓取支援的配置檔案清單。|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support)  | 捕獲影片解碼的支援資訊。|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_count)  | 捕獲影片延伸模組命令的數目。|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count)  | 針對指定的參數階段，抓取支援的參數數目。|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameters)  | 抓取指定參數階段的影片延伸模組命令參數清單。|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_size)  | 檢查影片擴充功能命令的配置大小。|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_support)  | 使用命令定義的輸入和輸出結構，抓取影片延伸模組命令支援。|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_commands)  | 從驅動程式抓取影片延伸模組命令的清單。|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)  | 當 D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR 指定的功能時，提供呼叫 ID3D12VideoDevice：： CheckFeatureSupport 的資料。 抓取影片編碼器的移動估計功能。|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources)  | 當 D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES 指定的功能時，提供呼叫 ID3D12VideoDevice：： CheckFeatureSupport 的資料。 抓取影片動作估計的受保護資源支援。|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_size)  | 描述影片動作估算器堆積的配置大小。|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_max_input_streams)  | 抓取視頻處理器支援的已啟用輸入資料流程數目上限。|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_reference_info)  | 抓取指定的交錯模式、篩選、速率轉換或自動處理功能所需的過去和未來參考框架數目。|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_support)  | 當 D3D12_FEATURE_VIDEO_PROCESS_SUPPORT 指定的功能時，提供呼叫 ID3D12VideoDevice：： CheckFeatureSupport 的資料。|
| [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)  | 代表呼叫 ID3D12VideoDecodeCommandList：： EndQuery 所叫用之影片解碼統計資料查詢的資料。|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input)  | 提供呼叫 ID3D12VideoEncodeCommandList：： ResolveMotionVectorHeap 的輸入資料。|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output)  | 接收 ID3D12VideoEncodeCommandList：： ResolveMotionVectorHeap 呼叫的輸出資料。|
| [D3D12_RESOURCE_COORDINATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resource_coordinate)  | 描述資源的座標。|
| [D3D12_VIDEO_DECODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_desc)  | 描述 ID3D12VideoDecoder。|
| [D3D12_VIDEO_DECODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc)  | 描述 ID3D12VideoDecoderHeap。|
| [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream)  | 代表從其解碼影片的壓縮位流。|
| [D3D12_VIDEO_DECODE_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_configuration)  | 描述影片解碼的設定。|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments)  | 指定解碼輸出轉換的參數。|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments1)  | 指定解碼輸出轉換的參數。|
| [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)  | 表示框架的解碼參數。|
| [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)  | 指定影片解碼作業的輸入資料流程參數。|
| [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)  | 表示單一元件的長條圖輸出緩衝區。|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)  | 指定影片解碼作業的輸出資料流程參數。|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1)  | 指定影片解碼作業的輸出資料流程參數。|
| [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames)  | 包含目前解碼作業的參考框架清單。|
| [D3D12_VIDEO_DECODE_SUB_SAMPLE_MAPPING_BLOCK](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_sub_sample_mapping_block)  | 定義適用于影片解碼之子樣本的加密位元組對應。|
| [D3D12_VIDEO_EXTENSION_COMMAND_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_desc)  | 描述影片延伸模組命令。|
| [D3D12_VIDEO_EXTENSION_COMMAND_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_info)  | 描述影片延伸模組命令。|
| [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_parameter_info)  | 描述影片擴充功能命令參數。|
| [D3D12_VIDEO_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_format)  | 定義資源內容描述的像素格式和色彩空間的組合。|
| [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_desc)  | 描述 ID3D12VideoMotionEstimator。 將此結構傳遞至 ID3D12VideoDevice1：： CreateVideoMotionEstimator，以建立 ID3D12VideoMotionEstimator 的實例。|
| [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input)  | 提供呼叫 ID3D12VideoEncodeCommandList：： EstimateMotion 的輸入資料。|
| [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)  | 接收 ID3D12VideoEncodeCommandList：： EstimateMotion 呼叫的輸出資料。|
| [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_vector_heap_desc)  | 描述 ID3D12VideoMotionEstimatorHeap。 將此結構傳遞至 ID3D12VideoDevice1：： CreateVideoMotionEstimatorHeap，以建立 ID3D12VideoMotionEstimatorHeap 的實例。|
| [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending)  | 指定影片處理的 Alpha 混合參數。|
| [D3D12_VIDEO_PROCESS_FILTER_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_filter_range)  | 定義影像篩選的支援值範圍。|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream)  | 包含視頻處理器 blend 功能的輸入資訊。|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)  | 指定傳遞至 ID3D12VideoCommandList 之輸入資料流程的輸入資料流程引數：:P rocessFrames。|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc)  | 指定影片處理作業的輸入資料流程參數。|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_rate)  | 提供資料流程速率的相關資訊。|
| [D3D12_VIDEO_PROCESS_LUMA_KEY](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_luma_key)  | 指定用於 luma 金鑰的設定。|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream)  | 表示影片處理命令的輸出資料流程。|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)  | 指定傳遞至 ID3D12VideoCommandList 之輸出的輸出資料流程引數：:P rocessFrames。|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  | 指定傳遞至 ID3D12VideoProcessCommandList 之輸出的輸出資料流程引數：:P rocessFrames。|
| [D3D12_VIDEO_PROCESS_REFERENCE_SET](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_reference_set)  | 包含執行影片處理所需的參考框架。|
| [D3D12_VIDEO_PROCESS_TRANSFORM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_transform)  | 指定影片處理的轉換參數。|
| [D3D12_VIDEO_SAMPLE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_sample)  | 描述圖片緩衝區的寬度、高度、格式和色彩空間。|
| [D3D12_VIDEO_SCALE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_scale_support)  | 描述影片 scaler 之輸出大小的支援調整範圍。|
| [D3D12_VIDEO_SIZE_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_size_range)  | 描述影片 scaler 支援的大小範圍。|



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 影片 Api](direct3d-12-video-apis.md)
</dt> </dl>

 

 



