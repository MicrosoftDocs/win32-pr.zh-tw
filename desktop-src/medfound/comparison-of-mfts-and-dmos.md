---
description: 媒體基礎轉換 (MFTs) 是首次以 DirectX 媒體物件（ (DMOs) ）引進的轉換模型演進。
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: MFT 和 DMO 的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026049"
---
# <a name="comparison-of-mfts-and-dmos"></a>MFT 和 DMO 的比較

媒體基礎轉換 (MFTs) 是首次以 DirectX 媒體物件（ (DMOs) ）引進的轉換模型演進。 本主題摘要說明 MFTs 與 DMOs 有何不同的主要方式。 如果您已經熟悉 SQL-DMO 介面，或者您想要將現有的 SQL-DMO 轉換成 MFT，請閱讀本主題。

本主題包含下列幾節：

-   [資料流程數目](#number-of-streams)
-   [格式協調](#format-negotiation)
-   [串流](#streaming)
    -   [配置資源](#allocating-resources)
    -   [處理資料](#processing-data)
    -   [沖洗](#flushing)
    -   [資料流程不連續](#stream-discontinuities)
-   [其他差異](#miscellaneous-differences)
-   [旗標](#flags)
    -   [ProcessInput 旗標](#processinput-flags)
    -   [ProcessOutput 旗標](#processoutput-flags)
    -   [GetInputStatus 旗標](#getinputstatus-flags)
    -   [GetOutputStatus 旗標](#getoutputstatus-flags)
    -   [GetInputStreamInfo 旗標](#getinputstreaminfo-flags)
    -   [GetOutputStreamInfo 旗標](#getoutputstreaminfo-flags)
    -   [SetInputType/SetOutputType 旗標](#setinputtypesetoutputtype-flags)
-   [錯誤碼](#error-codes)
-   [建立混合式 SQL-DMO/MFT 物件](#creating-hybrid-dmomft-objects)
-   [相關主題](#related-topics)

## <a name="number-of-streams"></a>資料流程數目

A 的資料流程有固定的資料流程，而 MFT 可支援動態的資料流程數目。 用戶端可以新增輸入資料流程，而 MFT 可以在處理期間新增輸出資料流程。 但是，不需要 MFTs 就能支援動態資料流。 一個 MFT 可以有固定數目的資料流程，就像說的一樣。

下列方法可用來在 MFT 上支援動態資料流：

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform：:D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

此外， [**IMFTransform：:P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) 方法會定義用於加入或移除輸出資料流程的行為。

因為 DMOs 有固定的資料流程，所以會使用以零為基底的索引值來識別該的資料流程。 相反地，MFTs 會使用不一定會對應到索引值的資料流程識別碼。 這是因為 MFT 上的資料流程數目可能會變更。 例如，可能會移除資料流程0，並將 stream 1 保留為第一個資料流程。 不過，具有固定資料流程的 MFT 應該會觀察與 DMOs 相同的慣例，並將索引值用於資料流程識別碼。

## <a name="format-negotiation"></a>格式協調

MFTs 使用 [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) 介面來描述媒體類型。 否則，使用 MFTs 的格式協商可在與 DMOs 相同的基本原則上運作。 下表列出 DMOs 的格式協商方法，以及 MFTs 的對應方法。



| SQL-DMO 方法                                                                        | MFT 方法                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>串流

如同 DMOs，MFTs 會透過呼叫 [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) 和 [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) 方法來處理資料。 以下是在串流處理資料時，SQL-DMO 和 MFT 程式之間的主要差異。

### <a name="allocating-resources"></a>配置資源

MFTs 沒有與 FreeStreamingResources 搭配使用的 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) 和 [**IMediaObject：： DMOs**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) 方法。 若要有效率地處理資源的配置和解除配置，MFT 可以在 [**IMFTransform：:P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 方法中回應下列訊息：

-   [**MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流**](mft-message-notify-begin-streaming.md)
-   [**MFT \_ 訊息 \_ 通知 \_ 開始 \_ \_ 資料流程**](mft-message-notify-start-of-stream.md)

此外，用戶端可以藉由呼叫 [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 與下列訊息來發出資料流程的開始和結束信號：

-   [**MFT \_ 訊息 \_ 通知 \_ 結束 \_ \_ 資料流程**](mft-message-notify-end-of-stream.md)
-   [**MFT \_ 訊息 \_ 通知 \_ 結束 \_ 資料流程**](mft-message-notify-end-streaming.md)

這兩個訊息沒有完全相同的專案。

### <a name="processing-data"></a>處理資料

MFTs 使用媒體範例來保存輸入和輸出資料。 媒體範例會公開 [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) 介面，並包含下列資料：

-   時間戳記和持續時間。
-   包含每個範例資訊的屬性。 如需屬性的清單，請參閱 [範例屬性](sample-attributes.md)。
-   零或多個媒體緩衝區。 每個媒體緩衝區都會公開 [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。

[**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)介面類別似于 sql-dmo **IMediaBuffer** 介面。 若要存取基礎記憶體緩衝區，請呼叫 [**IMFMediaBuffer：： Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)。 這個方法大約相當於 DMOs 的 [**IMediaBuffer：： GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) 。

若是未壓縮的影片資料，媒體緩衝區可能也支援 [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。 處理未壓縮影片 (為輸入或輸出) 的 MFT 應該準備好在緩衝區公開時使用 **IMF2DBuffer** 介面。 如需詳細資訊，請參閱 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)。

媒體基礎提供一些 [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)的標準執行，因此通常不需要撰寫您自己的實作為。 若要從媒體基礎緩衝區建立 SQL-DMO 緩衝區，請呼叫 [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer)。

### <a name="flushing"></a>沖洗

MFTs 沒有 [**Flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) 方法。 若要排清 MFT，請使用 [**mft \_ 訊息 \_ 命令 \_ 清除**](mft-message-command-flush.md)訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 。

### <a name="stream-discontinuities"></a>資料流程不連續

MFTs 沒有不連續的 [**方法。**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) 若要以信號表示資料流程中的中斷，請在輸入範例上設定 MFSampleExtension 不中斷屬性。 [**\_**](mfsampleextension-discontinuity-attribute.md)

## <a name="miscellaneous-differences"></a>其他差異

以下是 MFTs 和 DMOs 之間的一些額外微小差異。

-   下列的 SQL-DMO 方法沒有適用于 MFT 的對應專案：
    -   [**IMediaObject：： Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   不需要 MFTs 就能支援匯總。
-   MFTs 支援稱為 *清空* 的作業。 清空的目的是要處理保留在 MF 中的任何資料，而不提供任何更多輸入資料給 MFT (例如，在資料流程) 的結尾。 若要清空 MFT，請使用 [**mft \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md)訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 。 如需詳細資訊，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。
-   MFTs 可以有屬性，包括每個資料流程屬性。 使用下列方法從 MFT 取得屬性：

    -   [**IMFTransform：： GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   MFTs 可以處理事件。 若要將事件傳送到 MFT，請呼叫 [**IMFTransform：:P rocessevent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent)。 MFT 可透過 [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) 方法，將事件傳送給用戶端。 如需詳細資訊，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。

## <a name="flags"></a>Flags

下表列出各種的 SQL-DMO 旗標及其對等專案。 只要每個 a 的旗標直接對應到 MFT 旗標，這兩個旗標都有相同的數值。 不過，有些等旗標沒有完全相同的 MFT 對等專案，反之亦然。

### <a name="processinput-flags"></a>ProcessInput 旗標

DMOs： [**\_ Sql-dmo \_ 輸入 \_ 資料 \_ 緩衝區 \_ 旗標**](/previous-versions/windows/embedded/aa451599(v=msdn.10))列舉。

MFTs：沒有對等的列舉。



| SQL-DMO 旗標                                  | MFT 旗標                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **SQL-DMO \_ 輸入 \_ 資料 \_ BUFFERF \_ SYNCPOINT**  | 沒有對等的旗標。 請改為在範例上設定 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性。 |
| **SQL-DMO \_ 輸入 \_ 資料 \_ BUFFERF \_ 時間**       | 沒有對等的旗標。 請改為在範例上呼叫 [**IMFSample：： SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) 。                                  |
| **SQL-DMO \_ 輸入 \_ 資料 \_ BUFFERF \_ TIMELENGTH** | 沒有對等的旗標。 請改為在範例上呼叫 [**IMFSample：： SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) 。                          |



 

### <a name="processoutput-flags"></a>ProcessOutput 旗標

DMOs： [**\_ Sql-dmo \_ 進程 \_ 輸出 \_ 旗標**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags)列舉。

MFTs： [**\_ MFT \_ 進程 \_ 輸出 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags)列舉。



| SQL-DMO 旗標                                            | MFT 旗標                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_ \_ \_ \_ 當 \_ 沒有 \_ 緩衝區時，會捨棄進程輸出** | **\_ \_ \_ \_ 當 \_ 沒有 \_ 緩衝區時，MFT 進程輸出捨棄** |



 

DMOs： [**\_ Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區 \_ 旗標**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags)列舉。


MFTs： [**\_ MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags)列舉。



| SQL-DMO 旗標                                   | MFT 旗標                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ SYNCPOINT**  | 沒有對等的旗標。 請改為檢查範例上的 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性。 |
| **SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 時間**       | 沒有對等的旗標。 請改為在範例上呼叫 [**IMFSample：： GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 。                                        |
| **SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ TIMELENGTH** | 沒有對等的旗標。 請改為在範例上呼叫 [**IMFSample：： GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) 。                                |
| **SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 未完成** | **MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 未完成**                                                                                                           |
| 沒有對等的旗標。                        | **MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 格式 \_ 變更**                                                                                                       |
| 沒有對等的旗標。                        | **MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 資料流程 \_ 結束**                                                                                                          |
| 沒有對等的旗標。                        | **MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 無 \_ 範例**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>GetInputStatus 旗標

DMOs： **\_ Sql-dmo \_ 輸入 \_ 狀態 \_ 旗標** 列舉。

MFTs： [**\_ MFT \_ 輸入 \_ 狀態 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags)列舉。



| SQL-DMO 旗標                              | MFT 旗標                             |
|---------------------------------------|--------------------------------------|
| **SQL-DMO \_ 輸入 \_ STATUSF \_ 接受 \_ 資料** | **MFT \_ 輸入 \_ 狀態 \_ 接受 \_ 資料** |



 

### <a name="getoutputstatus-flags"></a>GetOutputStatus 旗標

DMOs：沒有對等的列舉。

MFTs： [**\_ MFT \_ 輸出 \_ 狀態 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags)列舉。



| SQL-DMO 旗標            | MFT 旗標                               |
|---------------------|----------------------------------------|
| 沒有對等的旗標。 | **可用的 MFT \_ 輸出 \_ 狀態 \_ 範例 \_** |



 

### <a name="getinputstreaminfo-flags"></a>GetInputStreamInfo 旗標

DMOs： [**\_ Sql-dmo \_ 輸入 \_ 資料流程 \_ 資訊 \_ 旗標**](/previous-versions/windows/embedded/aa451600(v=msdn.10))列舉。

MFTs： [**\_ MFT \_ 輸入 \_ 資料流程 \_ 資訊 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags)列舉。



| SQL-DMO 旗標                                             | MFT 旗標                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **SQL-DMO \_ 輸入 \_ STREAMF \_ 完整 \_ 範例**              | **MFT \_ 輸入 \_ 資料流程的 \_ 完整 \_ 範例**              |
| **SQL-DMO \_ 輸入 \_ STREAMF \_ \_ \_ 每個緩衝區一個樣本 \_** | **\_ \_ \_ \_ \_ 每個 \_ 緩衝區的 MFT 輸入資料流程單一範例** |
| **SQL-DMO \_ 輸入 \_ STREAMF \_ 固定 \_ 樣本 \_ 大小**         | **MFT \_ 輸入 \_ 資料流程 \_ 固定 \_ 樣本 \_ 大小**         |
| **SQL-DMO \_ 輸入 \_ STREAMF \_ 保留 \_ 緩衝區**              | **MFT \_ 輸入 \_ 資料流程 \_ 持有 \_ 緩衝區**              |
| 沒有對等的旗標。                                  | **MFT \_ 輸入 \_ 資料流程 \_ \_ 未 \_ ADDREF**           |
| 沒有對等的旗標。                                  | **MFT \_ 輸入 \_ 資料流程 \_ 移除**                   |
| 沒有對等的旗標。                                  | **選擇的 MFT \_ 輸入 \_ 資料流程 \_**                    |



 

### <a name="getoutputstreaminfo-flags"></a>GetOutputStreamInfo 旗標

DMOs： [**\_ Sql-dmo \_ 輸出 \_ 資料流程 \_ 資訊 \_ 旗標**](/previous-versions/ms806053(v=msdn.10))列舉。

MFTs： [**\_ MFT \_ 輸出 \_ 資料流程 \_ 資訊 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)列舉。



| SQL-DMO 旗標                                              | MFT 旗標                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **SQL-DMO \_ 輸出 \_ STREAMF \_ 完整 \_ 範例**              | **MFT \_ 輸出 \_ 資料流程的 \_ 完整 \_ 範例**              |
| **SQL-DMO \_ 輸出 \_ STREAMF \_ \_ \_ 每個 \_ 緩衝區的單一樣本** | **\_ \_ \_ \_ \_ 每個 \_ 緩衝區的 MFT 輸出資料流程單一範例** |
| **SQL-DMO \_ 輸出 \_ STREAMF \_ 固定 \_ 樣本 \_ 大小**         | **MFT \_ 輸出 \_ 資料流程 \_ 固定 \_ 樣本 \_ 大小**         |
| **SQL-DMO \_ 輸出 \_ STREAMF \_ DISCARDABLE**                 | **MFT \_ 輸出 \_ 資料流程 \_ DISCARDABLE**                 |
| **SQL-DMO \_ 輸出 \_ STREAMF \_ 選擇性**                    | **MFT \_ 輸出 \_ 資料流程 \_ 選擇性**                    |
| 沒有對等的旗標。                                   | **MFT \_ 輸出 \_ 資料流程 \_ 提供 \_ 範例**           |
| 沒有對等的旗標。                                   | **MFT \_ 輸出 \_ 資料流程 \_ 可以 \_ 提供 \_ 範例**       |
| 沒有對等的旗標。                                   | **MFT \_ 輸出 \_ 資料流程 \_ 延遲 \_ 讀取**                  |
| 沒有對等的旗標。                                   | **MFT \_ 輸出 \_ 資料流程 \_ 移除**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>SetInputType/SetOutputType 旗標

DMOs： [**\_ Sql-dmo \_ 集合 \_ 類型 \_ 旗標**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags)列舉。

MFTs： [**\_ MFT \_ 集合 \_ 類型 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags)列舉。



| SQL-DMO 旗標                        | MFT 旗標                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **SQL-DMO \_ SET \_ TYPEF \_ TEST \_** | **\_ \_ \_ 僅限設定類型測試 \_ 的 MFT**                                                       |
| **SQL-DMO \_ 設定 \_ TYPEF \_ CLEAR**      | 沒有對等的旗標。 相反地，請將媒體類型設為 **Null** 以清除媒體類型。 |



 

## <a name="error-codes"></a>錯誤碼

下表說明如何將 SQL-DMO 錯誤碼對應至 MFT 錯誤碼。 混合式 MFT/SQL-DMO 物件應從 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 方法和來自 [**IMFTRANSFORM**](/windows/win32/api/mftransform/nn-mftransform-imftransform) 方法的 MFT 錯誤碼傳回 sql-dmo 錯誤碼。 在標頭檔 MediaErr 中定義了 SQL-DMO 錯誤碼。 在標頭檔 mferror 中定義了 MFT 錯誤碼。



| SQL-DMO 錯誤碼                  | MFT 錯誤碼                       |
|---------------------------------|--------------------------------------|
| **SQL-DMO \_ E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **SQL-DMO \_ E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **SQL-DMO \_ E \_ NOTACCEPTING**        | **MF \_ E \_ NOTACCEPTING**              |
| **\_E E \_ 沒有 \_ 其他 \_ 專案**     | **MF \_ E \_ 沒有 \_ 其他 \_ 類型**           |
| **\_E E \_ 類型 \_ 不 \_ 接受** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_E E \_ 類型 \_ 未 \_ 設定**      | **\_ \_ \_ \_ 未設定 MF E 轉換 \_ 類型** |



 

## <a name="creating-hybrid-dmomft-objects"></a>建立混合式 SQL-DMO/MFT 物件

[**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform)介面會以 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)為基礎，這是 DirectX 媒體物件 (DMOs) 的主要介面。 您可以建立可公開這兩個介面的物件。 不過，這可能會導致命名衝突，因為介面具有某些共用相同名稱的方法。 您可以透過下列兩種方式之一來解決這個問題：

解決方案1：在包含 MFT 函式的任何 .cpp 檔案頂端包含下列程式程式碼：

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

這會變更 [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) 介面的宣告，因此大部分的方法名稱前面都會加上 "MFT"。 因此， [**IMFTransform：:P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) 會變成 **IMFTransform：： MFTProcessInput**， [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) 會保留其原始名稱。 如果您要將現有的 SQL-DMO 轉換成混合式的 SQL-DMO/MFT，這項技術最有用。 您可以加入新的 MFT 方法，而不需要變更 SQL-DMO 方法。

解決方案2：使用 c + + 語法來區分繼承自多個介面的名稱。 例如，宣告 [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) 的 MFT 版本，如下所示：

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

宣告 [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) 的 sql-dmo 版本，如下所示：

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

如果您對物件內的方法進行內部呼叫，您可以使用這個語法，但是這樣做會覆寫方法的虛擬狀態。 從物件內部進行呼叫的更好方法如下：

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

如此一來，如果您從 **CMyHybridObject** 衍生另一個類別，並覆寫 CMyHybridObject：： IMediaObject：:P rocessinput 方法，則會呼叫正確的虛擬方法。 SQL-DMO 介面記載于 DirectShow SDK 檔中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 
