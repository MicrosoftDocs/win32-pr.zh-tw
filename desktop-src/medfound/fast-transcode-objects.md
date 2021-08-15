---
description: 本主題說明如何使用轉碼 API 來編碼媒體檔案。
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: 使用轉碼 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e32ea24ebd4803319713be5fe7789cf41c3a99733338bdfe5ad69baf7396bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742476"
---
# <a name="using-the-transcode-api"></a>使用轉碼 API

本主題說明如何使用轉碼 API 來編碼媒體檔案。

-   [概觀](#overview)
-   [建立媒體來源](#creating-a-media-source)
-   [建立轉碼設定檔](#creating-a-transcode-profile)
    -   [音訊屬性](#audio-attributes)
    -   [影片屬性](#video-attributes)
    -   [容器屬性](#container-attributes)
-   [建立轉碼拓撲](#creating-a-transcode-topology)
-   [正在執行編碼會話](#running-the-encoding-session)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

在使用轉碼 API 之前，應用程式必須具有下列資訊片段：

-   將會重新編碼之現有媒體檔案的路徑或 URL。
-   輸出檔的名稱。
-   輸出檔的容器類型，例如，「設定」或「Advanced 串流格式」 (ASF) 。
-   編碼格式。 此資訊包含描述編碼音訊和影片串流的媒體類型。

若要使用轉碼 API，應用程式會執行下列步驟。

1.  建立媒體來源以讀取原始檔。
2.  建立轉碼設定檔。 新增描述音訊串流、影片串流和檔案容器的屬性。
3.  使用轉碼設定檔來建立編碼拓撲。 如需拓撲的詳細資訊，請參閱 [關於拓撲](about-topologies.md)的詳細資訊 (。 ) 
4.  在 [媒體會話](media-session.md)上設定拓撲。
5.  啟動媒體會話，並等候 [MESessionEnded](mesessionended.md) 事件。

本主題的其餘部分將更詳細地描述這些步驟。

## <a name="creating-a-media-source"></a>建立媒體來源

媒體來源是讀取和剖析來源檔案的物件。 若要建立媒體來源，請使用 [來源解析程式](source-resolver.md)。 您可以 [使用來源解析程式](using-the-source-resolver.md)，在主題中找到範例程式碼。

## <a name="creating-a-transcode-profile"></a>建立轉碼設定檔

*轉碼設定檔* 說明用來編碼輸出檔的格式和設定。 轉碼設定檔包含三組屬性：

-   音訊屬性：描述目標音訊格式和音訊編碼器設定。
-   影片屬性：描述目標影片格式和影片編碼器設定。
-   容器屬性：定義檔案容器的類型，以及某些全域編碼設定。

若要建立轉碼設定檔，請呼叫 [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) 函數。 此函數會傳回 [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) 介面的指標。 初始設定檔物件是空的;它不包含任何屬性。 下一步是加入定義設定檔的屬性。

### <a name="audio-attributes"></a>音訊屬性

若要加入音訊資料流程的屬性，請呼叫 [**IMFTranscodeProfile：： SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)。 這些屬性會指定音訊串流的編碼方式。 如果輸出檔案不會包含音訊資料流程，請省略這些屬性。

音訊屬性分為兩類：

-   指定編碼資料流程格式的屬性
-   指定其他編碼參數的屬性。

格式屬性只是媒體類型的屬性，如 [音訊媒體類型](audio-media-types.md)一節中所述。 確切的格式屬性集會視編碼器而定。  ([在媒體基礎中查看支援的媒體格式](supported-media-formats-in-media-foundation.md)。 ) 以下是典型的音訊格式屬性清單：



| Format 屬性                                                                         | Description                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)                                           | 子型別。 請參閱 [音訊子類型 guid](audio-subtype-guids.md)。 |
| [MF \_ MT \_ 音訊 \_ 數目 \_ 通道](mf-mt-audio-num-channels-attribute.md)                   | 音訊頻道的數目。                                    |
| [\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_](mf-mt-audio-samples-per-second-attribute.md)      | 每秒音訊樣本數。                          |
| [MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊](mf-mt-audio-block-alignment-attribute.md)             | 區塊對齊。                                             |
| [\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_](mf-mt-audio-avg-bytes-per-second-attribute.md) | 每秒的平均位元組數目 (編碼的位速率) 。   |



 

已定義下列編碼參數。



| 編碼參數                                                             | Description                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ 轉碼 \_ 沒有 \_ 插入 \_ 編碼器](mf-transcode-donot-insert-encoder.md) | 防止轉碼 API 插入音訊串流的編碼器。 |
| [MF \_ 轉碼 \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | 指定裝置一致性範本。  (僅適用于 ASF 檔案。 )     |
| [MF \_ 轉碼 \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | 指定編碼品質與速度之間的取捨。                |



 

您必須設定格式屬性。 編碼參數是選擇性的。

若要尋找與編碼器相容的格式，其中一種方式就是呼叫 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) 函式。 所需的編碼器是由子類型所指定。 函數會傳回該編碼器的媒體類型集合。 您可以從清單中選取類型，並將屬性複製到設定檔。 如需使用這種方法的範例程式碼，請參閱 [教學課程：編碼 WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)檔案。

### <a name="video-attributes"></a>影片屬性

若要加入影片資料流程的屬性，請呼叫 [**IMFTranscodeProfile：： SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)。 這些屬性會指定影片串流的編碼方式。 如果輸出檔案不會包含影片資料流程，請省略這些屬性。

如同音訊屬性，影片屬性分為兩類：

-   指定編碼資料流程格式的屬性
-   指定其他編碼參數的屬性。

格式屬性是媒體類型的屬性，如 [影片媒體類型](video-media-types.md)一節中所述。 以下是典型的影片格式屬性清單：



| Format 屬性                                                       | Description                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)                         | 子型別。 請參閱 [影片子類型 guid](video-subtype-guids.md)。 |
| [MF \_ MT \_ 幀 \_ 速率](mf-mt-frame-rate-attribute.md)                  | 畫面播放速率。                                                  |
| [MF \_ MT \_ 框架 \_ 大小](mf-mt-frame-size-attribute.md)                  | 框架大小。                                                  |
| [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)            | 平均位元速率。                                            |
| [MF \_ MT \_ 圖元 \_ 外觀 \_ 比例](mf-mt-pixel-aspect-ratio-attribute.md) | 圖元外觀比例。                                          |



 

已定義下列編碼參數。



| 編碼參數                                                             | Description                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ 轉碼 \_ 沒有 \_ 插入 \_ 編碼器](mf-transcode-donot-insert-encoder.md) | 防止轉碼 API 插入影片串流的編碼器。 |
| [MF \_ 轉碼 \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | 指定裝置一致性範本。  (僅適用于 ASF 檔案。 )     |
| [MF \_ 轉碼 \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | 指定編碼品質與速度之間的取捨。                |



 

您必須設定格式屬性。 編碼參數是選擇性的。

### <a name="container-attributes"></a>容器屬性

容器屬性會定義輸出檔案的檔案層級特性。 若要設定容器屬性，請呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)。 會定義下列屬性。



| 屬性                                                                          | 描述                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ 轉碼 \_ 調整 \_ 設定檔](mf-transcode-adjust-profile.md)                  | 定義要用於轉碼拓撲的資料流程設定。 您可以設定旗標使用輸入來源設定，或使用自訂資料流程屬性。 |
| [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md)                     | 指定輸出檔的檔案格式，例如「數量」或「ASF」。 根據此值，會將適當的媒體接收器新增至拓撲。            |
| [MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸](mf-transcode-skip-metadata-transfer.md) | 指定是否將來源的中繼資料複製到輸出檔。                                                                               |
| [MF \_ 轉碼 \_ TOPOLOGYMODE](mf-transcode-topologymode.md)                       | 指定轉碼期間是否可使用以硬體為基礎的編解碼器。                                                                                |
| [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)          | 解除鎖定具有使用規定限制的編解碼器。 如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。              |



 

需要有 [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) 屬性。 其他容器屬性是選擇性的。

## <a name="creating-a-transcode-topology"></a>建立轉碼拓撲

轉碼拓撲是部分拓撲，其中包含媒體來源、適當的編解碼器和媒體接收器。 若要建立轉碼拓撲，請呼叫 [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) 函數。 此函式會採用下列參數作為輸入：

-   媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。
-   輸出檔的名稱。
-   轉碼設定檔之 [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) 介面的指標。

函數會傳回 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面的指標。

## <a name="running-the-encoding-session"></a>正在執行編碼會話

建立拓撲之後，您就可以開始將檔案編碼。 您可以在此時捨棄設定檔。

1.  呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立媒體會話。
2.  呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定媒體會話上的拓撲。
3.  呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 以開始編碼會話。
4.  等候 [MESessionEnded](mesessionended.md) 事件。
5.  呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉媒體會話。
6.  等候 [MESessionClosed](mesessionclosed.md) 事件。
7.  呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)。
8.  呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)。

在步驟3和4之間進行編碼所花費的時間大多很久。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉碼 API](transcode-api.md)
</dt> <dt>

[關於媒體會話](about-the-media-session.md)
</dt> </dl>

 

 



