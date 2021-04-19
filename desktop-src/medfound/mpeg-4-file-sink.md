---
description: MPEG-2 檔案接收會建立檔案。
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: MPEG-2 File 接收
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106982122"
---
# <a name="mpeg-4-file-sink"></a>MPEG-2 File 接收

MPEG-2 檔案接收會建立檔案。 如需有關檔案格式的詳細資訊，請參閱下列標準檔：

-   ISO/IEC 14496-12： *資訊技術--音訊-視覺化物件的編碼--第12部分： ISO 基底媒體檔案格式*
-   ISO/IEC 14496-14： *資訊技術--音訊-視覺化物件的編碼--第14部分：數量檔案格式*

> [!Note]  
>  (這些資源可能無法在某些語言及國家/地區使用。 ) 

 

MPEG-2 file 接收不會封裝編碼功能。

若要建立 MPEG-2 file 接收器，請呼叫 [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) 函式。 MPEG 4 檔案接收會透過 **QueryInterface** 公開下列介面：

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a>範例描述方塊

使用的是可擴充的容器格式。 使用規定規格不會定義固定的結構，以描述未設定的容器中的媒體類型。 相反地，它會定義物件階層，讓您針對每個格式定義自訂結構。 格式描述會儲存在每個資料流程 ( [stsd] ) 方塊的範例描述中。 [範例描述] 方塊包含範例專案的清單。 針對每個範例專案，4位元組的程式碼（類似于 FOURCC）會定義格式結構。

MPEG-2 檔案接收可以針對下列格式產生範例描述方塊：

-   H.264/AVC 影片
-   AAC 音訊
-   MP3 音訊

針對其他格式，則必須在每個資料流程的媒體類型中提供 [範例描述] 方塊。 若要指定 [範例描述] 方塊，請在媒體類型上設定下列屬性：



| 屬性                                                                     | 描述                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ MT \_ MPEG4 \_ 範例 \_ 說明](mf-mt-mpeg4-sample-description.md)      | 以二進位 blob 的形式包含範例描述方塊。                                                                                                         |
| [MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案](mf-mt-mpeg4-current-sample-entry.md) | 指定 [範例描述] 方塊中的哪些範例專案目前為使用中狀態。 (選擇性。)<br/> 目前，此值必須為零。<br/> |



 

在某些情況下，必須等到所有資料都經過編碼之後，才可以產生範例描述方塊。 例如，可能事先不知道平均位元速率等資訊。 在這種情況下，您可以使用 MPEG 4 檔案接收上的 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面來更新媒體類型。 這必須在媒體接收完成之前完成。

媒體類型通常是由上游編碼器所建立。 編碼器可透過動態格式變更，在串流期間產生新的媒體類型。 如需詳細資訊，請參閱 [動態格式變更](basic-mft-processing-model.md)。

## <a name="h264avc-video"></a>H.264/AVC 影片

MPEG-2 檔案接收支援具有基本影片串流的 AVC 資料流程版本，其序列參數設定 (SPS) 和 [範例描述] 方塊中所含的圖片參數集 (PPS) NALUs，如 ISO/IEC 14496 第15節5.1 節所定義。 File 接收不支援另一種將 SPS/PPS NALUs 儲存為個別參數集基本資料流程的方法。

MPEG-2 file 接收器可以產生範例描述方塊，但必須提供給 SPS 和 PPS NALUs。 藉由設定 [ [**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md) ] 屬性，在媒體類型中指定這項資訊。 屬性的值是 h.264 序列標頭。 Sequence 標頭必須由 SP 和 PPS NALUs （以3位元組或4位元組起始碼分隔）組成。

（選擇性）當您設定 file 接收時，您可以從初始媒體類型省略 [**MF \_ MT \_ MPEG \_ 順序 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md) 屬性。 在這種情況下，您必須稍後更新媒體類型以包含 sequence 標頭。

MPEG-2 檔案接收的 AVC bitstreams 需求如下：

-   位流必須符合 h.264 附錄 B 格式規格。 尤其是，NALUs 必須以3個位元組或4位元組起始碼分隔。
-   媒體範例必須包含對應至單一呈現時間的所有配量和資料 NALUs。
-   將 B 框架寫入至設定檔案時，您必須同時設定簡報時間戳記和解碼時間戳記。 如果 stream 有 B 框架，但未設定解碼時間戳記，則配置寫入器將會看到畫面上的時間，並會捨棄框架。 

## <a name="aac-audio"></a>AAC 音訊

針對 AAC 音訊，MPEG-2 檔案接收可以針對下列子類型產生範例描述方塊：

-   **MFAudioFormat \_ AAC**
-   **MEDIASUBTYPE \_ 原始 \_ AAC1**

如需這些 substypes 的詳細資訊，請參閱 [AAC 媒體類型](aac-media-types.md)。

針對 **MFAudioFormat \_ AAC** 子類型，媒體類型可選擇性地包含 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性。 如果有的話，這個屬性會出現在 **WAVEFORMATEX** 結構後面的 [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo)結構部分 (也就是 **wfx** 成員) 之後。 後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。 如果不存在 **MF \_ MT \_ 使用者 \_ 資料** 屬性，則會假設資料流程 AAC 低複雜度 (LC) 設定檔，而 MPEG 4 檔案接收會產生適當的範例描述方塊。

針對 **MEDIASUBTYPE \_ RAW \_ AAC1** 子類型，媒體接收器必須包含 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性，而且屬性必須包含 AudioSpecificConfig () 資料。

MPEG-2 檔案接收會使用 ' mp4a ' 範例專案搭配 objectTypeIndication = 0x40 來建立 AAC 範例描述方塊的 MPEG-2 變化。 它不會使用 MPEG-2 物件類型。

## <a name="mp3-audio"></a>MP3 音訊

若為 MP3 音訊，MPEG-2 file 接收器可以從標準音頻媒體類型產生範例描述方塊。  (查看 [音訊媒體類型](audio-media-types.md)。 ) 

MPEG-2 檔案接收會使用 ' mp4a ' 範例專案搭配 objectTypeIndication = 0x6b 的 MPEG-2 音訊，建立 MP3 範例描述方塊的 MPEG 4 變化。

## <a name="limitations"></a>限制

-   所撰寫檔案的大小上限為 4 GB。 在 Windows 8 中，支援超過4個 GBGB 的檔案。
-   MPEG-2 檔案接收不支援 [edts] 和 [elst] 方塊 ( 編輯清單) 。

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a>Windows 8 更新至 MPEG-2 來源和接收

-   Windows 8 MPEG-2 來源和接收中新增的旋轉讀取和寫入支援。 Windows 7 MPEG-2 來源和接收中不支援此功能。

    MPEG 4 來源會讀取作用中影片播放軌的旋轉角度，作為從 ' mvhd ' 和 ' tkhd ' 旋轉角度的總和。

    Microsoft MPEG-2 接收會在 ' tkhd ' 中寫入旋轉角度，但會在 ' mvhd ' 中寫入0度的 (識別) 矩陣。 請注意，Microsoft MPEG 4 接收器只支援單一影片播放軌。

    IPropertyStore 只會讀取第一個影片播放軌的旋轉角度，作為從 ' mvhd ' 和 ' tkhd ' 旋轉角度的總和。

    IPropertyStore 只會在旋轉角度根據 ' mvhd ' 中的旋轉角度（如果有的話）調整旋轉角度之後，才在 ' tkhd ' 中寫入第一個影片播放軌的旋轉角度。

-   Windows 8 MPEG-2 來源和接收中支援 ' moof ' )  ( 的電影片段，但 ' mfra ' 不支援。
-   Windows 8 的 MPEG-2 來源支援 .h。

    MPEG 4 來源現在會將 MPEG-2 檔案格式的兩個 fourcc ' h263 ' 和 ' 263 ' 對應到 **MFVideoFormat \_ h263** 的媒體類型。

-   在 Windows 8 MPEG-2 來源的 MJPEG 中新增了更多 fourcc 支援。

    MPEG 4 來源會將 ' dmb1 ' 的 foucc 對應至 **MFVideoFormat \_ MJPG** 的媒體類型。

-   Windows 8 MPEG-2 來源中新增的漢字中繼資料支援。

    MPEG-2 來源會從 ' soal '、' soar '、' soaa '、' sonm ' 和 ' soco ' 讀取中繼資料。 IPropertyStore 會透過一組對應的 PKEYs 來讀取 Furignana 中繼資料。

    下表顯示 shell 正式名稱、屬性索引鍵，以及 MPEG-2 檔案格式的 box/標記識別項之間的對應。

    

    | 欄位                                | 屬性索引鍵                         | 標記/Box 識別碼 |
    |--------------------------------------|--------------------------------------|------------|
    | AlbumTitleSortOverride  | PKEY \_ 音樂 \_ AlbumTitleSortOverride  | soal       |
    | ArtistSortOverride      | PKEY \_ 音樂 \_ ArtistSortOverride      | 飆升       |
    | AlbumArtistSortOverride | PKEY \_ 音樂 \_ AlbumArtistSortOverride | soaa       |
    | System. TitleSortOverride             | PKEY \_ TitleSortOverride             | sonm       |
    | ComposerSortOverride    | PKEY \_ 音樂 \_ ComposerSortOverride    | soco       |

    

     

-   Windows 8 MPEG-2 來源中新增了身歷聲 3D atom 支援。

-   Windows 8 的 MPEG-2 來源和接收中新增了 AC3 和 DD + 支援。
-   針對非 fragmental 的，支援大於 4 GB 的檔案的 Windows 8 MPEG 接收器。
-   Windows 8 的 MPEG-2 來源已優化清除。

    為了減少延遲，特定搜尋位置的兩個最接近主要畫面格的資訊會透過 [**IMFSeekInfo：： GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes)公開。 由於主要畫面格沒有相依的框架，因此只會在解碼一個畫面格之後呈現畫面格。 使用 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 透過媒體來源、管線或應用程式取得這個介面。

    在 MPEG 4 來源中將速率設定為零。 當管線處於清除模式時，速率為零。

-   您可以將 SPS 和 PPS 儲存在 MPEG 4 接收的範例資料中。

    [MF \_在 MPEG 4 接收上的 MPEG4SINK \_ SPSPPS \_ 傳遞](mf-mpeg4sink-spspps-passthrough.md) 屬性定義為允許將 SPS 和 PPS 儲存在一起， (h.264 video 資料) 的輸入範例。 產生的已產生的等式剪輯可由 Windows 7 MPEG-2 來源與其他專案播放。

-   您可以從 MPEG 接收器的輸入範例中解壓縮 SPS 和 PPS。

    當 SP 和 PPS 未設定在 MPEG 接收器的輸入媒體類型上的 [MF \_ MT \_ MPEG \_ 序列 \_ 標頭](mf-mt-mpeg-sequence-header-attribute.md) 時，mpeg 4 接收會嘗試從輸入範例中解壓縮 sps 和 pps。 MPEG-2 接收會忽略任何輸入範例，直到它找到第一個 SPS 和 PPS 為止，因為沒有 SPS 和 PPS 的所有輸入範例都不能進行解碼。

-   AVC 設定記錄中的3D 資訊支援非 fragmental 的配置。
-   NALU 長度會針對 h.264 壓縮範例公開，以優化 h.264 VLD DXVA 解碼。

    MPEG-2 來源集會設定 **MFVideoFormat \_ H264** 或 **MFVideoFormat \_ H264** 輸出媒體類型的 [MF \_ NALU \_ 長度 \_](mf-nalu-length-set.md) 。 它會在每個輸出範例上設定 [MF \_ NALU \_ 長度 \_ 資訊](mf-nalu-length-information.md) 的 blob，其中有一個壓縮範例中不同 NALU 的四位元組 NALU 長度。

-   針對在 ADTS 中的的 MPEG2 音訊新增支援。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體來源和接收](media-sources-and-sinks.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> <dt>

[媒體基礎中的 MPEG 4 支援](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
