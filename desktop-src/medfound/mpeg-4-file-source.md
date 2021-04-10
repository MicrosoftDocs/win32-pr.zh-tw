---
description: MPEG-2 檔案來源會剖析3GPP 檔案。
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: MPEG-2 檔案來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191776"
---
# <a name="mpeg-4-file-source"></a>MPEG-2 檔案來源

MPEG-2 檔案來源會剖析3GPP 檔案。 如需有關檔案格式的詳細資訊，請參閱下列標準檔：

-   ISO/IEC 14496-12： *資訊技術--音訊-視覺化物件的編碼--第12部分： ISO 基底媒體檔案格式*
-   ISO/IEC 14496-14： *資訊技術--音訊-視覺化物件的編碼--第14部分：數量檔案格式*

> [!Note]  
>  (這些資源可能無法在某些語言及國家/地區使用。 ) 

 

MPEG 4 檔案來源不會將檔案中的音訊/影片資料解碼。

本主題包含下列幾節：

## <a name="file-extensions-and-mime-types"></a>副檔名和 MIME 類型

MPEG 4 檔案來源是下列副檔名的預設媒體來源。



| 副檔名 | Description           |
|----------------|-----------------------|
| .3g2           | 3GPP2                 |
| .3gp           | 3GPP                  |
| .3gp2          | 3GPP2                 |
| .3gpp          | 3GPP                  |
| .m4a           | MPEG-2 音訊          |
| .m4v           | MPEG 4 影片          |
| .mov           | Apple QuickTime 電影 |
| .mp4           | MPEG-2 音訊或影片 |
| .mp4v          | MPEG 4 影片          |



 

它也是下列 MIME 類型的預設媒體來源。



| MIME 類型 (MIME type)   | Description  |
|-------------|--------------|
| 音訊/3gpp  | 3GPP 音訊   |
| 音訊/3gpp2 | 3GPP2 音訊  |
| 音訊/的   | MPEG-2 音訊 |
| 影片/3gpp  | 3GPP 影片   |
| 影片/3gpp2 | 3GPP2 影片  |
| 影片/   | MPEG 4 影片 |



 

## <a name="media-types"></a>媒體類型

使用的是可擴充的容器格式。 使用規定規格不會定義固定的結構，以描述未設定的容器中的媒體類型。 相反地，它會定義物件階層，讓您針對每個格式定義自訂結構。 格式描述會儲存在該資料流程 ( [stsd] ) 框的範例描述中。 [範例描述] 方塊包含範例專案的清單。 針對每個範例專案，4位元組的程式碼（類似于 FOURCC）會定義格式結構。

此擴充性表示 MPEG 4 檔案來源無法辨識每個可能的格式描述。 相反地，在建立資料流程的媒體類型時，它會採用兩層式的方法。 每個媒體類型至少包含下列屬性。



| 屬性                                                                     | 描述                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                     | 等於 **MFMediaType \_ 音訊** 或 **MFMediaType \_ 影片**。     |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                            | 指定資料流程子類型。                                  |
| [MF \_ MT \_ MPEG4 \_ 範例 \_ 說明](mf-mt-mpeg4-sample-description.md)      | 以二進位 blob 的形式包含完整的範例描述方塊。 |
| [MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案](mf-mt-mpeg4-current-sample-entry.md) | 在 [範例描述] 方塊中指定目前的專案。     |



 

MPEG 4 檔案來源會辨識某些範例專案類型。 針對這些專案，它可以剖析格式結構並建立完整的媒體類型，以及描述格式詳細資料的其他屬性。 請參閱 [媒體類型屬性](media-type-attributes.md)。

MPEG 4 檔案來源可以剖析下列範例專案。



| 範例輸入碼 | 主要類型 | Subtype                                                               | 描述                                         | 附註                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alaw            | 音訊      | **WAVE \_ 格式 \_ ALAW**                                                | 定律編碼                                        |                                                                                                                                                                                                  |
| 幅            | 影片      | **MFVideoFormat \_ MJPG**                                               | 相片-JPEG 資料流程                                   | QuickTime 容器格式也支援具有 ' mjpa ' 或 ' mjpb ' 專案的動畫 JPEG 串流，但 MPEG 4 檔案來源並不提供這些類型的完整媒體類型。               |
| avc1            | 影片      | **MFVideoFormat \_ H264**                                               | H.264 影片                                         |                                                                                                                                                                                                  |
| mp4a            | 音訊      | **MFAudioFormat \_ AAC**<br/> **MFAudioFormat \_ MP3**<br/>   | AAC 或 MP3                                          | ' Mp4a ' 專案可以描述其他 MPEG 音訊格式，但 MPEG 4 檔案來源不會剖析格式結構。                                                                          |
| 'mp4v'            | 影片      | **MFVideoFormat \_ M4S2**<br/> **MFVideoFormat \_ MP4V**<br/> | MPEG 4 第2部分                                       | **MFVideoFormat \_M4S2** 可用於 mpeg-2 第2部分的簡單設定檔。<br/> **MFVideoFormat \_MP4V** 適用于所有其他 MPEG 4 第2部分的設定檔，包括 Advanced Simple Profile。<br/> |
| 原始            | 音訊      | **MFAudioFormat \_ PCM**                                                | 8位 PCM 音訊                                     |                                                                                                                                                                                                  |
| 'sowt'            | 音訊      | **MFAudioFormat \_ PCM**                                                | 16位位元組由小到大 PCM 音訊                      |                                                                                                                                                                                                  |
| 補            | 音訊      | **MFAudioFormat \_ PCM**                                                | 16位的位元組由大到小 PCM 音訊                         | MPEG-2 檔案來源會將音訊資料轉換為位元組由小到小的格式。                                                                                                                          |
| ulaw            | 音訊      | **WAVE \_ 格式 \_ MULAW**                                               | μ定律編碼                                        |                                                                                                                                                                                                  |
| ' vc-1 '            | 影片      | **MFVideoFormat \_ WVC1**                                               | VC-1 影片                                          |                                                                                                                                                                                                  |
| 以上            | 音訊      | **MFAudioFormat \_ PCM**                                                | 8位或16位的位元組由大到小 PCM 音訊                | MPEG-2 檔案來源會將音訊資料轉換為位元組由小到小的格式。                                                                                                                          |
| 0x00000000        | 音訊      | **MFAudioFormat \_ PCM**                                                | 8位或16位的位元組由大到小 PCM 音訊                | MPEG-2 檔案來源會將音訊資料轉換為位元組由小到小的格式。                                                                                                                          |
| 0x6d730002        | 音訊      | **WAVE \_ 格式 \_ ADPCM**                                               | 適應性差異脈衝程式碼 (ADPCM)  |                                                                                                                                                                                                  |
| 0x6d730011        | 音訊      | **WAVE \_ 格式 \_ IMA \_ ADPCM**                                          | ADPCM                                               |                                                                                                                                                                                                  |



 

針對上表中未顯示的任何其他程式碼，MPEG 檔來源會設定子類型，如下所示：

1.  *子類型* = MFMPEG4Format \_ 基底
2.  *子類型*。Data1 = 範例輸入碼

針對未顯示在表格中的程式碼，解碼器必須使用 [MF \_ MT \_ MPEG4 \_ 範例 \_ 描述](mf-mt-mpeg4-sample-description.md) 屬性來剖析範例描述方塊。

如需範例輸入碼清單以及相關規格的連結，請參閱「數量的」 [註冊授權](https://mp4ra.org) 網站。

## <a name="limitations"></a>限制

MPEG-2 檔案來源不支援下列檔的下列功能：

-   外部追蹤。
-   電影片段 ( [moof] 或 [mfra] 方塊) 。 Windows 8 支援 ' moof '。
-   資料流程處理的簡報。 MPEG-2 檔案來源會以無訊息方式忽略提示追蹤。
-   依 SMPTE 時間碼搜尋。
-   壓縮 ( ' cmov ' ) 原子。

僅支援影片和音訊串流。 任何包含其他資料流程類型的追蹤都會以無訊息方式略過。 媒體資料必須放在 ' mdat ' 原子內。

如果已安裝 Windows Vista 的平臺更新補充，則會在 Windows Vista 上提供 MPEG-2 檔案來源，但只能使用 [來源讀取器](source-reader.md)在 windows vista 上進行存取。

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
-   針對非 fragmental 的，Windows 8 的 MPEG-2 接收器支援大於 4 gb 的檔案 (GB) 。
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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源和接收](media-sources-and-sinks.md)
</dt> <dt>

[媒體基礎中的 MPEG 4 支援](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




