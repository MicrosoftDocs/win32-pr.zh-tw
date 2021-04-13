---
description: 本文包含使用 Direct3D 12 影片 Api 的一般指引。
ms.assetid: ''
title: Direct3D 12 影片總覽
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: b21587f2784b34131da9c050655b6f3fbe43582d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510802"
---
# <a name="direct3d-12-video-overview"></a>Direct3D 12 影片總覽

本文包含使用 Direct3D 12 影片 Api 的一般指引。

## <a name="about-direct3d-12-video"></a>關於 Direct3D 12 影片

Direct3D 12 video 介面提供一種新的方式，讓應用程式能夠執行影片解碼和流程。 Direct3D 12 介面與先前的 Direct3D 11 介面不同，因為它是設計成與 Direct3D 12 準則和樣式一致，其中包括下列各項：

- 提供開發人員更多控制權
 - 配置硬體可存取的記憶體
 - 用來產生 & 提交命令的 CPU 執行緒
   - 獨立產生和提交
   - 非封鎖
 - 排程硬體工作
- 涵蓋現有的功能，包括大部分的 Direct3D 11 影片功能，但同時保持簡單且容易使用
- 主要 Direct3D 12 應用程式等於或優於 Direct3D 11 的強大功能和效能
- 與其他 Direct3D 12 Api 的一致性
- 與現有圖形 Api 的互通性


## <a name="video-decoding"></a>影片解碼

下列各節說明執行 Direct3D 12 影片解碼時所牽涉到的一些工作。

### <a name="query-for-decoding-capabilities"></a>查詢解碼功能

呼叫 [ID3D12VideoDevice：： CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) ，以檢查 Direct3D 12 影片解碼作業的支援詳細資料。 傳遞 [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) 列舉的值，以指定您要求支援資訊的功能。

### <a name="create-the-video-decoder"></a>建立影片解碼

呼叫 [ID3D12VideoDevice：： CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) ，以建立 [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) 介面的實例。 此解碼會保存解碼會話的狀態，包括參考相關資料，例如動作向量。  如果發生解析度變更或 [MaxDecodePictureBufferCount](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) 變更，則會重新建立解碼器物件。 解碼寬度和高度會在任何尺規之前指定原生串流解析度。  最大解碼圖片緩衝區 (DPB) 計數會指定最大的 DPB 計數，而不需要重新建立影片解碼器。

您可以使用此解碼器來記錄多個命令清單中的命令，但是一次只能與一個命令清單相關聯。  應用程式會負責同步處理對解碼器的存取。

### <a name="create-the-video-decoder-heap"></a>建立影片解碼堆積 

呼叫 [ID3D12VideoDevice：： CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) ，以建立 [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) 介面的實例。 此物件包含解析相依的驅動程式資源和狀態。

### <a name="decoding-a-frame"></a>解碼框架

影片處理作業的所有輸入和輸出參數都會組織成輸入參數結構、 [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)和輸出參數結構， [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)。
應用程式會管理參考框架，因此需要為每個解碼作業設定參考框架。
當命令清單記錄妥當時，請在 video 命令佇列上呼叫 [ID3D12CommandQueue：： ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) ，以將畫面解碼提交給 GPU。


### <a name="enabling-decoder-output-conversions"></a>啟用解碼器輸出轉換
如果此解碼器支援轉換，請適當地填滿 [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) 結構，以啟用所需的轉換。 所需輸出的格式和解析度與解碼器的原生輸出，會透過色彩空間和轉換參數中指定之解析度的差異進行通訊。

##  <a name="querying-decoding-status"></a>查詢解碼狀態 
使用 [ID3D12VideoDecodeCommandList：： BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) 和 [ID3D12VideoDecodeCommandList：： EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) 方法來查詢解碼作業的狀態。

[D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)結構是用來描述影片解碼統計資料。 若要取得此結構的實例，請呼叫 [ID3D12VideoDecodeCommandList：： EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery)，並傳入 [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type)的堆積查詢類型值。 請注意，此查詢不會使用 [ID3D12VideoDecodeCommandList：： BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery)。

## <a name="video-processing"></a>影片處理

Direct3D 12 影片 Api 採用簡化的影片處理方法，消除了未廣泛使用的 Direct3D 11 功能，並移除跨裝置強制執行之功能的功能檢查。 影片處理的列舉程式已消除。 請改為呼叫 [ID3D12VideoDevice：： CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) ，以允許應用程式識別視頻處理器的功能。 所需的影片、交錯、身歷聲格式和速率會提供為 **CheckFeatureSupport** 的輸入。

### <a name="removed-capabilities"></a>已移除功能

Direct3D 12 影片處理不支援下列來自 Direct3D 11 的功能：
- 自訂費率。  相反地， [ID3D12VideoProcessCommandList：:P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) 命令錄製期間提供輸入和輸出速率。
- 現在只有兩種可用的去交錯模式： [BOB](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) 和 [CUSTOM](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags)。 已消除其他模式。 自訂是硬體廠商提供的高品質去交錯模式。
- 不再支援 [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) 中的所有選用身歷聲格式。 相反地，如果支援身歷聲， [nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)、 [水準](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)、 [垂直](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)和 [分隔](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) 是所有硬體裝置的必要項。
- [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps)或[D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps)沒有對等專案。 相反地，輸入和輸出格式是建立視頻處理器的引數，而且在這段時間，如果影片處理器可以或無法以指定的格式執行作業，則應該是已知的。 [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags)用來指出是否可以使用自動處理功能。
- [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)沒有對等專案。
- [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps)沒有對等專案。
- 從身歷聲轉換成 mono 時，我們假設基準視圖是0。
- Direct3D 12 影片處理不支援將 mono 轉換成身歷聲，且不支援 mono 位移。 


### <a name="creating-a-video-processor"></a>建立視頻處理器

呼叫 [ID3D12VideoDevice：： CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) 來建立 [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor)的實例。 影片處理器會保存影片處理會話的狀態，包括必要的中繼記憶體、快取的處理資料，或其他暫存的工作空間。 影片處理器建立引數指定在 ID3D12VideoProcessCommandList1 執行或可使用的作業 [：:P rocessframes1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) time。  用來執行影片程式作業的驅動程式配置 (例如，中繼) 會在視頻處理器建立時配置。  使用 [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) 來提前判斷視頻處理器的配置大小。

影片處理器只能用來記錄多個命令清單中的命令，但是一次只能與一個命令清單相關聯。  應用程式會負責同步處理對視頻處理器的存取。  應用程式也必須針對影片 procoessor 記錄影片處理命令，其順序是在 GPU 上執行。

影片處理作業的所有輸入和輸出引數都會組織成輸入引數結構、 [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)和輸出引數結構， [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)。 應用程式必須呼叫 [ID3D12VideoProcessCommandList：:P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) 來記錄要執行的影片處理作業。 

錄製命令清單時，請在 video 命令佇列上呼叫 [ID3D12CommandQueue：： ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) ，以將畫面格處理提交給 GPU。


## <a name="tiers"></a>階層

Direct3D 12 video 定義了將硬體裝置的功能分組的階層，讓應用程式可以使用較少的程式碼路徑來滿足各種不同的硬體。 階層是以 [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) 列舉來指定。

在所有層級中，將可使用下列各項：

- 不需要在解析變更時重新取得解碼器。 只有在解析變更時才需要重新建立解碼器堆積。
- 所有的參考框架都會由應用程式管理。 這可讓系統儲存記憶體，因為我們不需要在某些階層中配置最大的 DPBs，在每個層級的解碼器建立時，並讓應用程式在解決方案變更案例中具有彈性。

請注意，這些層級為超集合。 應用程式可能會決定進行第1層，但不使用較高層級的功能，但可能無法提供最佳效能。 如需與不同層級相關聯之功能的詳細資訊，請參閱 [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier)。

## <a name="reference-frames"></a>參考框架

使用 Direct3D 12 影片時，會明確傳遞參考框架。 這可在我們解碼框架時，清楚使用紋理或材質陣列的陣列。 使用應用程式做為參考時，不需要傳遞完全相同的資源控制碼;例如，可能會決定將某個資源複製到另一個資源，然後傳遞複本而不是原始的資源。 驅動程式仍會使用 DXVA *RefFrameList* 和 *CurrPic* 索引來儲存每個已解碼框架的相關資料。


## <a name="directx-12-fences"></a>DirectX 12 的時限

在 DirectX 12 中，應用程式會負責同步處理其緩衝區的存取。 在解碼案例中，需要將圍牆新增至輸入緩衝區和輸出緩衝區。 每個隔離都有與其相關聯的值，並用於 CPU 和硬體引擎的同步處理。 如需詳細資訊，請參閱 [使用資源阻礙在 Direct3D 12 中同步處理資源狀態](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)。

一般的實作為每個輸入緩衝區都會有一個隔離。 在輸入緩衝區的情況下，可能會在整個解碼程式完成之前，可以使用緩衝區。 系統會忽略此案例，並假設在解碼完成時可使用輸入緩衝區。
執行通常也會有每個輸出緩衝區的範圍。 比方說，如果將輸出傳送至組合器，就需要有一個範圍，當該框架的呈現方式最後完成時，就會發出信號，表示該輸出再次可供解碼器使用。


## <a name="related-topics"></a>相關主題

<dl> <dt>
[Direct3D 12 影片 api](direct3d-12-video-apis.md) 
[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </dl>

 

 
